<template>
  <section id="sold" class="bg-slate-100 py-24 sm:py-32">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="max-w-3xl">
        <p
          class="text-sm font-medium uppercase tracking-[0.3em] text-slate-500"
        >
          Top Residential Sales Last 5 Years
        </p>

        <h2
          class="mt-5 text-5xl font-semibold tracking-tight text-slate-900 sm:text-6xl lg:text-7xl"
        >
          Get it
          <span class="font-light italic">sold.</span>
        </h2>

        <p class="mt-6 max-w-2xl text-lg leading-8 text-slate-600">
          We helped nearly 90 clients in 2021, and closed 28.5 million in
          sales!
        </p>
      </div>

      <div
        class="mt-16 grid gap-px overflow-hidden rounded-2xl bg-slate-300 sm:grid-cols-2 lg:grid-cols-3"
      >
        <div class="bg-white p-8 sm:p-10">
          <p class="text-5xl font-semibold tracking-tight text-slate-900">
            ~90
          </p>

          <p
            class="mt-4 text-sm font-medium uppercase tracking-[0.15em] text-slate-500"
          >
            Clients helped in 2021
          </p>
        </div>

        <div class="bg-white p-8 sm:p-10">
          <p class="text-5xl font-semibold tracking-tight text-slate-900">
            $28.5M
          </p>

          <p
            class="mt-4 text-sm font-medium uppercase tracking-[0.15em] text-slate-500"
          >
            Sales closed in 2021
          </p>
        </div>

        <div class="bg-white p-8 sm:p-10 sm:col-span-2 lg:col-span-1">
          <p class="text-2xl font-semibold tracking-tight text-slate-900">
            Top Residential
          </p>

          <p
            class="mt-4 text-sm font-medium uppercase tracking-[0.15em] text-slate-500"
          >
            Sales over the last 5 years
          </p>
        </div>
      </div>

      <div class="mt-16 grid gap-5 md:grid-cols-3">
        <div class="overflow-hidden rounded-2xl">
          <img
            :src="getItSoldImage"
            alt="Marci Metzger real estate"
            class="h-full min-h-80 w-full object-cover transition duration-500 hover:scale-105"
          />
        </div>

        <div class="overflow-hidden rounded-2xl">
          <img
            :src="getItSoldImage2"
            alt="The Ridge Realty Group"
            class="h-full min-h-80 w-full object-cover transition duration-500 hover:scale-105"
          />
        </div>

        <div class="overflow-hidden rounded-2xl">
          <img
            :src="getItSoldImage3"
            alt="Pahrump real estate"
            class="h-full min-h-80 w-full object-cover transition duration-500 hover:scale-105"
          />
        </div>
      </div>

      <div class="mt-16 grid gap-12 lg:grid-cols-2 lg:gap-20">
        <div>
          <p
            class="text-sm font-medium uppercase tracking-[0.2em] text-slate-500"
          >
            Don't Just List it...
          </p>

          <h3
            class="mt-4 text-3xl font-semibold tracking-tight text-slate-900"
          >
            Get it
            <span class="font-light italic">SOLD!</span>
          </h3>

          <p class="mt-5 text-base leading-7 text-slate-600">
            We exhaust every avenue to ensure our listings are at the
            fingertips of every possible buyer, getting you top dollar for
            your home.
          </p>
        </div>

        <div>
          <p
            class="text-sm font-medium uppercase tracking-[0.2em] text-slate-500"
          >
            Guide to Buyers
          </p>

          <h3
            class="mt-4 text-3xl font-semibold tracking-tight text-slate-900"
          >
            Nobody knows the market
            <span class="font-light italic">like we do.</span>
          </h3>

          <p class="mt-5 text-base leading-7 text-slate-600">
            Enjoy having a pro at your service. Market analysis, upgrades
            lists, contractors on speed dial, & more!
          </p>
        </div>
      </div>

      <div class="mt-16 border-t border-slate-300 pt-8">
        <p class="max-w-4xl text-lg leading-8 text-slate-600">
          Our team works hard everyday to grow and learn, so that we may
          continue to excel in our market. Our clients deserve our best, &
          we want to make sure our best is better every year.
        </p>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import getItSoldImage from '@/assets/images/get-it-sold-img.webp'
import getItSoldImage2 from '@/assets/images/get-it-sold-img2.webp'
import getItSoldImage3 from '@/assets/images/get-it-sold-img3.webp'
</script>

