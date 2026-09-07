<template>
  <section id="contact" class="bg-white py-24 sm:py-32">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="grid gap-16 lg:grid-cols-12 lg:gap-20">
        <div class="lg:col-span-5">
          <p
            class="text-sm font-medium uppercase tracking-[0.3em] text-slate-500"
          >
            Call or Visit
          </p>

          <h2
            class="mt-5 text-5xl font-semibold tracking-tight text-slate-900 sm:text-6xl lg:text-7xl"
          >
            Let's make your
            <span class="font-light italic">next move.</span>
          </h2>

          <div class="mt-12 space-y-8">
            <div>
              <p
                class="text-xs font-semibold uppercase tracking-[0.2em] text-slate-400"
              >
                Visit
              </p>

              <address
                class="mt-2 max-w-sm text-base leading-7 text-slate-700 not-italic"
              >
                3190 HW-160, Suite F<br />
                Pahrump, Nevada 89048<br />
                United States
              </address>
            </div>

            <div>
              <p
                class="text-xs font-semibold uppercase tracking-[0.2em] text-slate-400"
              >
                Call
              </p>

              <a
                href="tel:+12069196886"
                class="mt-2 inline-block text-xl font-semibold tracking-tight text-slate-900 transition hover:text-slate-500"
              >
                (206) 919-6886
              </a>
            </div>

            <div>
              <p
                class="text-xs font-semibold uppercase tracking-[0.2em] text-slate-400"
              >
                Office Hours
              </p>

              <p class="mt-2 text-base leading-7 text-slate-700">
                Daily · 8:00 AM–7:00 PM
              </p>

              <p class="mt-1 text-sm leading-6 text-slate-500">
                Appointments outside office hours available upon request.
              </p>
            </div>

            <div>
              <p
                class="text-xs font-semibold uppercase tracking-[0.2em] text-slate-400"
              >
                Directions
              </p>

              <a
                href="https://www.google.com/maps/dir/?api=1&destination=3190%20HW-160%2C%20Suite%20F%2C%20Pahrump%2C%20Nevada%2089048"
                target="_blank"
                rel="noopener noreferrer"
                class="mt-3 inline-flex items-center rounded-full bg-slate-900 px-6 py-3 text-sm font-semibold text-white transition hover:bg-slate-700"
              >
                Get directions
                <span aria-hidden="true" class="ml-2">↗</span>
              </a>
            </div>
          </div>
        </div>

        <div class="lg:col-span-7">
          <div class="rounded-3xl bg-slate-100 p-6 sm:p-8 lg:p-10">
            <div>
              <p
                class="text-xs font-semibold uppercase tracking-[0.2em] text-slate-400"
              >
                Send a Message
              </p>

              <h3
                class="mt-3 text-3xl font-semibold tracking-tight text-slate-900"
              >
                How can we help?
              </h3>

              <p class="mt-3 text-sm leading-6 text-slate-500">
                Tell us what you're looking for and we'll be happy to help.
              </p>
            </div>

            <form
              class="mt-10 space-y-6"
              @submit.prevent
            >
              <div>
                <label
                  for="contact-name"
                  class="mb-2 block text-sm font-medium text-slate-700"
                >
                  Name
                </label>

                <input
                  id="contact-name"
                  type="text"
                  name="name"
                  autocomplete="name"
                  placeholder="Your name"
                  class="w-full rounded-xl border border-slate-300 bg-white px-4 py-3.5 text-sm text-slate-900 outline-none transition placeholder:text-slate-400 focus:border-slate-900 focus:ring-1 focus:ring-slate-900"
                />
              </div>

              <div>
                <label
                  for="contact-email"
                  class="mb-2 block text-sm font-medium text-slate-700"
                >
                  Email
                </label>

                <input
                  id="contact-email"
                  type="email"
                  name="email"
                  autocomplete="email"
                  placeholder="you@example.com"
                  class="w-full rounded-xl border border-slate-300 bg-white px-4 py-3.5 text-sm text-slate-900 outline-none transition placeholder:text-slate-400 focus:border-slate-900 focus:ring-1 focus:ring-slate-900"
                />
              </div>

              <div>
                <label
                  for="contact-phone"
                  class="mb-2 block text-sm font-medium text-slate-700"
                >
                  Phone
                </label>

                <input
                  id="contact-phone"
                  type="tel"
                  name="phone"
                  autocomplete="tel"
                  placeholder="Your phone number"
                  class="w-full rounded-xl border border-slate-300 bg-white px-4 py-3.5 text-sm text-slate-900 outline-none transition placeholder:text-slate-400 focus:border-slate-900 focus:ring-1 focus:ring-slate-900"
                />
              </div>

              <div>
                <label
                  for="contact-message"
                  class="mb-2 block text-sm font-medium text-slate-700"
                >
                  Message
                </label>

                <textarea
                  id="contact-message"
                  name="message"
                  rows="5"
                  placeholder="How can we help?"
                  class="w-full resize-none rounded-xl border border-slate-300 bg-white px-4 py-3.5 text-sm text-slate-900 outline-none transition placeholder:text-slate-400 focus:border-slate-900 focus:ring-1 focus:ring-slate-900"
                ></textarea>
              </div>

              <button
                type="submit"
                class="w-full rounded-xl bg-slate-900 px-6 py-4 text-sm font-semibold text-white transition hover:bg-slate-700 focus:outline-none focus:ring-2 focus:ring-slate-900 focus:ring-offset-2"
              >
                Send Message
              </button>
            </form>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
