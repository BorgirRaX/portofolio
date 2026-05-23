<script setup lang="ts">
import { ref, onMounted } from 'vue'

const isVisible = ref(false)
const skillsSection = ref<HTMLElement | null>(null)

const activeSkills = [
  "HTML",
  "CSS",
  "JavaScript",
  "Vue 3",
  "Tailwind CSS",
  "Git",
  "Python"
]

const learningSkills = [
  "Solidity",
  "ethers.js",
  "Smart Contract UI",
  "Web3 UX"
]

onMounted(() => {
  const observer = new IntersectionObserver(
    (entries) => {
      if (entries[0].isIntersecting) {
        isVisible.value = true
        observer.disconnect()
      }
    },
    { threshold: 0.1 }
  )
  if (skillsSection.value) {
    observer.observe(skillsSection.value)
  }
})
</script>

<template>
  <section
    id="skills"
    ref="skillsSection"
    class="py-24 md:py-32 bg-background border-t border-soft-navy/40 relative overflow-hidden"
  >
    <div class="max-w-4xl mx-auto px-6 relative z-10">
      <!-- Section Title -->
      <div class="text-left mb-16">
        <span class="font-mono text-xs font-semibold tracking-widest text-primary uppercase mb-3 block">
          // SKILLS
        </span>
        <h2 class="font-display font-bold text-2xl md:text-3xl text-accent-white">
          Things I build with<span class="text-primary">.</span>
        </h2>
      </div>

      <!-- Main Columns (2 Columns) -->
      <div class="grid grid-cols-1 md:grid-cols-2 gap-12 md:gap-16">
        <!-- Left Column: Building With -->
        <div class="flex flex-col items-start">
          <h3 class="font-display font-semibold text-base text-accent-white mb-3 tracking-wide uppercase">
            Building With
          </h3>
          <div class="w-10 h-0.5 bg-primary/40 mb-6"></div>

          <div class="flex flex-wrap gap-2.5">
            <div
              v-for="(skill, index) in activeSkills"
              :key="skill"
              :style="{ transitionDelay: `${index * 40}ms` }"
              :class="[
                'transition-all duration-700 transform',
                isVisible ? 'opacity-100 translate-y-0 scale-100' : 'opacity-0 translate-y-3 scale-95'
              ]"
            >
              <div class="px-4 py-2 border border-soft-navy rounded-xl text-accent-white font-mono text-xs uppercase tracking-wider bg-card/10 hover:border-primary/50 transition-colors duration-300">
                {{ skill }}
              </div>
            </div>
          </div>
        </div>

        <!-- Right Column: Learning -->
        <div class="flex flex-col items-start">
          <h3 class="font-display font-semibold text-base text-text-muted mb-3 tracking-wide uppercase">
            Learning
          </h3>
          <div class="w-10 h-0.5 bg-soft-navy mb-6"></div>

          <div class="flex flex-wrap gap-2.5">
            <div
              v-for="(skill, index) in learningSkills"
              :key="skill"
              :style="{ transitionDelay: `${(index + activeSkills.length) * 40}ms` }"
              :class="[
                'transition-all duration-700 transform',
                isVisible ? 'opacity-100 translate-y-0 scale-100' : 'opacity-0 translate-y-3 scale-95'
              ]"
            >
              <div class="px-4 py-2 border border-dashed border-soft-navy/80 rounded-xl text-text-muted font-mono text-xs uppercase tracking-wider bg-card/5 hover:border-primary/30 transition-colors duration-300">
                {{ skill }}
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
