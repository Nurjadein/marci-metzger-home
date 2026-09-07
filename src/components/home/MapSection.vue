<template>
  <section class="bg-slate-100 py-16 sm:py-20">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div
        class="overflow-hidden rounded-3xl bg-white shadow-sm ring-1 ring-slate-200"
      >
        <div
          class="relative h-[360px] overflow-hidden bg-slate-200 sm:h-[440px]"
          aria-label="Map showing the location of The Ridge Realty Group in Pahrump, Nevada"
          role="img"
        >
          <div class="absolute inset-0 bg-[linear-gradient(135deg,#e2e8f0_0%,#f8fafc_45%,#e2e8f0_100%)]"></div>

          <div
            class="absolute left-[-10%] top-[42%] h-16 w-[120%] rotate-[-12deg] bg-white/80 shadow-sm"
          ></div>

          <div
            class="absolute left-[18%] top-[-15%] h-[140%] w-12 rotate-[28deg] bg-white/70 shadow-sm"
          ></div>

          <div
            class="absolute bottom-[-20%] right-[20%] h-[120%] w-20 rotate-[-35deg] bg-white/60"
          ></div>

          <div
            class="absolute left-[-5%] top-[62%] h-5 w-[110%] rotate-[8deg] bg-white/60"
          ></div>

          <div
            class="absolute right-[8%] top-[-10%] h-[120%] w-5 rotate-[48deg] bg-white/50"
          ></div>

          <div
            class="absolute left-1/2 top-1/2 flex -translate-x-1/2 -translate-y-1/2 flex-col items-center"
          >
            <div
              class="relative flex h-14 w-14 items-center justify-center rounded-full bg-slate-900 shadow-xl ring-8 ring-white/60"
            >
              <svg
                viewBox="0 0 24 24"
                class="h-7 w-7 text-white"
                fill="none"
                stroke="currentColor"
                stroke-width="1.8"
                aria-hidden="true"
              >
                <path
                  d="M20 10c0 5-8 11-8 11S4 15 4 10a8 8 0 1 1 16 0Z"
                />
                <circle cx="12" cy="10" r="2.5" />
              </svg>
            </div>

            <div
              class="mt-4 rounded-full bg-white px-4 py-2 text-xs font-semibold uppercase tracking-[0.16em] text-slate-900 shadow-lg"
            >
              The Ridge Realty Group
            </div>
          </div>

          <div
            class="absolute left-6 top-6 rounded-full border border-white/70 bg-white/80 px-4 py-2 text-xs font-medium uppercase tracking-[0.18em] text-slate-500 shadow-sm backdrop-blur-sm"
          >
            Pahrump, Nevada
          </div>
        </div>

        <div
          class="flex flex-col gap-6 border-t border-slate-200 px-6 py-7 sm:px-8 lg:flex-row lg:items-center lg:justify-between lg:px-10"
        >
          <div>
            <p
              class="text-xs font-semibold uppercase tracking-[0.25em] text-slate-400"
            >
              The Ridge Realty Group
            </p>

            <h3
              class="mt-2 text-xl font-semibold tracking-tight text-slate-900"
            >
              Visit our office
            </h3>

            <p class="mt-2 text-sm leading-6 text-slate-500">
              3190 HW-160, Suite F, Pahrump, Nevada 89048
            </p>
          </div>

          <a
            href="https://www.google.com/maps/dir/?api=1&destination=3190%20HW-160%2C%20Suite%20F%2C%20Pahrump%2C%20Nevada%2089048"
            target="_blank"
            rel="noopener noreferrer"
            class="inline-flex shrink-0 items-center justify-center rounded-full bg-slate-900 px-7 py-3.5 text-sm font-semibold text-white transition duration-300 hover:-translate-y-0.5 hover:bg-slate-700 hover:shadow-lg focus:outline-none focus:ring-2 focus:ring-slate-900 focus:ring-offset-2"
          >
            Get directions
            <span aria-hidden="true" class="ml-2 text-base">↗</span>
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
</script>
