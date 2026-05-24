<script setup>
import { ref, onMounted, onUnmounted } from 'vue'
import NavBar from './components/NavBar.vue'
import HeroSection from './components/HeroSection.vue'
import AboutSection from './components/AboutSection.vue'
import SkillsSection from './components/SkillsSection.vue'
import ProjectsSection from './components/ProjectsSection.vue'
import ContactSection from './components/ContactSection.vue'
import FooterSection from './components/FooterSection.vue'

const mouseX = ref(0)
const mouseY = ref(0)
const cursorX = ref(0)
const cursorY = ref(0)
const isHovering = ref(false)
const isDesktop = ref(false)
let animationFrameId = null

const updateMouse = (e) => {
  mouseX.value = e.clientX
  mouseY.value = e.clientY
}

const checkHover = (e) => {
  const target = e.target
  if (
    target.tagName === 'A' ||
    target.tagName === 'BUTTON' ||
    target.closest('a') ||
    target.closest('button') ||
    target.closest('[class*="group"]') ||
    target.closest('[class*="cursor-pointer"]')
  ) {
    isHovering.value = true
  } else {
    isHovering.value = false
  }
}

const animateCursor = () => {
  // Linear interpolation (lerp) with a smooth 0.16 factor for subtle follow
  cursorX.value += (mouseX.value - cursorX.value) * 0.16
  cursorY.value += (mouseY.value - cursorY.value) * 0.16
  animationFrameId = requestAnimationFrame(animateCursor)
}

onMounted(() => {
  isDesktop.value = window.matchMedia('(pointer: fine)').matches
  if (isDesktop.value) {
    window.addEventListener('mousemove', updateMouse)
    window.addEventListener('mouseover', checkHover)
    // Seeding start coordinates to prevent flash
    mouseX.value = window.innerWidth / 2
    mouseY.value = window.innerHeight / 2
    cursorX.value = mouseX.value
    cursorY.value = mouseY.value
    animateCursor()
  }
})

onUnmounted(() => {
  if (isDesktop.value) {
    window.removeEventListener('mousemove', updateMouse)
    window.removeEventListener('mouseover', checkHover)
    if (animationFrameId !== null) {
      cancelAnimationFrame(animationFrameId)
    }
  }
})
</script>

<template>
  <div
    class="relative bg-background text-accent-white min-h-screen font-sans selection:bg-primary/20 selection:text-accent-white overflow-x-hidden"
  >
    <!-- Global Shared Canvas Layer -->
    <div class="fixed inset-0 z-0 pointer-events-none select-none overflow-hidden bg-background">
      <!-- Global Grid Background -->
      <div class="absolute inset-0 opacity-[0.05] dark:opacity-[0.022] text-primary">
        <svg width="100%" height="100%" xmlns="http://www.w3.org/2000/svg">
          <defs>
            <pattern id="global-grid-lines" width="55" height="55" patternUnits="userSpaceOnUse">
              <path d="M 55 0 L 0 0 0 55" fill="none" stroke="currentColor" stroke-width="0.75" />
            </pattern>
          </defs>
          <rect width="100%" height="100%" fill="url(#global-grid-lines)" />
        </svg>
      </div>

      <!-- Global Grain Overlay -->
      <svg
        class="absolute inset-0 w-full h-full opacity-[0.015] dark:opacity-[0.007] pointer-events-none z-0"
        xmlns="http://www.w3.org/2000/svg"
      >
        <defs>
          <filter id="globalGrainyNoise">
            <feTurbulence
              type="fractalNoise"
              baseFrequency="0.75"
              numOctaves="3"
              stitchTiles="stitch"
            />
          </filter>
        </defs>
        <rect width="100%" height="100%" filter="url(#globalGrainyNoise)" />
      </svg>
    </div>

    <!-- Cinematic Subtle Mouse Cursor (Desktop Only) -->
    <div
      v-if="isDesktop"
      class="custom-cursor"
      :class="{ 'custom-cursor-hover': isHovering }"
      :style="{ left: `${cursorX}px`, top: `${cursorY}px` }"
    ></div>

    <NavBar />
    <HeroSection />
    <AboutSection />
    <SkillsSection />
    <ProjectsSection />
    <ContactSection />
    <FooterSection />
  </div>
</template>
