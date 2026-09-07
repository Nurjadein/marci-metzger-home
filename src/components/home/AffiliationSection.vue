<template>
  <section class="border-y border-slate-200 bg-white py-16 sm:py-20">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="text-center">
        <p
          class="text-xs font-semibold uppercase tracking-[0.3em] text-slate-400"
        >
        </p>

        <div
          class="mx-auto mt-10 grid max-w-4xl grid-cols-2 items-center gap-10 sm:grid-cols-4 sm:gap-8"
        >
          <div class="flex h-20 items-center justify-center">
            <img
              :src="affiliationImage"
              alt="Affiliation logo"
              class="max-h-20 w-auto max-w-full object-contain transition duration-300 hover:opacity-100 hover:grayscale-0"
            />
          </div>

          <div class="flex h-20 items-center justify-center">
            <img
              :src="affiliationImage1"
              alt="Equal Housing logo"
              class="max-h-20 w-auto max-w-full object-contain transition duration-300 hover:opacity-100 hover:grayscale-0"
            />
          </div>

          <div class="flex h-20 items-center justify-center">
            <img
              :src="affiliationImage2"
              alt="REALTOR logo"
              class="max-h-20 w-auto max-w-full object-contain transition duration-300 hover:opacity-100 hover:grayscale-0"
            />
          </div>

          <div class="flex h-20 items-center justify-center">
            <img
              :src="affiliationImage3"
              alt="Chamber of Commerce logo"
              class="max-h-20 w-auto max-w-full object-contain transition duration-300 hover:opacity-100 hover:grayscale-0"
            />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import affiliationImage from '@/assets/images/affiliation-img.webp'
import affiliationImage1 from '@/assets/images/affiliation-img1.webp'
import affiliationImage2 from '@/assets/images/affiliation-img2.webp'
import affiliationImage3 from '@/assets/images/affiliation-img3.webp'
</script>
