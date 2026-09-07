<template>
  <section
    id="gallery"
    class="overflow-hidden bg-white py-24 sm:py-32"
    @mouseenter="pauseAutoPlay"
    @mouseleave="resumeAutoPlay"
  >
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div
        class="flex flex-col gap-6 sm:flex-row sm:items-end sm:justify-between"
      >
        <div>
          <p
            class="text-sm font-medium uppercase tracking-[0.3em] text-slate-500"
          >
            Photo Gallery
          </p>

          <h2
            class="mt-5 max-w-3xl text-5xl font-semibold tracking-tight text-slate-900 sm:text-6xl lg:text-7xl"
          >
            A closer look at
            <span class="font-light italic">Pahrump.</span>
          </h2>
        </div>

        <div class="flex items-end justify-between gap-8 sm:pb-1">
          <p class="max-w-sm text-base leading-7 text-slate-500">
            Explore the places, homes, and community that make Pahrump worth
            calling home.
          </p>

          <div class="hidden shrink-0 text-right sm:block">
            <p class="text-xs font-medium uppercase tracking-[0.2em] text-slate-400">
              Gallery
            </p>
            <p class="mt-1 text-2xl font-semibold tracking-tight text-slate-900">
              {{ currentIndex + 1 }}
              <span class="font-light text-slate-400">
                / {{ galleryImages.length }}
              </span>
            </p>
          </div>
        </div>
      </div>

      <div class="mt-14">
        <div
          ref="galleryContainer"
          class="relative overflow-hidden rounded-2xl bg-slate-100"
          @touchstart="handleTouchStart"
          @touchend="handleTouchEnd"
        >
          <div class="relative h-[28rem] overflow-hidden sm:h-[36rem] lg:h-[42rem]">
            <img
              :src="currentImage?.src"
              :alt="currentImage?.alt"
              class="absolute inset-0 h-full w-full object-cover"
              :style="imageStyle"
              draggable="false"
            />

            <div
              class="absolute inset-0 bg-gradient-to-t from-slate-950/30 via-transparent to-transparent"
            ></div>

            <div
              class="absolute inset-x-0 bottom-0 flex items-end justify-between p-5 sm:p-7 lg:p-8"
            >
              <div class="text-white">
                <p
                  class="text-xs font-medium uppercase tracking-[0.25em] text-white/70"
                >
                  The Ridge Realty Group
                </p>

                <p class="mt-2 text-sm font-medium sm:text-base">
                  Pahrump, Nevada
                </p>
              </div>

              <div class="flex gap-2">
                <button
                  type="button"
                  aria-label="Previous gallery image"
                  class="flex h-11 w-11 items-center justify-center rounded-full border border-white/40 bg-slate-950/20 text-white backdrop-blur-sm transition hover:bg-white hover:text-slate-900 focus:outline-none focus:ring-2 focus:ring-white focus:ring-offset-2 focus:ring-offset-slate-900"
                  @click="showPrevious"
                >
                  <span aria-hidden="true" class="text-xl leading-none">
                    ←
                  </span>
                </button>

                <button
                  type="button"
                  aria-label="Next gallery image"
                  class="flex h-11 w-11 items-center justify-center rounded-full border border-white/40 bg-slate-950/20 text-white backdrop-blur-sm transition hover:bg-white hover:text-slate-900 focus:outline-none focus:ring-2 focus:ring-white focus:ring-offset-2 focus:ring-offset-slate-900"
                  @click="showNext"
                >
                  <span aria-hidden="true" class="text-xl leading-none">
                    →
                  </span>
                </button>
              </div>
            </div>
          </div>
        </div>

        <div class="mt-5 flex items-center justify-between sm:hidden">
          <p
            class="text-xs font-medium uppercase tracking-[0.2em] text-slate-400"
          >
            Gallery
          </p>

          <p class="text-sm font-semibold text-slate-900">
            {{ currentIndex + 1 }}
            <span class="font-normal text-slate-400">
              / {{ galleryImages.length }}
            </span>
          </p>
        </div>

        <div class="mt-6 flex items-center gap-2">
          <button
            v-for="(image, index) in galleryImages"
            :key="image.src"
            type="button"
            :aria-label="`Show gallery image ${index + 1}`"
            :aria-current="index === currentIndex ? 'true' : undefined"
            class="group relative h-1.5 flex-1 overflow-hidden rounded-full bg-slate-200"
            @click="goToImage(index)"
          >
            <span
              class="absolute inset-y-0 left-0 rounded-full bg-slate-900 transition-all duration-300"
              :class="index === currentIndex ? 'w-full' : 'w-0'"
            ></span>
          </button>
        </div>

        <div class="mt-6 hidden gap-3 overflow-x-auto pb-2 md:flex">
          <button
            v-for="(image, index) in galleryImages"
            :key="`thumbnail-${image.src}`"
            type="button"
            :aria-label="`Show gallery image ${index + 1}`"
            :aria-current="index === currentIndex ? 'true' : undefined"
            class="group relative h-20 w-28 shrink-0 overflow-hidden rounded-lg focus:outline-none focus:ring-2 focus:ring-slate-900 focus:ring-offset-2"
            @click="goToImage(index)"
          >
            <img
              :src="image.src"
              :alt="image.alt"
              class="h-full w-full object-cover transition duration-300 group-hover:scale-105"
              :class="
                index === currentIndex
                  ? 'scale-105'
                  : 'opacity-60 group-hover:opacity-100'
              "
              draggable="false"
            />

            <span
              v-if="index === currentIndex"
              class="absolute inset-0 ring-2 ring-inset ring-white"
            ></span>
          </button>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { computed, onBeforeUnmount, onMounted, ref } from 'vue'

