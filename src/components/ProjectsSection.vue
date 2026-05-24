<script setup>
import { ref } from 'vue'

const hoveredProject = ref(null)

const projects = [
  {
    id: 1,
    name: "Naka Coffee",
    desc: "Landing page untuk coffee shop di Semarang dengan pendekatan emotional branding dan clean storytelling.",
    tech: "HTML · CSS · JavaScript",
    linkText: "Kunjungi Situs",
    linkUrl: "#",
    colSpan: "md:col-span-1",
    theme: "from-primary/3 to-transparent",
    glowColor: "rgba(74, 158, 204, 0.03)", // Reduced futuristic glow
    borderHover: "hover:border-primary/30"
  },
  {
    id: 2,
    name: "Personal Portfolio",
    desc: "Cinematic portfolio dengan fokus pada interaksi frontend, tipografi tebal, dan ritme visual yang kuat.",
    tech: "Vue 3 · Tailwind · Vite",
    linkText: "Kunjungi Situs",
    linkUrl: "#",
    colSpan: "md:col-span-2",
    theme: "from-primary/3 to-transparent",
    glowColor: "rgba(74, 158, 204, 0.03)", // Reduced futuristic glow
    borderHover: "hover:border-primary/30"
  },
  {
    id: 3,
    name: "Odin Recipes",
    desc: "Proyek awal untuk memahami semantik dasar dokumen HTML dan tata letak struktur halaman web sederhana.",
    tech: "HTML · CSS",
    linkText: "Lihat Repositori",
    linkUrl: "#",
    colSpan: "md:col-span-3",
    theme: "from-primary/3 to-transparent",
    glowColor: "rgba(74, 158, 204, 0.03)", // Reduced futuristic glow
    borderHover: "hover:border-primary/30"
  }
]
</script>

