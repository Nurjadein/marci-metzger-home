<template>
  <header
    class="fixed inset-x-0 top-0 z-50 transition-all duration-300"
    :class="
      isScrolled
        ? 'border-b border-slate-200 bg-white/95 shadow-sm backdrop-blur-md'
        : 'bg-transparent'
    "
  >
    <nav
      class="mx-auto flex h-20 max-w-7xl items-center justify-between px-6 lg:px-8"
      aria-label="Main navigation"
    >
      <a
        href="#"
        class="flex flex-col leading-none"
        :class="isScrolled ? 'text-slate-900' : 'text-white'"
      >
        <span class="text-sm font-semibold uppercase tracking-[0.18em]">
          Marci Metzger
        </span>

        <span
          class="mt-1 text-[10px] font-medium uppercase tracking-[0.2em]"
          :class="isScrolled ? 'text-slate-500' : 'text-white/70'"
        >
          The Ridge Realty Group
        </span>
      </a>

      <div class="hidden items-center gap-8 lg:flex">
        <a
          v-for="item in navigation"
          :key="item.href"
          :href="item.href"
          class="text-sm font-medium transition"
          :class="
            isScrolled
              ? 'text-slate-600 hover:text-slate-900'
              : 'text-white/85 hover:text-white'
          "
        >
          {{ item.label }}
        </a>

        <a
          href="#contact"
          class="rounded-full px-5 py-2.5 text-sm font-semibold transition"
          :class="
            isScrolled
              ? 'bg-slate-900 text-white hover:bg-slate-700'
              : 'bg-white text-slate-900 hover:bg-white/90'
          "
        >
          Get Started
        </a>
      </div>

      <button
        type="button"
        :aria-expanded="isMenuOpen"
        aria-controls="mobile-navigation"
        aria-label="Toggle navigation menu"
        class="flex h-10 w-10 items-center justify-center rounded-full transition lg:hidden"
        :class="
          isScrolled
            ? 'text-slate-900 hover:bg-slate-100'
            : 'text-white hover:bg-white/10'
        "
        @click="isMenuOpen = !isMenuOpen"
      >
        <svg
          v-if="!isMenuOpen"
          viewBox="0 0 24 24"
          class="h-6 w-6"
          fill="none"
          stroke="currentColor"
          stroke-width="1.8"
          aria-hidden="true"
        >
          <path d="M4 7h16M4 12h16M4 17h16" />
        </svg>

        <svg
          v-else
          viewBox="0 0 24 24"
          class="h-6 w-6"
          fill="none"
          stroke="currentColor"
          stroke-width="1.8"
          aria-hidden="true"
        >
          <path d="m6 6 12 12M18 6 6 18" />
        </svg>
      </button>
    </nav>

    <Transition
      enter-active-class="overflow-hidden transition-all duration-300 ease-out"
      enter-from-class="max-h-0 opacity-0"
      enter-to-class="max-h-[500px] opacity-100"
      leave-active-class="overflow-hidden transition-all duration-200 ease-in"
      leave-from-class="max-h-[500px] opacity-100"
      leave-to-class="max-h-0 opacity-0"
    >
      <div
        v-if="isMenuOpen"
        id="mobile-navigation"
        class="border-t border-slate-200 bg-white lg:hidden"
      >
        <div class="mx-auto max-w-7xl px-6 py-5">
          <nav aria-label="Mobile navigation">
            <div class="flex flex-col">
              <a
                v-for="item in navigation"
                :key="item.href"
                :href="item.href"
                class="border-b border-slate-100 py-4 text-sm font-medium text-slate-700 transition hover:text-slate-900"
                @click="handleMobileNavigation(item.href)"
              >
                {{ item.label }}
              </a>

              <a
                href="#contact"
                class="mt-5 rounded-full bg-slate-900 px-5 py-3 text-center text-sm font-semibold text-white transition hover:bg-slate-700"
                @click="handleMobileNavigation('#contact')"
              >
                Get Started
              </a>
            </div>
          </nav>
        </div>
      </div>
    </Transition>
  </header>
</template>

<script setup lang="ts">
import { onBeforeUnmount, onMounted, ref } from 'vue'

const isScrolled = ref(false)
const isMenuOpen = ref(false)

const navigation = [
  { label: 'About', href: '#about' },
  { label: 'Get It Sold', href: '#sold' },
  { label: 'Properties', href: '#properties' },
  { label: 'Services', href: '#services' },
  { label: 'Contact', href: '#contact' },
]

const handleScroll = () => {
  isScrolled.value = window.scrollY > 40
}

const handleMobileNavigation = (href: string) => {
  isMenuOpen.value = false

  window.requestAnimationFrame(() => {
    const target = document.querySelector<HTMLElement>(href)

    target?.scrollIntoView({
      behavior: 'smooth',
      block: 'start',
    })
  })
}

onMounted(() => {
  handleScroll()

  window.addEventListener('scroll', handleScroll, {
    passive: true,
  })
})

onBeforeUnmount(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>
