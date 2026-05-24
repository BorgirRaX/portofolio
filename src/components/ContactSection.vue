<script setup>
// ContactSection component
</script>

<template>
  <section
    id="contact"
    class="pt-12 pb-20 md:pt-16 md:pb-24 bg-transparent relative"
  >
    <!-- Subtle dotted texture transitioning from Projects -->
    <div
      class="absolute -top-[150px] bottom-0 left-0 right-0 pointer-events-none z-0 opacity-40 dark:opacity-20 text-primary/60"
      style="
        background-image: radial-gradient(currentColor 1.5px, transparent 1.5px);
        background-size: 32px 32px;
        mask-image: linear-gradient(to bottom, transparent 0%, black 15%, transparent 60%);
        -webkit-mask-image: linear-gradient(to bottom, transparent 0%, black 15%, transparent 60%);
      "
    ></div>

    <!-- Right-side ambient dotted grid behind CTA buttons -->
    <div
      class="absolute inset-0 pointer-events-none z-0 opacity-50 dark:opacity-20 text-primary/70"
      style="
        background-image: radial-gradient(currentColor 1.5px, transparent 1.5px);
        background-size: 28px 28px;
        mask-image: radial-gradient(ellipse at 75% 55%, black 0%, rgba(0,0,0,0.6) 40%, transparent 70%);
        -webkit-mask-image: radial-gradient(ellipse at 75% 55%, black 0%, rgba(0,0,0,0.6) 40%, transparent 70%);
      "
    ></div>

    <!-- Doodle connector crossing the boundary -->
    <div class="absolute -top-10 left-1/2 -translate-x-1/2 flex flex-col items-center pointer-events-none select-none z-20">
      <svg class="w-3 h-14 text-primary/40 dark:text-primary/30" viewBox="0 0 20 80" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M10,0 Q18,20 5,40 T10,80" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-dasharray="3 4" />
      </svg>
      <span class="font-handwritten text-[11px] text-text-muted/60 -mt-2">the end is near</span>
    </div>

    <!-- Ambient transition glow from Projects to Contact -->
    <div
      class="absolute -top-[160px] left-1/3 w-[600px] h-[300px] rounded-full bg-primary/4 dark:bg-primary/2 blur-[130px] pointer-events-none z-0"
    ></div>

    <!-- Ambient glow background overlay -->
    <div
      class="absolute bottom-0 left-1/3 translate-y-1/2 w-[250px] h-[250px] rounded-full bg-primary/3 blur-[90px] pointer-events-none z-0"
    ></div>

    <div class="max-w-5xl mx-auto px-6 relative z-10">
      <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 lg:gap-16 items-center">
        <!-- LEFT SIDE: Text and Headings (7 cols) -->
        <div class="lg:col-span-7 flex flex-col items-start text-left relative">
          <!-- Let's Talk Eyebrow -->
          <span
            class="font-mono text-xs font-semibold tracking-widest text-primary uppercase mb-4 block"
          >
            // LET&apos;S TALK
          </span>

          <!-- Headline with Hand-drawn Underlines -->
          <h2
            class="font-display font-bold text-3xl md:text-5xl text-accent-white mb-6 leading-tight tracking-tight"
          >
            Got an idea, brand, or weird project in mind?<br />
            <span class="relative inline-block text-primary mt-1">
              Let&apos;s talk.
              <span
                class="absolute left-0 -bottom-2 w-full h-[4px] bg-primary/45 rounded-full"
              ></span>
              <span
                class="absolute left-1 -bottom-3.5 w-[96%] h-[2px] bg-primary/30 rounded-full"
              ></span>
            </span>
          </h2>

          <!-- Subtext -->
          <p
            class="font-sans text-sm sm:text-base text-text-muted leading-loose font-light max-w-[58ch] mb-8"
          >
            I&apos;m open to freelance project, landing page, frontend collaboration, or just chat about
            internet and coffee.
          </p>

          <!-- Coffee micro copy & Handwritten Arrow -->
          <div class="flex items-center gap-2 select-none text-primary/40 mt-2 ml-1">
            <span class="font-handwritten text-sm text-text-muted/80 tracking-wide">
              usually replies after coffee ☕
            </span>
            <svg
              class="w-8 h-8 text-primary/30 transform rotate-25 pointer-events-none select-none"
              viewBox="0 0 100 100"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M15,15 C35,10 50,30 40,55"
                stroke="currentColor"
                stroke-width="1.8"
                stroke-linecap="round"
              />
              <path
                d="M28,49 L43,58 L39,41"
                stroke="currentColor"
                stroke-width="1.8"
                stroke-linecap="round"
              />
            </svg>
          </div>
        </div>

        <!-- RIGHT SIDE: Stacked CTAs & Sticky note (5 cols) -->
        <div
          class="lg:col-span-5 flex flex-col items-center lg:items-start relative w-full lg:pl-8 py-8"
        >
          <!-- Floating decorative hand-drawn star identical to skills/about -->
          <svg
            class="absolute -top-6 right-12 w-8 h-8 text-primary/30 animate-pulse-slow select-none pointer-events-none"
            viewBox="0 0 100 100"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M 48,12 Q 62,48 76,86 Q 44,60 12,36 Q 50,36 88,38 Q 58,64 28,88 Q 36,48 52,10"
              stroke="currentColor"
              stroke-width="3"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
          </svg>

          <!-- Scrapbook Sticky Note -->
          <div
            class="absolute -left-10 -bottom-14 hidden lg:flex items-center gap-1 z-20 select-none -rotate-6 transition-transform duration-700 ease-[cubic-bezier(0.16,1,0.3,1)] hover:-rotate-2 hover:scale-105"
          >
            <div
              class="w-24 h-24 bg-[#fdf5cb] text-neutral-800 p-3 shadow-[0_12px_28px_rgba(0,0,0,0.08),0_2px_4px_rgba(0,0,0,0.04)] select-none z-20 flex flex-col justify-between border border-neutral-300/30 relative"
            >
              <!-- Torn Aged Scotch Tape doodle physically holding the note -->
              <div
                class="absolute -top-3 left-1/2 -translate-x-1/2 w-11 h-5 bg-[#f4ebd0]/50 dark:bg-[#f4ebd0]/30 border-x border-dashed border-neutral-400/25 backdrop-blur-[1.5px] rotate-[-4deg] z-30 pointer-events-none select-none shadow-[0_1px_3px_rgba(0,0,0,0.04)]"
                style="clip-path: polygon(0% 12%, 8% 0%, 15% 10%, 25% 1%, 35% 12%, 45% 0%, 55% 10%, 65% 2%, 75% 12%, 85% 0%, 92% 8%, 100% 0%, 100% 88%, 92% 100%, 82% 88%, 72% 98%, 62% 88%, 52% 100%, 42% 88%, 32% 98%, 22% 88%, 12% 100%, 5% 88%, 0% 100%);"
              ></div>
              <div
                class="absolute top-1 left-1/2 -translate-x-1/2 w-6 h-1 bg-neutral-400/20 rounded"
              ></div>
              <span
                class="font-handwritten text-[9px] leading-tight font-semibold text-neutral-700 pt-0.5"
                >currently debugging life 🐛</span
              >
              <span class="font-mono text-[5px] text-neutral-400 self-end">BorgirRaX</span>
            </div>
          </div>

          <!-- Primary and Secondary CTA Stack -->
          <div class="flex flex-col gap-5 w-full max-w-sm relative z-10">
            <!-- Primary WhatsApp CTA -->
            <a
              href="https://wa.me/6282151887927"
              target="_blank"
              rel="noopener noreferrer"
              class="group/btn inline-flex items-center justify-between px-7 py-4 rounded-full bg-primary text-dark-navy border border-primary font-mono text-xs tracking-wider uppercase font-semibold transition-all duration-500 ease-[cubic-bezier(0.16,1,0.3,1)] hover:bg-primary/95 hover:-translate-y-1 hover:shadow-[0_12px_35px_rgba(74,158,204,0.25)] cursor-pointer"
            >
              <div class="flex items-center gap-3.5">
                <svg class="w-4 h-4 fill-current" viewBox="0 0 24 24">
                  <path
                    d="M12.031 2c-5.516 0-9.99 4.474-9.99 9.99 0 1.763.46 3.42 1.258 4.876l-1.3 4.746 4.863-1.276c1.396.762 2.99 1.196 4.674 1.196 5.516 0 10-4.484 10-10 0-5.515-4.484-9.99-10-9.99zm0 18.293c-1.528 0-3.02-.41-4.322-1.186l-.31-.184-3.21.842.857-3.128-.202-.322c-.852-1.354-1.303-2.928-1.303-4.527 0-4.566 3.716-8.283 8.283-8.283 4.567 0 8.284 3.716 8.284 8.283-.001 4.568-3.718 8.285-8.285 8.285z"
                  />
                </svg>
                  <span>Chat on WhatsApp</span>
              </div>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="w-4 h-4 transform group-hover/btn:translate-x-1.5 transition-transform duration-300"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
                stroke-width="2"
              >
                <path stroke-linecap="round" stroke-linejoin="round" d="M14 5l7 7m0 0l-7 7m7-7H3" />
              </svg>
            </a>

            <!-- Secondary Outlined Email CTA (Slightly Offset) -->
            <a
              href="mailto:jimyhendrie123@gmail.com"
              class="group/btn inline-flex items-center justify-between px-7 py-4 rounded-full border border-soft-navy hover:border-primary/50 bg-card/25 backdrop-blur-sm text-text-muted hover:text-accent-white font-mono text-xs tracking-wider uppercase transition-all duration-500 ease-[cubic-bezier(0.16,1,0.3,1)] hover:-translate-y-1 translate-x-3 cursor-pointer"
            >
              <div class="flex items-center gap-3.5">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="w-4 h-4 text-primary group-hover/btn:text-accent-white transition-colors duration-300"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke="currentColor"
                  stroke-width="1.8"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"
                  />
                </svg>
                <span>Send Email</span>
              </div>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="w-4 h-4 opacity-50 group-hover/btn:opacity-100 group-hover/btn:translate-x-1 transition-all duration-300"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
                stroke-width="1.8"
              >
                <path stroke-linecap="round" stroke-linejoin="round" d="M9 5l7 7-7 7" />
              </svg>
            </a>
          </div>

          <!-- Secondary Social Links with Floating Handwritten Tooltips -->
          <div
            class="mt-10 flex items-center font-mono text-[10px] tracking-widest text-text-muted/60 relative z-10 w-full max-w-sm pl-4"
          >
            <span class="uppercase opacity-45 select-none mr-8">// FIND ME</span>
            <div class="flex items-center gap-3">
              <!-- GITHUB -->
              <div class="relative group/social flex flex-col items-center">
                <!-- Tooltip -->
                <div
                  class="absolute bottom-full mb-2 px-3 py-1 bg-card border border-soft-navy rounded-lg shadow-md whitespace-nowrap opacity-0 pointer-events-none group-hover/social:opacity-100 group-hover/social:-translate-y-1 transition-all duration-300 z-30 select-none scale-90 group-hover/social:scale-100"
                >
                  <span class="font-handwritten text-xs text-text-muted tracking-wide"
                    >late night commits ⚡</span
                  >
                  <!-- Tooltip Caret -->
                  <div
                    class="absolute top-full left-1/2 -translate-x-1/2 -mt-1 border-4 border-transparent border-t-soft-navy"
                  ></div>
                </div>
                <!-- Button -->
                <a
                  href="https://github.com/BorgirRaX"
                  target="_blank"
                  rel="noopener noreferrer"
                  class="p-2 rounded-full border border-soft-navy/80 hover:border-primary/40 bg-card/20 hover:bg-card/55 transition-all duration-500 ease-[cubic-bezier(0.16,1,0.3,1)] hover:-translate-y-0.5 text-text-muted hover:text-accent-white cursor-pointer shadow-sm hover:shadow-[0_4px_12px_rgba(74,158,204,0.08)]"
                  aria-label="GitHub"
                >
                  <svg class="w-3.5 h-3.5 fill-current" viewBox="0 0 24 24">
                    <path
                      fill-rule="evenodd"
                      d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.53 1.032 1.53 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482C19.138 20.193 22 16.435 22 12.017 22 6.484 17.522 2 12 2z"
                      clip-rule="evenodd"
                    />
                  </svg>
                </a>
              </div>

              <!-- INSTAGRAM -->
              <div class="relative group/social flex flex-col items-center">
                <!-- Tooltip -->
                <div
                  class="absolute bottom-full mb-2 px-3 py-1 bg-card border border-soft-navy rounded-lg shadow-md whitespace-nowrap opacity-0 pointer-events-none group-hover/social:opacity-100 group-hover/social:-translate-y-1 transition-all duration-300 z-30 select-none scale-90 group-hover/social:scale-100"
                >
                  <span class="font-handwritten text-xs text-text-muted tracking-wide"
                    >random life snapshots 📸</span
                  >
                  <!-- Tooltip Caret -->
                  <div
                    class="absolute top-full left-1/2 -translate-x-1/2 -mt-1 border-4 border-transparent border-t-soft-navy"
                  ></div>
                </div>
                <!-- Button -->
                <a
                  href="https://instagram.com/jh.07x"
                  target="_blank"
                  rel="noopener noreferrer"
                  class="p-2 rounded-full border border-soft-navy/80 hover:border-primary/40 bg-card/20 hover:bg-card/55 transition-all duration-500 ease-[cubic-bezier(0.16,1,0.3,1)] hover:-translate-y-0.5 text-text-muted hover:text-accent-white cursor-pointer shadow-sm hover:shadow-[0_4px_12px_rgba(74,158,204,0.08)]"
                  aria-label="Instagram"
                >
                  <svg class="w-3.5 h-3.5 fill-current" viewBox="0 0 24 24">
                    <path
                      d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zM12 0C8.741 0 8.333.014 7.053.072 2.695.272.273 2.69.073 7.051C.014 8.333 0 8.741 0 12c0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98C15.668.014 15.259 0 12 0zm0 5.838a6.162 6.162 0 100 12.324 6.162 6.162 0 000-12.324zM12 16a4 4 0 110-8 4 4 0 010 8zm6.406-11.845a1.44 1.44 0 100 2.881 1.44 1.44 0 000-2.881z"
                    />
                  </svg>
                </a>
              </div>

              <!-- X / TWITTER -->
              <div class="relative group/social flex flex-col items-center">
                <!-- Tooltip -->
                <div
                  class="absolute bottom-full mb-2 px-3 py-1 bg-card border border-soft-navy rounded-lg shadow-md whitespace-nowrap opacity-0 pointer-events-none group-hover/social:opacity-100 group-hover/social:-translate-y-1 transition-all duration-300 z-30 select-none scale-90 group-hover/social:scale-100"
                >
                  <span class="font-handwritten text-xs text-text-muted tracking-wide"
                    >web3 rabbit hole 🐇</span
                  >
                  <!-- Tooltip Caret -->
                  <div
                    class="absolute top-full left-1/2 -translate-x-1/2 -mt-1 border-4 border-transparent border-t-soft-navy"
                  ></div>
                </div>
                <!-- Button -->
                <a
                  href="https://x.com/0x62Burger"
                  target="_blank"
                  rel="noopener noreferrer"
                  class="p-2 rounded-full border border-soft-navy/80 hover:border-primary/40 bg-card/20 hover:bg-card/55 transition-all duration-500 ease-[cubic-bezier(0.16,1,0.3,1)] hover:-translate-y-0.5 text-text-muted hover:text-accent-white cursor-pointer shadow-sm hover:shadow-[0_4px_12px_rgba(74,158,204,0.08)]"
                  aria-label="X (formerly Twitter)"
                >
                  <svg class="w-3.5 h-3.5 fill-current" viewBox="0 0 24 24">
                    <path
                      d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-5.214-6.817L4.99 21.75H1.68l7.73-8.835L1.254 2.25H8.08l4.713 6.231zm-1.161 17.52h1.833L7.084 4.126H5.117z"
                    />
                  </svg>
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Very subtle bottom-right decorative hand-drawn sparkle -->
    <svg
      class="absolute bottom-8 right-12 w-6 h-6 text-primary/35 pointer-events-none select-none animate-pulse-slow hidden md:block"
      viewBox="0 0 100 100"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
    >
      <path
        d="M 50,20 Q 50,50 80,50 Q 50,50 50,80 Q 50,50 20,50 Q 50,50 50,20 Z"
        stroke="currentColor"
        stroke-width="2"
        stroke-linecap="round"
        stroke-linejoin="round"
      />
    </svg>
  </section>
</template>
