<script setup>
import { ref } from 'vue'

import nakaCoffeeImg from '@/assets/nakaCoffee_project.png'
import portfolioImg from '@/assets/portofolio_project.png'
import goProduktifImg from '@/assets/go.produktif_project.png'

const hoveredCard = ref(null)

// Data-driven reusable project items structure
const projects = [
  {
    id: 1,
    layout: 'naka',
    index: '// PROYEK #01',
    name: 'Naka Coffee',
    desc: 'Landing page untuk coffee shop dengan pendekatan emotional branding dan clean storytelling. Let the coffee aroma inspire the digital pixels.',
    tech: ['HTML', 'CSS', 'JavaScript'],
    linkText: 'Taste the vibe →',
    linkUrl: 'https://borgirrax.github.io/naka-landing-page/',
    cols: 'md:col-span-7',
    hoverRotate: 'hover:rotate-[-0.5deg]',
    accentGlow: 'rgba(212, 117, 74, 0.04)',
    accentBorder: 'rgba(212, 117, 74, 0.22)',
    stickerText: 'currently caffeinated ☕',
    image: nakaCoffeeImg,
  },
  {
    id: 2,
    layout: 'portfolio',
    index: '// PROYEK #02',
    name: 'Personal Portfolio',
    desc: 'Cinematic digital scrapbook dengan interaksi frontend, tipografi tebal, grain analog, dan detail dekoratif personal yang interaktif.',
    tech: ['Vue 3', 'Tailwind', 'Vite'],
    linkText: 'You are here →',
    linkUrl: '#',
    cols: 'md:col-span-5',
    hoverRotate: 'hover:rotate-[0.5deg]',
    accentGlow: 'rgba(74, 158, 204, 0.04)',
    accentBorder: 'rgba(74, 158, 204, 0.28)',
    stickerText: 'built with coffee & care ⚡',
    image: portfolioImg,
  },
  {
    id: 3,
    layout: 'goproduktif',
    index: '// PROYEK #03',
    name: 'GoProduktif',
    desc: 'Aplikasi produktivitas kolaboratif untuk mengelola daftar tugas harian, memantau goals, dan membantu Anda agar tetap fokus bekerja.',
    tech: ['HTML', 'CSS', 'JavaScript'],
    linkText: 'Open Site →',
    linkUrl: 'https://goproduktif.netlify.app/',
    cols: 'md:col-span-8',
    hoverRotate: 'hover:rotate-[-0.5deg]',
    accentGlow: 'rgba(74, 158, 204, 0.04)',
    accentBorder: 'rgba(74, 158, 204, 0.28)',
    stickerText: 'anti-scroll-twitter tool ⏱️',
    image: goProduktifImg,
  },
  {
    id: 4,
    layout: 'cursed',
    index: '// EXPERIMENTAL',
    name: 'Cursed Ideas',
    desc: 'Kumpulan eksperimen desain interaktif, prototipe WebGL, dan ide-ide unik yang dibuat tengah malam.',
    tech: ['In Orbit'],
    linkText: 'See the chaos 🔒',
    linkUrl: null,
    cols: 'md:col-span-4',
    hoverRotate: 'hover:rotate-[0.5deg]',
    accentGlow: 'rgba(74, 158, 204, 0.02)',
    accentBorder: 'rgba(74, 158, 204, 0.18)',
    stickerText: null,
    image: null,
  },
]
</script>

