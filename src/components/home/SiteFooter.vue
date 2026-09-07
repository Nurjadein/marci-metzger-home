<template>
  <footer class="bg-slate-950 text-white">
    <div class="mx-auto max-w-7xl px-6 py-16 lg:px-8 lg:py-20">
      <div class="grid gap-12 lg:grid-cols-12">
        <div class="lg:col-span-5">
          <p class="text-sm font-semibold uppercase tracking-[0.2em] text-white">
            Marci Metzger
          </p>

          <p class="mt-2 text-xs font-medium uppercase tracking-[0.2em] text-white/40">
            The Ridge Realty Group
          </p>

          <p class="mt-6 max-w-md text-sm leading-7 text-white/60">
            Pahrump real estate expertise backed by nearly three decades of
            experience helping buyers and sellers move with confidence.
          </p>

          <a
            href="tel:+12069196886"
            class="mt-6 inline-block text-lg font-semibold text-white transition hover:text-white/70"
          >
            (206) 919-6886
          </a>
        </div>

        <div class="lg:col-span-3">
          <p
            class="text-xs font-semibold uppercase tracking-[0.25em] text-white/40"
          >
            Explore
          </p>

          <nav class="mt-6" aria-label="Footer navigation">
            <ul class="space-y-4">
              <li v-for="link in exploreLinks" :key="link.href">
                <a
                  :href="link.href"
                  class="text-sm text-white/70 transition hover:text-white"
                >
                  {{ link.label }}
                </a>
              </li>
            </ul>
          </nav>
        </div>

        <div class="lg:col-span-4">
          <p
            class="text-xs font-semibold uppercase tracking-[0.25em] text-white/40"
          >
            Visit
          </p>

          <address
            class="mt-6 text-sm not-italic leading-7 text-white/70"
          >
            3190 HW-160, Suite F<br />
            Pahrump, Nevada 89048<br />
            United States
          </address>

          <div class="mt-6">
            <p class="text-xs uppercase tracking-[0.2em] text-white/40">
              Office Hours
            </p>

            <p class="mt-2 text-sm text-white/70">
              Daily · 8:00 AM–7:00 PM
            </p>
          </div>

          <a
            href="https://www.google.com/maps/dir/?api=1&destination=3190%20HW-160%2C%20Suite%20F%2C%20Pahrump%2C%20Nevada%2089048"
            target="_blank"
            rel="noopener noreferrer"
            class="mt-6 inline-flex items-center text-sm font-semibold text-white transition hover:text-white/70"
          >
            Get directions
            <span aria-hidden="true" class="ml-2">↗</span>
          </a>
        </div>
      </div>

      <div
        class="mt-16 flex flex-col gap-6 border-t border-white/10 pt-8 sm:flex-row sm:items-center sm:justify-between"
      >
        <p class="text-xs text-white/40">
          Connect with us
        </p>

        <div class="flex items-center gap-3">
          <a
            href="https://www.facebook.com/MarciHomes/"
            target="_blank"
            rel="noopener noreferrer"
            aria-label="Facebook"
            class="flex h-10 w-10 items-center justify-center rounded-full border border-white/10 text-white/60 transition hover:border-white/30 hover:text-white"
          >
            <svg
              viewBox="0 0 24 24"
              class="h-5 w-5"
              fill="currentColor"
              aria-hidden="true"
            >
              <path
                d="M14.5 8.5H17V5.1c-.43-.06-1.91-.18-3.63-.18-3.6 0-6.07 2.2-6.07 6.27v3.5H3.27v3.8H7.8V24h4.4v-5.51h3.63l.58-3.8H12.2v-3.07c0-1.1.3-1.85 2.3-1.85Z"
              />
            </svg>
          </a>

          <a
            href="https://www.instagram.com/marcimetzger_theridge/"
            target="_blank"
            rel="noopener noreferrer"
            aria-label="Instagram"
            class="flex h-10 w-10 items-center justify-center rounded-full border border-white/10 text-white/60 transition hover:border-white/30 hover:text-white"
          >
            <svg
              viewBox="0 0 24 24"
              class="h-5 w-5"
              fill="none"
              stroke="currentColor"
              stroke-width="1.8"
              aria-hidden="true"
            >
              <rect x="3" y="3" width="18" height="18" rx="5" />
              <circle cx="12" cy="12" r="4.25" />
              <circle
                cx="17.4"
                cy="6.6"
                r="1"
                fill="currentColor"
                stroke="none"
              />
            </svg>
          </a>

          <a
            href="https://www.linkedin.com/in/marci-metzger-30642496/"
            target="_blank"
            rel="noopener noreferrer"
            aria-label="LinkedIn"
            class="flex h-10 w-10 items-center justify-center rounded-full border border-white/10 text-white/60 transition hover:border-white/30 hover:text-white"
          >
            <svg
              viewBox="0 0 24 24"
              class="h-5 w-5"
              fill="currentColor"
              aria-hidden="true"
            >
              <path
                d="M5.2 3.5A2.2 2.2 0 1 1 5.2 7.9a2.2 2.2 0 0 1 0-4.4ZM3.4 9.4h3.6V21H3.4V9.4Zm5.8 0h3.45V11h.05c.48-.91 1.65-1.87 3.4-1.87 3.64 0 4.31 2.4 4.31 5.52V21h-3.6v-5.62c0-1.34-.03-3.06-1.86-3.06-1.86 0-2.15 1.45-2.15 2.96V21H9.2V9.4Z"
              />
            </svg>
          </a>

          <a
            href="https://www.yelp.com/biz/xr3yQN_m2SgO0R_7S6p62w"
            target="_blank"
            rel="noopener noreferrer"
            aria-label="Yelp"
            class="flex h-10 w-10 items-center justify-center rounded-full border border-white/10 text-white/60 transition hover:border-white/30 hover:text-white"
          >
            <svg
              viewBox="0 0 24 24"
              class="h-5 w-5"
              fill="currentColor"
              aria-hidden="true"
            >
              <path
                d="M11.15 2.4c.35-.25.82-.2 1.1.12.52.61 1.22 1.58 1.62 2.47.34.76.54 1.65.61 2.28.08.77-.59 1.4-1.34 1.28l-2.83-.46c-.75-.12-1.15-.98-.77-1.63l1.61-2.77ZM7.08 7.1c.3-.7 1.18-.96 1.82-.54l2.42 1.59c.64.42.66 1.34.05 1.79l-2.31 1.58c-.61.42-1.43.16-1.69-.54L6.3 8.73c-.16-.43-.1-.88.1-1.63.13-.01.38-.01.68 0Zm-2.65 4.72c.75-.08 1.68-.07 2.45.05  . . ."
              />
            </svg>
          </a>
        </div>
      </div>

      <div class="mt-8 border-t border-white/10 pt-6">
        <p class="text-xs text-white/30">
          © {{ currentYear }} Marci Metzger · The Ridge Realty Group. All rights reserved.
        </p>
      </div>
    </div>
  </footer>
</template>

<script setup lang="ts">
const currentYear = new Date().getFullYear()

const exploreLinks = [
  { label: 'Home', href: '#' },
  { label: 'About', href: '#about' },
  { label: 'Get It Sold', href: '#sold' },
  { label: 'Properties', href: '#properties' },
  { label: 'Services', href: '#services' },
  { label: 'Contact', href: '#contact' },
]
</script>