import galleryImage1 from '@/assets/images/gal-img1.webp'
import galleryImage2 from '@/assets/images/gal-img2.webp'
import galleryImage3 from '@/assets/images/gal-img3.webp'
import galleryImage4 from '@/assets/images/gal-img4.webp'
import galleryImage5 from '@/assets/images/gal-img5.webp'
import galleryImage6 from '@/assets/images/gal-img6.webp'
import galleryImage7 from '@/assets/images/gal-img7.webp'

interface GalleryImage {
  src: string
  alt: string
}

const galleryImages: GalleryImage[] = [
  {
    src: galleryImage1,
    alt: 'Pahrump real estate',
  },
  {
    src: galleryImage2,
    alt: 'Pahrump property',
  },
  {
    src: galleryImage3,
    alt: 'Pahrump community',
  },
  {
    src: galleryImage4,
    alt: 'Pahrump home',
  },
  {
    src: galleryImage5,
    alt: 'Pahrump real estate',
  },
  {
    src: galleryImage6,
    alt: 'Pahrump property',
  },
  {
    src: galleryImage7,
    alt: 'Pahrump real estate',
  },
]

const currentIndex = ref(0)
const galleryContainer = ref<HTMLElement | null>(null)

const isPaused = ref(false)
const touchStartX = ref(0)
const parallaxOffset = ref(0)

let autoPlayTimer: ReturnType<typeof setInterval> | undefined

const currentImage = computed(() => {
  return galleryImages[currentIndex.value]
})

const imageStyle = computed(() => {
  return {
    transform: `translate3d(0, ${parallaxOffset.value}px, 0) scale(1.06)`,
    transition: 'transform 300ms ease-out',
  }
})

function showNext() {
  currentIndex.value =
    (currentIndex.value + 1) % galleryImages.length

  resetAutoPlay()
}

function showPrevious() {
  currentIndex.value =
    (currentIndex.value - 1 + galleryImages.length) %
    galleryImages.length

  resetAutoPlay()
}

function goToImage(index: number) {
  currentIndex.value = index
  resetAutoPlay()
}

function startAutoPlay() {
  stopAutoPlay()

  autoPlayTimer = setInterval(() => {
    if (!isPaused.value) {
      currentIndex.value =
        (currentIndex.value + 1) % galleryImages.length
    }
  }, 6000)
}

function stopAutoPlay() {
  if (autoPlayTimer) {
    clearInterval(autoPlayTimer)
    autoPlayTimer = undefined
  }
}

function resetAutoPlay() {
  startAutoPlay()
}

function pauseAutoPlay() {
  isPaused.value = true
}

function resumeAutoPlay() {
  isPaused.value = false
}

function handleTouchStart(event: TouchEvent) {
  touchStartX.value = event.changedTouches[0]?.clientX ?? 0
}

function handleTouchEnd(event: TouchEvent) {
  const touchEndX = event.changedTouches[0]?.clientX ?? 0
  const distance = touchStartX.value - touchEndX

  const swipeThreshold = 50

  if (Math.abs(distance) < swipeThreshold) {
    return
  }

  if (distance > 0) {
    showNext()
  } else {
    showPrevious()
  }
}

function handleScroll() {
  if (!galleryContainer.value) {
    return
  }

  const rect = galleryContainer.value.getBoundingClientRect()
  const viewportHeight = window.innerHeight

  if (rect.bottom < 0 || rect.top > viewportHeight) {
    return
  }

  const centerOffset =
    viewportHeight / 2 - (rect.top + rect.height / 2)

  const maxOffset = 14

  parallaxOffset.value = Math.max(
    -maxOffset,
    Math.min(maxOffset, centerOffset * 0.025),
  )
}

onMounted(() => {
  startAutoPlay()
  window.addEventListener('scroll', handleScroll, { passive: true })
  handleScroll()
})

onBeforeUnmount(() => {
  stopAutoPlay()
  window.removeEventListener('scroll', handleScroll)
})
</script>
```