<template>
  <section id="projects" class="pt-14 pb-16 md:pt-18 md:pb-20 bg-transparent relative overflow-hidden">
    <div class="max-w-5xl mx-auto px-6 relative z-10">
      <div class="mb-16 text-left max-w-2xl relative">
        <svg
          class="absolute right-4 -top-6 w-16 h-16 text-primary/30 hidden md:block select-none pointer-events-none"
          viewBox="0 0 100 100"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M10,80 Q35,75 50,45 Q55,30 45,15"
            stroke="currentColor"
            stroke-width="1.8"
            stroke-linecap="round"
          />
          <path
            d="M35,22 L45,15 L52,25"
            stroke="currentColor"
            stroke-width="1.8"
            stroke-linecap="round"
            stroke-linejoin="round"
          />
        </svg>
        <span
          class="font-mono text-xs font-semibold tracking-widest text-primary uppercase mb-3 block"
        >
          // SELECTED PROJECTS
        </span>
        <h2
          class="font-display font-bold text-3xl md:text-5xl text-accent-white mb-5 leading-tight tracking-tight"
        >
          Things I've built<br />
          <span class="relative inline-block text-primary">
            instead of sleeping.
            <span
              class="absolute left-0 -bottom-2.5 w-full h-[4px] bg-primary/45 rounded-full"
            ></span>
            <span
              class="absolute left-[3%] -bottom-4 w-[94%] h-[2px] bg-primary/30 rounded-full"
            ></span>
          </span>
        </h2>
        <p
          class="font-sans text-xs md:text-sm text-text-muted leading-relaxed font-light max-w-[55ch]"
        >
          A few things I've designed, built, debugged at 2AM, and occasionally screamed at.
        </p>
      </div>

      <!-- Bento Grid Layout -->
      <div class="grid grid-cols-1 md:grid-cols-12 gap-6 md:gap-8">
        <div
          v-for="project in projects"
          :key="project.id"
          :class="[
            'group relative rounded-3xl border border-soft-navy bg-card/40 overflow-hidden flex flex-col justify-between p-8 md:p-10 transition-all duration-700 ease-[cubic-bezier(0.16,1,0.3,1)] hover:-translate-y-1.5',
            project.cols,
            project.hoverRotate,
          ]"
          @mouseenter="hoveredCard = project.id"
          @mouseleave="hoveredCard = null"
          :style="
            hoveredCard === project.id
              ? { boxShadow: project.accentGlow, borderColor: project.accentBorder }
              : {}
          "
        >
          <div
            v-if="project.layout === 'naka'"
            class="absolute inset-0 bg-linear-to-b from-amber-700/5 via-transparent to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-700 pointer-events-none"
          ></div>
          <div
            v-else-if="project.layout === 'portfolio' || project.layout === 'goproduktif'"
            class="absolute inset-0 bg-linear-to-b from-primary/5 via-transparent to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-700 pointer-events-none"
          ></div>

          <div
            v-if="project.layout === 'cursed'"
            class="absolute inset-0 z-0 opacity-[0.03] group-hover:opacity-[0.06] transition-opacity duration-500 pointer-events-none"
          >
            <svg width="100%" height="100%" xmlns="http://www.w3.org/2000/svg">
              <pattern id="card-grid" width="20" height="20" patternUnits="userSpaceOnUse">
                <rect width="20" height="20" fill="none" stroke="#4a9ecc" stroke-width="0.5" />
              </pattern>
              <rect width="100%" height="100%" fill="url(#card-grid)" />
            </svg>
          </div>
          <div
            v-if="project.layout === 'naka'"
            class="absolute right-4 -top-2.5 z-20 inline-flex items-center gap-1 px-2.5 py-0.5 bg-card/75 border border-amber-500/25 rounded-md shadow-sm backdrop-blur-[2px] rotate-6 select-none pointer-events-none transition-transform duration-500 group-hover:rotate-0"
          >
            <span class="font-mono text-[8px] font-medium text-amber-500 tracking-wide">
              {{ project.stickerText }}
            </span>
          </div>

          <div
            v-if="project.layout === 'portfolio'"
            class="absolute -top-3 left-16 w-14 h-5.5 bg-yellow-100/10 dark:bg-yellow-100/5 backdrop-blur-[1px] border border-yellow-200/10 -rotate-3 z-20 pointer-events-none select-none"
          ></div>
          <div
            v-if="project.layout === 'portfolio'"
            class="absolute right-4 -top-2.5 z-20 inline-flex items-center gap-1 px-2.5 py-0.5 bg-card/75 border border-text-muted/15 rounded-md shadow-sm backdrop-blur-[2px] -rotate-3 select-none pointer-events-none transition-transform duration-500 group-hover:rotate-0"
          >
            <span class="font-mono text-[8px] font-medium text-text-muted/80 tracking-wide">
              {{ project.stickerText }}
            </span>
          </div>

          <div
            v-if="project.layout === 'goproduktif'"
            class="absolute right-4 -top-2.5 z-20 inline-flex items-center gap-1 px-2.5 py-0.5 bg-card/75 border border-text-muted/15 rounded-md shadow-sm backdrop-blur-[2px] rotate-3 select-none pointer-events-none transition-transform duration-500 group-hover:rotate-0"
          >
            <span class="font-mono text-[8px] font-medium text-text-muted/80 tracking-wide">
              {{ project.stickerText }}
            </span>
          </div>

          <div
            v-if="project.layout === 'cursed'"
            class="absolute -right-3 -bottom-3 w-28 h-28 bg-[#fdf5cb] text-neutral-800 p-3.5 shadow-xl rotate-6 transition-transform duration-700 ease-[cubic-bezier(0.16,1,0.3,1)] group-hover:rotate-2 group-hover:scale-105 select-none z-20 flex flex-col justify-between border border-neutral-300/30"
          >
            <div
              class="absolute top-1 left-1/2 -translate-x-1/2 w-8 h-1.5 bg-neutral-400/20 rounded"
            ></div>
            <span
              class="font-handwritten text-xs leading-tight font-semibold text-neutral-700 tracking-wide pt-1"
            >
              currently tweaking this 🔧
            </span>
            <span class="font-mono text-[7px] text-neutral-500 self-end">v0.9.9</span>
          </div>

          <div
            v-if="project.layout === 'goproduktif'"
            class="flex flex-col md:flex-row gap-8 items-stretch h-full w-full"
          >
            <div class="flex flex-col justify-between md:w-[42%] z-10 relative">
              <div>
                <div class="flex justify-between items-start mb-6">
                  <span class="font-mono text-[9px] text-text-muted/60 tracking-widest uppercase">{{
                    project.index
                  }}</span>
                </div>

                <div class="mb-6">
                  <h3
                    class="font-display font-bold text-xl md:text-2xl text-accent-white tracking-tight group-hover:text-primary transition-colors duration-450 mb-3"
                  >
                    {{ project.name }}
                  </h3>
                  <p
                    class="font-sans text-xs md:text-sm text-text-muted/80 leading-relaxed font-light"
                  >
                    {{ project.desc }}
                  </p>
                </div>
              </div>

              <!-- Tech tags & CTA -->
              <div class="mt-auto">
                <div class="flex flex-wrap gap-1.5 mb-6">
                  <span
                    v-for="tag in project.tech"
                    :key="tag"
                    class="font-mono text-[9px] text-primary/80 bg-soft-navy/40 border border-soft-navy/80 px-2 py-0.5 rounded-full uppercase"
                  >
                    {{ tag }}
                  </span>
                </div>

                <div class="border-t border-soft-navy/40 pt-4 flex items-center justify-between">
                  <span class="font-mono text-[8px] text-text-muted/50 tracking-widest uppercase"
                    >LAUNCHED</span
                  >
                  <a
                    :href="project.linkUrl"
                    target="_blank"
                    rel="noopener noreferrer"
                    class="inline-flex items-center gap-1.5 text-xs font-semibold text-primary group-hover:text-accent-white transition-colors duration-300 cursor-pointer"
                  >
                    {{ project.linkText }}
                  </a>
                </div>
              </div>
            </div>

            <div
              class="md:w-[58%] flex items-center justify-center relative min-h-[240px] md:min-h-auto z-10"
            >
              <div
                class="w-full relative transition-all duration-700 ease-[cubic-bezier(0.16,1,0.3,1)] -rotate-2 group-hover:rotate-[0.5deg] group-hover:scale-[1.03]"
              >
                <div
                  class="relative rounded-2xl border border-soft-navy/70 bg-dark-navy/60 p-1.5 shadow-[0_20px_45px_rgba(6,12,20,0.4)] overflow-hidden"
                >
                  <img
                    :src="project.image"
                    :alt="project.name"
                    class="rounded-xl w-full h-auto object-cover opacity-85 group-hover:opacity-100 transition-opacity duration-500"
                    loading="lazy"
                  />
                  <div
                    class="absolute inset-0 bg-linear-to-t from-dark-navy/30 via-transparent to-transparent pointer-events-none rounded-xl"
                  ></div>
                </div>
              </div>
              <div
                class="absolute right-0 -bottom-4 hidden md:flex items-center gap-1 select-none pointer-events-none text-primary/45 rotate-6 z-20"
              >
                <span class="font-handwritten text-xs text-text-muted/70 tracking-wide"
                  >humble beginnings 🌱</span
                >
              </div>
            </div>
          </div>

          <div v-else class="flex flex-col justify-between h-full w-full">
            <div class="z-10 relative">
              <div class="flex justify-between items-start mb-6">
                <span
                  class="font-mono text-[9px]"
                  :class="
                    project.layout === 'naka'
                      ? 'text-amber-600/80 in-[.light]:text-amber-700'
                      : 'text-text-muted/60'
                  "
                >
                  {{ project.index }}
                </span>
                <div class="flex flex-wrap gap-1.5">
                  <span
                    v-for="tag in project.tech"
                    :key="tag"
                    :class="[
                      'font-mono text-[9px] px-2 py-0.5 rounded-full uppercase',
                      project.layout === 'naka'
                        ? 'text-amber-500 bg-amber-500/10 border border-amber-500/20 in-[.light]:text-amber-800 in-[.light]:bg-amber-600/10 in-[.light]:border-amber-600/20'
                        : 'text-primary/80 bg-soft-navy/40 border border-soft-navy/80',
                    ]"
                  >
                    {{ tag }}
                  </span>
                </div>
              </div>

              <!-- Title & Description -->
              <div class="mb-8">
                <h3
                  :class="[
                    'font-display font-bold text-xl md:text-2xl tracking-tight transition-colors duration-450 mb-3',
                    project.layout === 'naka'
                      ? 'text-accent-white group-hover:text-amber-500'
                      : 'text-accent-white group-hover:text-primary',
                  ]"
                >
                  {{ project.name }}
                </h3>
                <p
                  :class="[
                    'font-sans text-xs md:text-sm leading-relaxed font-light',
                    project.layout === 'naka'
                      ? 'text-text-muted/80 max-w-[48ch]'
                      : 'text-text-muted/80 max-w-[44ch]',
                  ]"
                >
                  {{ project.desc }}
                </p>
              </div>
            </div>

            <!-- CARD 1: Naka Coffee Screenshot Area -->
            <div
              v-if="project.layout === 'naka'"
              class="relative w-full aspect-video md:aspect-16/10 overflow-hidden rounded-2xl border border-soft-navy/60 bg-dark-navy/80 shadow-2xl z-10 mb-8 transition-transform duration-700 ease-[cubic-bezier(0.16,1,0.3,1)] group-hover:scale-[1.02]"
            >
              <img
                :src="project.image"
                :alt="project.name"
                class="w-full h-full object-cover object-top opacity-90 group-hover:opacity-100 transition-all duration-750"
                loading="lazy"
              />
              <div
                class="absolute inset-0 bg-linear-to-t from-dark-navy/30 via-transparent to-transparent pointer-events-none"
              ></div>
              <div
                class="absolute inset-0 bg-amber-500/2 mix-blend-overlay pointer-events-none"
              ></div>
            </div>

            <div
              v-else-if="project.layout === 'portfolio'"
              class="relative w-full aspect-video overflow-hidden rounded-xl border border-soft-navy/60 bg-dark-navy/80 shadow-2xl z-10 mb-8 transition-transform duration-700 ease-[cubic-bezier(0.16,1,0.3,1)] group-hover:scale-[1.02]"
            >
              <div
                class="h-6 bg-dark-navy/90 border-b border-soft-navy/40 flex items-center px-3 gap-1.5"
              >
                <div class="w-1.5 h-1.5 rounded-full bg-[#ff5f56]"></div>
                <div class="w-1.5 h-1.5 rounded-full bg-[#ffbd2e]"></div>
                <div class="w-1.5 h-1.5 rounded-full bg-[#27c93f]"></div>
                <div
                  class="h-3.5 bg-card/60 border border-soft-navy/40 rounded px-2 text-[7px] font-mono text-text-muted/50 flex items-center mx-auto w-[65%] justify-center overflow-hidden truncate"
                >
                  localhost:5173
                </div>
              </div>
              <div class="relative w-full h-[calc(100%-24px)]">
                <img
                  :src="project.image"
                  :alt="project.name"
                  class="w-full h-full object-cover object-top opacity-90 group-hover:opacity-100 transition-opacity duration-700"
                  loading="lazy"
                />
                <div
                  class="absolute inset-0 bg-linear-to-t from-dark-navy/30 to-transparent pointer-events-none"
                ></div>
              </div>
            </div>

            <div
              v-else-if="project.layout === 'cursed'"
              class="relative w-full h-32 flex items-center justify-center rounded-2xl border border-soft-navy/40 bg-dark-navy/40 z-10 mb-8 overflow-hidden"
            >
              <svg
                viewBox="0 0 100 100"
                fill="none"
                class="w-20 h-20 text-primary/30 group-hover:text-primary/60 transition-colors duration-500"
              >
                <circle
                  cx="50"
                  cy="50"
                  r="40"
                  stroke="currentColor"
                  stroke-width="0.75"
                  stroke-dasharray="4 4"
                />
                <circle cx="50" cy="50" r="28" stroke="currentColor" stroke-width="1" />
                <path
                  d="M50,10 L50,90 M10,50 L90,50"
                  stroke="currentColor"
                  stroke-width="0.5"
                  stroke-opacity="0.3"
                />
                <path
                  d="M22,22 L78,78"
                  stroke="currentColor"
                  stroke-width="0.5"
                  stroke-opacity="0.2"
                  stroke-dasharray="2 2"
                />
                <circle cx="70" cy="30" r="2" fill="currentColor" class="animate-pulse" />
                <path
                  d="M50,50 Q60,38 68,52 Q55,62 50,50 Z"
                  stroke="currentColor"
                  stroke-width="1.2"
                  stroke-linecap="round"
                  fill="currentColor"
                  fill-opacity="0.08"
                />
              </svg>
              <div class="absolute bottom-2 left-3 font-mono text-[7px] text-text-muted/30">
                SYSTEM: ACTIVE
              </div>
            </div>

            <div
              class="relative z-10 mt-auto flex items-center justify-between border-t border-soft-navy/40 pt-5"
            >
              <span
                class="font-mono text-[9px] tracking-widest uppercase"
                :class="project.layout === 'naka' ? 'text-amber-500/70' : 'text-text-muted/55'"
              >
                {{ project.layout === 'cursed' ? 'RESTRICTED ACCESS' : 'READ MORE // LAUNCH' }}
              </span>

              <a
                v-if="project.linkUrl"
                :href="project.linkUrl"
                :target="project.linkUrl !== '#' ? '_blank' : undefined"
                :rel="project.linkUrl !== '#' ? 'noopener noreferrer' : undefined"
                :class="[
                  'inline-flex items-center gap-1.5 text-xs font-semibold transition-colors duration-300 cursor-pointer',
                  project.layout === 'naka'
                    ? 'text-amber-500 in-[.light]:text-amber-700 group-hover:text-accent-white in-[.light]:group-hover:text-accent-white'
                    : 'text-primary group-hover:text-accent-white',
                ]"
              >
                {{ project.linkText }}
              </a>
              <div
                v-else
                class="flex items-center gap-1.5 text-xs font-semibold text-text-muted/50 cursor-not-allowed select-none"
              >
                {{ project.linkText }}
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div
      class="absolute bottom-2 left-[28%] text-primary/25 pointer-events-none select-none animate-pulse-slow hidden md:block"
    >
      <svg class="w-3.5 h-3.5" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
        <circle cx="12" cy="12" r="3.5" fill="currentColor" />
      </svg>
    </div>
  </section>
</template>
