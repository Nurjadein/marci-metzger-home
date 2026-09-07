<template>
  <section id="services" class="bg-slate-100 py-24 sm:py-32">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="max-w-3xl">
        <p
          class="text-sm font-medium uppercase tracking-[0.3em] text-slate-500"
        >
          Our Services
        </p>

        <h2
          class="mt-5 text-5xl font-semibold tracking-tight text-slate-900 sm:text-6xl lg:text-7xl"
        >
          Real estate
          <span class="font-light italic">done right.</span>
        </h2>

        <p class="mt-6 max-w-2xl text-lg leading-8 text-slate-600">
          Whether you're buying, selling, or exploring your options, our team
          is here to make the process clear, confident, and straightforward.
        </p>
      </div>

      <div class="mt-16 grid gap-6 lg:grid-cols-3">
        <article class="group overflow-hidden rounded-3xl bg-white">
          <div class="relative h-72 overflow-hidden">
            <img
              :src="realEstateImage"
              alt="Real estate services"
              class="h-full w-full object-cover transition duration-700 group-hover:scale-105"
            />

            <div
              class="absolute inset-0 bg-gradient-to-t from-slate-950/60 via-slate-950/10 to-transparent"
            ></div>

            <div class="absolute left-6 top-6">
              <span
                class="flex h-11 w-11 items-center justify-center rounded-full bg-white/95 text-sm font-semibold text-slate-900"
              >
                01
              </span>
            </div>
          </div>

          <div class="p-8 sm:p-9">
            <h3
              class="text-2xl font-semibold tracking-tight text-slate-900"
            >
              Real estate
              <span class="font-light italic">done right.</span>
            </h3>

            <p class="mt-5 text-base leading-7 text-slate-600">
              Nervous about your property adventure? Don't be. Whether you're
              getting ready to buy or sell your residence, looking at investment
              properties, or just curious about the markets, our team ensures
              you get the best experience possible!
            </p>
          </div>
        </article>

        <article class="group overflow-hidden rounded-3xl bg-white">
          <div class="relative h-72 overflow-hidden">
            <img
              :src="commercialResidentialImage"
              alt="Commercial and residential real estate"
              class="h-full w-full object-cover transition duration-700 group-hover:scale-105"
            />

            <div
              class="absolute inset-0 bg-gradient-to-t from-slate-950/60 via-slate-950/10 to-transparent"
            ></div>

            <div class="absolute left-6 top-6">
              <span
                class="flex h-11 w-11 items-center justify-center rounded-full bg-white/95 text-sm font-semibold text-slate-900"
              >
                02
              </span>
            </div>
          </div>

          <div class="p-8 sm:p-9">
            <h3
              class="text-2xl font-semibold tracking-tight text-slate-900"
            >
              Commercial &
              <span class="font-light italic">Residential</span>
            </h3>

            <p class="mt-5 text-base leading-7 text-slate-600">
              Large or small, condo or mansion, we can find it and get at the
              price that's right. Fixer-uppers? Luxury? We can help with all of
              it! We live, work, and play in this community. Happy to help you
              find where to put your hard-earned dollars.
            </p>
          </div>
        </article>

        <article class="group overflow-hidden rounded-3xl bg-white">
          <div class="relative h-72 overflow-hidden">
            <img
              :src="expertiseImage"
              alt="Real estate expertise"
              class="h-full w-full object-cover transition duration-700 group-hover:scale-105"
            />

            <div
              class="absolute inset-0 bg-gradient-to-t from-slate-950/60 via-slate-950/10 to-transparent"
            ></div>

            <div class="absolute left-6 top-6">
              <span
                class="flex h-11 w-11 items-center justify-center rounded-full bg-white/95 text-sm font-semibold text-slate-900"
              >
                03
              </span>
            </div>
          </div>

          <div class="p-8 sm:p-9">
            <h3
              class="text-2xl font-semibold tracking-tight text-slate-900"
            >
              Rely on
              <span class="font-light italic">expertise.</span>
            </h3>

            <p class="mt-5 text-base leading-7 text-slate-600">
              If you have questions about affordability, credit, and loan
              options, trust us to connect you with the right people to get the
              answers you need in a timely fashion. We make sure you feel
              confident and educated every step of the way.
            </p>
          </div>
        </article>
      </div>

      <div
        class="mt-12 flex flex-col gap-6 border-t border-slate-300 pt-8 sm:flex-row sm:items-center sm:justify-between"
      >
        <p class="max-w-xl text-base leading-7 text-slate-600">
          Ready to make your next move? Let's talk about what you're looking
          for.
        </p>

        <a
          href="#contact"
          class="inline-flex shrink-0 items-center text-sm font-semibold text-slate-900 transition hover:text-slate-500"
        >
          Get in touch
          <span aria-hidden="true" class="ml-2 text-lg">→</span>
        </a>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import commercialResidentialImage from '@/assets/images/commercial-and-residential.webp'
import realEstateImage from '@/assets/images/real-estate-done-right.webp'
import expertiseImage from '@/assets/images/rely-on-expertise.webp'
</script>
