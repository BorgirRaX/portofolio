<script setup lang="ts">
import { ref, onMounted, onUnmounted } from 'vue'

const scrolled = ref(false)
const mobileMenuOpen = ref(false)
const isLight = ref(false)

const handleScroll = () => {
  scrolled.value = window.scrollY > 20
}

const toggleTheme = () => {
  isLight.value = !isLight.value
  if (isLight.value) {
    document.documentElement.classList.add('light')
    localStorage.setItem('theme', 'light')
  } else {
    document.documentElement.classList.remove('light')
    localStorage.setItem('theme', 'dark')
  }
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
  const savedTheme = localStorage.getItem('theme')
  if (savedTheme === 'dark') {
    isLight.value = false
    document.documentElement.classList.remove('light')
  } else {
    isLight.value = true
    document.documentElement.classList.add('light')
  }
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>

<template>
  <header
    :class="[
      'fixed top-0 left-0 right-0 z-50 transition-all duration-500 border-b border-transparent',
      scrolled
        ? 'bg-background/70 backdrop-blur-md py-3.5 border-soft-navy'
        : 'bg-transparent py-5',
    ]"
  >
    <div class="max-w-5xl mx-auto px-6 flex justify-between items-center">
      <!-- Logo -->
      <a
        href="#"
        class="font-display font-bold text-base text-primary tracking-tight hover:opacity-85 transition-opacity"
      >
        jimy<span class="text-accent-white">.</span>
      </a>

      <!-- Desktop Links -->
      <nav class="hidden md:flex items-center gap-7">
        <a
          href="#about"
          class="font-sans font-medium text-[13px] text-text-muted hover:text-accent-white tracking-wide transition-colors py-2"
        >
          About
        </a>
        <a
          href="#skills"
          class="font-sans font-medium text-[13px] text-text-muted hover:text-accent-white tracking-wide transition-colors py-2"
        >
          Skills
        </a>
        <a
          href="#projects"
          class="font-sans font-medium text-[13px] text-text-muted hover:text-accent-white tracking-wide transition-colors py-2"
        >
          Projects
        </a>
        <a
          href="#contact"
          class="font-sans font-medium text-[13px] text-text-muted hover:text-accent-white tracking-wide transition-colors py-2"
        >
          Contact
        </a>
      </nav>

      <!-- Action Buttons -->
      <div class="flex items-center gap-3">
        <!-- Theme Toggle -->
        <button
          @click="toggleTheme"
          class="p-2 rounded-lg border border-soft-navy hover:border-primary/50 bg-card/20 hover:bg-card/60 transition-all duration-300 cursor-pointer text-text-muted hover:text-accent-white"
          aria-label="Toggle Theme"
        >

          <svg
            v-if="!isLight"
            xmlns="http://www.w3.org/2000/svg"
            class="w-4 h-4"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="2"
          >
            <circle cx="12" cy="12" r="4" />
            <path
              d="M12 2v2M12 20v2M4.93 4.93l1.41 1.41M17.66 17.66l1.41 1.41M2 12h2M20 12h2M6.34 17.66l-1.41 1.41M19.07 4.93l-1.41 1.41"
            />
          </svg>
          <svg
            v-else
            xmlns="http://www.w3.org/2000/svg"
            class="w-4 h-4"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="2"
          >
            <path d="M12 3a6.36 6.36 0 0 0 9 9 9 9 0 1 1-9-9Z" />
          </svg>
        </button>

        <button
          @click="mobileMenuOpen = !mobileMenuOpen"
          class="md:hidden p-2 rounded-lg border border-soft-navy text-text-muted hover:text-accent-white bg-card/20 transition-colors"
          aria-label="Toggle Mobile Menu"
        >
          <svg
            v-if="!mobileMenuOpen"
            xmlns="http://www.w3.org/2000/svg"
            class="w-4 h-4"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
            stroke-width="2"
          >
            <line x1="4" x2="20" y1="12" y2="12" />
            <line x1="4" x2="20" y1="6" y2="6" />
            <line x1="4" x2="20" y1="18" y2="18" />
          </svg>
          <svg
            v-else
            xmlns="http://www.w3.org/2000/svg"
            class="w-4 h-4"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
            stroke-width="2"
          >
            <line x1="18" x2="6" y1="6" y2="18" />
            <line x1="6" x2="18" y1="6" y2="18" />
          </svg>
        </button>
      </div>
    </div>

    <div
      v-if="mobileMenuOpen"
      class="md:hidden absolute top-full left-0 right-0 bg-background/95 border-b border-soft-navy py-5 px-8 flex flex-col gap-3.5 backdrop-blur-md transition-all duration-300 ease-in-out"
    >
      <a
        href="#about"
        @click="mobileMenuOpen = false"
        class="font-sans font-medium text-[13px] text-text-muted hover:text-accent-white transition-colors py-2"
      >
        About
      </a>
      <a
        href="#skills"
        @click="mobileMenuOpen = false"
        class="font-sans font-medium text-[13px] text-text-muted hover:text-accent-white transition-colors py-2"
      >
        Skills
      </a>
      <a
        href="#projects"
        @click="mobileMenuOpen = false"
        class="font-sans font-medium text-[13px] text-text-muted hover:text-accent-white transition-colors py-2"
      >
        Projects
      </a>
      <a
        href="#contact"
        @click="mobileMenuOpen = false"
        class="font-sans font-medium text-[13px] text-text-muted hover:text-accent-white transition-colors py-2"
      >
        Contact
      </a>
    </div>
  </header>
</template>
