<template>
  <section
    id="properties"
    class="relative overflow-hidden py-24 sm:py-32"
  >
    <div class="absolute inset-0">
      <img
        :src="dreamHomeImage"
        alt=""
        aria-hidden="true"
        class="h-full w-full object-cover"
      />

      <div class="absolute inset-0 bg-slate-950/65"></div>
    </div>

    <div class="relative mx-auto max-w-7xl px-6 lg:px-8">
      <div class="max-w-3xl">
        <p
          class="text-sm font-medium uppercase tracking-[0.3em] text-white/70"
        >
          Find Your Dream Home
        </p>

        <h2
          class="mt-5 text-5xl font-semibold tracking-tight text-white sm:text-6xl lg:text-7xl"
        >
          Your search starts
          <span class="font-light italic">here.</span>
        </h2>

        <p class="mt-6 max-w-2xl text-lg leading-8 text-white/80">
          Explore available properties and narrow your search by the
          features that matter most to you.
        </p>
      </div>

      <div
        class="mt-16 rounded-3xl border border-white/20 bg-white/95 p-6 shadow-2xl backdrop-blur-sm sm:p-8 lg:p-10"
      >
        <div class="mb-8">
          <h3 class="text-2xl font-semibold tracking-tight text-slate-900">
            Search Listings
          </h3>

          <p class="mt-2 text-sm leading-6 text-slate-500">
            Find a property that fits what you're looking for.
          </p>
        </div>

        <form
          class="grid gap-5 sm:grid-cols-2 lg:grid-cols-4"
          @submit.prevent
        >
          <div class="lg:col-span-2">
            <label
              for="location"
              class="mb-2 block text-sm font-medium text-slate-700"
            >
              Location
            </label>

            <input
              id="location"
              type="text"
              placeholder="City, ZIP code, or area"
              class="w-full rounded-xl border border-slate-300 bg-white px-4 py-3.5 text-sm text-slate-900 outline-none transition placeholder:text-slate-400 focus:border-slate-900 focus:ring-1 focus:ring-slate-900"
            />
          </div>

          <div>
            <label
              for="property-type"
              class="mb-2 block text-sm font-medium text-slate-700"
            >
              Type
            </label>

            <select
              id="property-type"
              class="w-full rounded-xl border border-slate-300 bg-white px-4 py-3.5 text-sm text-slate-900 outline-none transition focus:border-slate-900 focus:ring-1 focus:ring-slate-900"
            >
              <option>Any Type</option>
              <option>Residential</option>
              <option>Commercial</option>
            </select>
          </div>

          <div>
            <label
              for="sort"
              class="mb-2 block text-sm font-medium text-slate-700"
            >
              Sort By
            </label>

            <select
              id="sort"
              class="w-full rounded-xl border border-slate-300 bg-white px-4 py-3.5 text-sm text-slate-900 outline-none transition focus:border-slate-900 focus:ring-1 focus:ring-slate-900"
            >
              <option>Newest</option>
              <option>Price: Low to High</option>
              <option>Price: High to Low</option>
            </select>
          </div>

          <div>
            <label
              for="bedrooms"
              class="mb-2 block text-sm font-medium text-slate-700"
            >
              Bedrooms
            </label>

            <select
              id="bedrooms"
              class="w-full rounded-xl border border-slate-300 bg-white px-4 py-3.5 text-sm text-slate-900 outline-none transition focus:border-slate-900 focus:ring-1 focus:ring-slate-900"
            >
              <option>Any</option>
              <option>1+</option>
              <option>2+</option>
              <option>3+</option>
              <option>4+</option>
              <option>5+</option>
            </select>
          </div>

          <div>
            <label
              for="baths"
              class="mb-2 block text-sm font-medium text-slate-700"
            >
              Baths
            </label>

            <select
              id="baths"
              class="w-full rounded-xl border border-slate-300 bg-white px-4 py-3.5 text-sm text-slate-900 outline-none transition focus:border-slate-900 focus:ring-1 focus:ring-slate-900"
            >
              <option>Any</option>
              <option>1+</option>
              <option>2+</option>
              <option>3+</option>
              <option>4+</option>
            </select>
          </div>

          <div>
            <label
              for="min-price"
              class="mb-2 block text-sm font-medium text-slate-700"
            >
              Min Price
            </label>

            <input
              id="min-price"
              type="number"
              placeholder="$0"
              min="0"
              class="w-full rounded-xl border border-slate-300 bg-white px-4 py-3.5 text-sm text-slate-900 outline-none transition placeholder:text-slate-400 focus:border-slate-900 focus:ring-1 focus:ring-slate-900"
            />
          </div>

          <div>
            <label
              for="max-price"
              class="mb-2 block text-sm font-medium text-slate-700"
            >
              Max Price
            </label>

            <input
              id="max-price"
              type="number"
              placeholder="No max"
              min="0"
              class="w-full rounded-xl border border-slate-300 bg-white px-4 py-3.5 text-sm text-slate-900 outline-none transition placeholder:text-slate-400 focus:border-slate-900 focus:ring-1 focus:ring-slate-900"
            />
          </div>

          <div class="flex items-end sm:col-span-2 lg:col-span-4">
            <button
              type="submit"
              class="w-full rounded-xl bg-slate-900 px-6 py-3.5 text-sm font-semibold text-white transition hover:bg-slate-700 focus:outline-none focus:ring-2 focus:ring-slate-900 focus:ring-offset-2"
            >
              Search Now
            </button>
          </div>
        </form>
      </div>

      <div
        class="mt-10 flex flex-col gap-5 sm:flex-row sm:items-center sm:justify-between"
      >
        <p class="text-sm leading-6 text-white/70">
          Looking for something specific? Let our team help you find it.
        </p>

        <a
          href="#contact"
          class="inline-flex items-center text-sm font-semibold text-white transition hover:text-white/70"
        >
          Talk to Marci
          <span aria-hidden="true" class="ml-2">→</span>
        </a>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import dreamHomeImage from '@/assets/images/find-your-dream-home-bg-img.webp'
</script>