<template>
  <section id="projects" class="py-24 md:py-32 bg-background relative">
    <!-- SVG Analog Noise / Grain Overlay -->
    <svg class="absolute inset-0 w-full h-full opacity-[0.012] pointer-events-none z-0" xmlns="http://www.w3.org/2000/svg">
      <filter id="grainyNoiseProjects">
        <feTurbulence type="fractalNoise" baseFrequency="0.75" numOctaves="3" stitchTiles="stitch" />
      </filter>
      <rect width="100%" height="100%" filter="url(#grainyNoiseProjects)" />
    </svg>

    <!-- Faded and reduced opacity Grid Background -->
    <div class="absolute inset-0 z-0 opacity-[0.08] pointer-events-none">
      <svg width="100%" height="100%" xmlns="http://www.w3.org/2000/svg">
        <pattern id="grid-large-subtle" width="120" height="120" patternUnits="userSpaceOnUse">
          <line x1="0" y1="0" x2="120" y2="0" stroke="#4a9ecc" stroke-width="0.35" />
          <line x1="0" y1="0" x2="0" y2="120" stroke="#4a9ecc" stroke-width="0.35" />
        </pattern>
        <rect width="100%" height="100%" fill="url(#grid-large-subtle)" />
      </svg>
    </div>

    <div class="max-w-5xl mx-auto px-6 relative z-10">
      <!-- Section Header -->
      <div class="mb-16 text-left max-w-xl">
        <span class="font-mono text-xs font-semibold tracking-widest text-primary uppercase mb-3 block">
          // SELECTED PROJECTS
        </span>
        <h2 class="font-display font-bold text-2xl md:text-3xl text-accent-white mb-4">
          Selected Projects<span class="text-primary">.</span>
        </h2>
        <p class="font-sans text-sm text-text-muted leading-relaxed font-light">
          A few things I've designed, built, and occasionally debugged at 2AM.
        </p>
      </div>

      <!-- Bento Grid with micro-rotations and playful stickers -->
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <div
          v-for="project in projects"
          :key="project.id"
          :class="[
            'relative rounded-3xl border border-soft-navy bg-card/40 overflow-hidden flex flex-col justify-between p-8 md:p-10 group transition-all duration-700 hover:-translate-y-1',
            project.colSpan,
            project.borderHover,
            project.id % 2 === 0 ? 'hover:rotate-[0.5deg]' : 'hover:-rotate-[0.5deg]'
          ]"
          @mouseenter="hoveredProject = project.id"
          @mouseleave="hoveredProject = null"
          :style="hoveredProject === project.id ? { boxShadow: `0 8px 30px ${project.glowColor}` } : {}"
        >
          <!-- Custom Personality Stickers -->
          <!-- Naka Coffee Sticker -->
          <div v-if="project.id === 1" class="absolute -right-2 -top-2.5 z-20 inline-flex items-center gap-1 px-2.5 py-0.5 bg-card/60 border border-text-muted/15 rounded-md shadow-sm backdrop-blur-[2px] rotate-6 select-none pointer-events-none transition-transform duration-500 group-hover:rotate-0">
            <span class="font-mono text-[8px] font-medium text-text-muted/80 tracking-wide">currently caffeinated ☕</span>
          </div>

          <!-- Personal Portfolio Sticker -->
          <div v-if="project.id === 2" class="absolute right-4 -top-2.5 z-20 inline-flex items-center gap-1 px-2.5 py-0.5 bg-card/60 border border-text-muted/15 rounded-md shadow-sm backdrop-blur-[2px] -rotate-3 select-none pointer-events-none transition-transform duration-500 group-hover:rotate-0">
            <span class="font-mono text-[8px] font-medium text-text-muted/80 tracking-wide">built between coffee cups & confusion ⚡</span>
          </div>

          <!-- Odin Recipes Sticker -->
          <div v-if="project.id === 3" class="absolute right-6 -top-2.5 z-20 inline-flex items-center gap-1 px-2.5 py-0.5 bg-card/60 border border-text-muted/15 rounded-md shadow-sm backdrop-blur-[2px] rotate-2 select-none pointer-events-none transition-transform duration-500 group-hover:rotate-0">
            <span class="font-mono text-[8px] font-medium text-text-muted/80 tracking-wide">panenan bisa nunggu 🌱</span>
          </div>

          <!-- Subtle gradient overlay on hover -->
          <div :class="['absolute inset-0 bg-gradient-to-br opacity-0 group-hover:opacity-100 transition-opacity duration-500 pointer-events-none', project.theme]"></div>

          <!-- Upper Content -->
          <div class="relative z-10">
            <!-- Project Header -->
            <div class="flex justify-between items-start mb-6">
              <span class="font-mono text-[9px] text-text-muted tracking-widest uppercase">// PROYEK #0{{ project.id }}</span>
              <span class="font-mono text-[9px] text-text-muted uppercase tracking-wider px-2.5 py-0.5 border border-soft-navy bg-background/60 rounded-full">
                {{ project.tech }}
              </span>
            </div>

            <!-- Title & Description -->
            <h3 class="font-display font-bold text-lg md:text-xl text-accent-white tracking-tight group-hover:text-primary transition-colors duration-450 mb-3">
              {{ project.name }}
            </h3>
            <p class="font-sans text-[13px] sm:text-sm text-text-muted leading-[1.7] font-light mb-8 max-w-[56ch]">
              {{ project.desc }}
            </p>
          </div>

          <!-- Graphic Mockups Styled to Look Hand-Sketched / Imperfect -->
          <div class="relative z-10 w-full h-36 flex items-center justify-center mb-8 overflow-hidden rounded-2xl border border-soft-navy/40 bg-dark-navy/60 p-4">
            
            <!-- Naka Coffee Graphic (ID: 1) -->
            <svg v-if="project.id === 1" viewBox="0 0 200 100" fill="none" class="w-48 h-full opacity-55 group-hover:opacity-85 transition-opacity duration-500">
              <circle cx="100" cy="50" r="28" stroke="#4a9ecc" stroke-width="1" stroke-dasharray="3 3" />
              <!-- Sketch-style Circle -->
              <path d="M100,26 C114,26 126,38 126,50 C126,62 114,74 100,74 C86,74 74,62 74,50 C74,38 86,26 100,26 Z" stroke="#4a9ecc" stroke-width="1.3" stroke-linecap="round" stroke-linejoin="round" />
              <!-- Coffee Cup outline -->
              <path d="M91,44 L109,44 L109,55 C109,59 105,62 100,62 C95,62 91,59 91,55 Z" fill="none" stroke="#d4eeff" stroke-width="1.3" stroke-linecap="round" />
              <path d="M109,47 C113,47 114,51 109,52" fill="none" stroke="#d4eeff" stroke-width="1.3" stroke-linecap="round" />
              <!-- Heat wave sketches -->
              <path d="M96,38 C97,35 95,34 96,32" stroke="#d4eeff" stroke-width="0.8" stroke-linecap="round" />
              <path d="M100,37 C101,34 99,33 100,31" stroke="#d4eeff" stroke-width="0.8" stroke-linecap="round" />
            </svg>

            <!-- Personal Portfolio Graphic (ID: 2) -->
            <svg v-else-if="project.id === 2" viewBox="0 0 200 100" fill="none" class="w-full h-full opacity-55 group-hover:opacity-85 transition-opacity duration-500">
              <!-- Hand-drawn styled window shell -->
              <path d="M26,22 C50,20 150,19 174,21 C176,28 175,72 174,79 C150,81 50,80 26,79 C24,72 25,28 26,22 Z" fill="#0A0F18" stroke="#4a9ecc" stroke-width="1.2" stroke-linecap="round" stroke-linejoin="round" />
              <!-- Control Dots -->
              <circle cx="36" cy="31" r="2" fill="#4a9ecc" />
              <circle cx="44" cy="31" r="2" fill="#152232" />
              <circle cx="52" cy="31" r="2" fill="#152232" />
              <!-- Divider line -->
              <path d="M26,38 C50,38 150,38 174,38" stroke="#152232" stroke-width="1.2" stroke-linecap="round" />
              <!-- Hand-drawn layout rectangles -->
              <path d="M37,47 C48,46 68,46 76,47 C77,51 76,59 76,63 C65,64 48,64 37,63 C36,59 36,51 37,47 Z" fill="#152232" />
              <path d="M88,49 C110,48 140,48 160,49" stroke="#152232" stroke-width="1.2" stroke-linecap="round" />
              <path d="M88,57 C105,56 130,56 145,57" stroke="#152232" stroke-width="1.2" stroke-linecap="round" />
              <path d="M88,65 C100,64 115,64 125,65" stroke="#4a9ecc" stroke-width="1.2" stroke-linecap="round" />
            </svg>

            <!-- Odin Recipes Graphic (ID: 3) -->
            <svg v-else-if="project.id === 3" viewBox="0 0 200 100" fill="none" class="w-full h-full opacity-55 group-hover:opacity-85 transition-opacity duration-500">
              <!-- Hand-drawn plate container -->
              <path d="M42,22 C70,20 130,20 158,22 C160,35 160,65 158,78 C130,80 70,80 42,78 C40,65 40,35 42,22 Z" fill="#0A0F18" stroke="#4a9ecc" stroke-width="1.2" stroke-linecap="round" stroke-linejoin="round" />
              <path d="M65,34 C74,34 81,41 81,50 C81,59 74,66 65,66 C56,66 49,59 49,50 C49,41 56,34 65,34 Z" stroke="#152232" stroke-width="1.2" stroke-linecap="round" />
              <!-- Hand-drawn Fork/Spoon elements -->
              <path d="M60,42 L60,58" stroke="#d4eeff" stroke-width="1.5" stroke-linecap="round" />
              <path d="M57,42 L63,42 M57,46 L63,46" stroke="#d4eeff" stroke-width="0.8" />
              <path d="M70,42 L70,58" stroke="#d4eeff" stroke-width="1.5" stroke-linecap="round" />
              <path d="M67,42 C67,39 73,39 73,42 Z" fill="#d4eeff" />
              <!-- Text lines -->
              <path d="M96,38 L146,38" stroke="#152232" stroke-width="1.2" stroke-linecap="round" />
              <path d="M96,48 L146,48" stroke="#152232" stroke-width="1.2" stroke-linecap="round" />
              <path d="M96,58 L126,58" stroke="#4a9ecc" stroke-width="1.2" stroke-linecap="round" />
            </svg>
          </div>

          <!-- Card Footer Links -->
          <div class="relative z-10 mt-auto flex items-center justify-between border-t border-soft-navy/40 pt-5">
            <span class="font-mono text-[9px] text-text-muted tracking-widest uppercase">READ MORE // LAUNCH</span>
            <a
              :href="project.linkUrl"
              class="inline-flex items-center gap-1.5 text-xs font-semibold text-primary group-hover:text-accent-white transition-colors duration-300 cursor-pointer"
            >
              {{ project.linkText }}
              <svg xmlns="http://www.w3.org/2000/svg" class="w-4 h-4 transform group-hover:translate-x-1 transition-transform duration-300" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
                <path stroke-linecap="round" stroke-linejoin="round" d="M14 5l7 7m0 0l-7 7m7-7H3" />
              </svg>
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
