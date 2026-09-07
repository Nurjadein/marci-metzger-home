<template>
  <section class="relative flex min-h-screen items-center overflow-hidden">
    <div class="absolute inset-0">
      <img
        :src="heroImage"
        alt="Beautiful modern home"
        class="h-full w-full object-cover"
      />

      <div class="absolute inset-0 bg-slate-950/45"></div>
      <div class="absolute inset-0 bg-gradient-to-r from-slate-950/70 via-slate-950/30 to-transparent"></div>
    </div>

    <div class="relative z-10 mx-auto w-full max-w-7xl px-6 pt-24 lg:px-8">
      <div class="max-w-3xl">
        <p class="mb-5 text-sm font-medium uppercase tracking-[0.3em] text-white/80">
          The Ridge Realty Group
        </p>

        <h1 class="text-5xl font-semibold tracking-tight text-white sm:text-6xl lg:text-8xl">
          Your next chapter
          <span class="block font-light italic">
            starts here.
          </span>
        </h1>

        <p class="mt-7 max-w-xl text-lg leading-8 text-white/85">
          Pahrump real estate expertise backed by nearly three decades
          of experience helping buyers and sellers move with confidence.
        </p>

        <div class="mt-10 flex flex-wrap gap-4">
          <a
            href="#properties"
            class="rounded-full bg-white px-7 py-3.5 text-sm font-semibold text-slate-900 transition hover:bg-white/90"
          >
            Find Your Dream Home
          </a>

          <a
            href="#contact"
            class="rounded-full border border-white/70 px-7 py-3.5 text-sm font-semibold text-white transition hover:bg-white hover:text-slate-900"
          >
            Get It Sold
          </a>
        </div>
      </div>
    </div>

    <div class="absolute bottom-8 right-6 z-10 lg:right-8">
    <p class="text-xs uppercase tracking-[0.25em] text-white/70">
        Pahrump, Nevada
    </p>
    </div>
  </section>
</template>
<script setup lang="ts">
import heroImage from '@/assets/images/bg-image.webp'
</script>