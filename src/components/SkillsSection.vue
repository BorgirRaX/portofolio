<script setup>
import { ref, onMounted } from 'vue'

const isVisible = ref(false)
const skillsSection = ref(null)

const activeSkills = [
  {
    name: 'HTML',
    url: 'https://developer.mozilla.org/en-US/docs/Web/HTML',
    desc: 'Semantic markup & high-fidelity SEO anchors.',
    icon: 'html',
  },
  {
    name: 'CSS',
    url: 'https://developer.mozilla.org/en-US/docs/Web/CSS',
    desc: 'Flexbox, Grid, & writing absolute dark magic.',
    icon: 'css',
  },
  {
    name: 'JavaScript',
    url: 'https://developer.mozilla.org/en-US/docs/Web/JavaScript',
    desc: 'Asynchronous callbacks & modern ES6+ suffering.',
    icon: 'js',
  },
  {
    name: 'Vue 3',
    url: 'https://vuejs.org/',
    desc: 'Composition API, custom directives, & ref() spam.',
    icon: 'vue',
  },
  {
    name: 'Tailwind CSS',
    url: 'https://tailwindcss.com/',
    desc: 'Aesthetic utility classes & hyper-speed styling.',
    icon: 'tailwind',
  },
  {
    name: 'Git',
    url: 'https://git-scm.com/',
    desc: 'Rebasing, branching, & merge conflict panic.',
    icon: 'git',
  },
  {
    name: 'Python',
    url: 'https://docs.python.org/3/',
    desc: 'Quick automation scripts & data parsing wizardry.',
    icon: 'python',
  },
]

const learningSkills = [
  {
    name: 'Solidity',
    url: 'https://docs.soliditylang.org/',
    desc: 'Smart contract development & gas optimization hacks.',
    icon: 'solidity',
  },
  {
    name: 'Ethers.js',
    url: 'https://docs.ethers.org/v6/',
    desc: 'Plumbing the browser frontend straight to the blockchain.',
    icon: 'ethers',
  },
  {
    name: 'Smart Contract UI',
    url: 'https://ethereum.org/en/developers/docs/dapps/',
    desc: 'Syncing volatile contract states with RPC network latency.',
    icon: 'contract',
  },
  {
    name: 'Web3 UX',
    url: 'https://ethereum.org/en/developers/docs/web3-ux/',
    desc: 'Designing transactions to save users gas fees & sanity.',
    icon: 'web3ux',
  },
]

onMounted(() => {
  const observer = new IntersectionObserver(
    (entries) => {
      if (entries[0].isIntersecting) {
        isVisible.value = true
        observer.disconnect()
      }
    },
    { threshold: 0.1 },
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
    class="pt-10 pb-20 md:pt-12 md:pb-28 bg-transparent relative"
  >
    <div
      class="absolute -top-[250px] -bottom-[80px] left-0 right-0 pointer-events-none z-0 opacity-50 dark:opacity-20 text-primary/70"
      style="
        background-image: radial-gradient(currentColor 1.5px, transparent 1.5px);
        background-size: 28px 28px;
        mask-image: radial-gradient(ellipse at 50% 45%, black 0%, rgba(0,0,0,0.85) 40%, transparent 70%);
        -webkit-mask-image: radial-gradient(ellipse at 50% 45%, black 0%, rgba(0,0,0,0.85) 40%, transparent 70%);
      "
    ></div>
    <div
      class="absolute -top-[150px] left-1/2 -translate-x-1/2 w-[550px] h-[300px] rounded-full bg-primary/4 dark:bg-primary/2 blur-[120px] pointer-events-none z-0"
    ></div>
    <div class="absolute top-2 right-[22%] text-primary/35 pointer-events-none select-none rotate-15 hidden md:block">
      <span class="font-handwritten text-xs text-text-muted/70 tracking-wider">drift... ✨</span>
    </div>
    <div class="max-w-4xl mx-auto px-6 relative z-20">
      <div class="text-left mb-12 relative">
        <svg
          class="absolute -right-2 -top-6 w-9 h-9 text-primary/30 hidden md:block select-none pointer-events-none animate-pulse-slow"
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

        <span
          class="font-mono text-xs font-semibold tracking-widest text-primary uppercase mb-3 block"
        >
          // SKILLS
        </span>
        <h2
          class="font-display font-extrabold text-2xl md:text-3xl lg:text-4xl text-accent-white leading-[1.1] tracking-tight"
        >
          THINGS I USE TO<br />
          <span class="relative inline-block text-primary">
            MAKE WEIRD STUFF.
            <span
              class="absolute left-0 -bottom-2 w-full h-[4.5px] bg-primary/45 rounded-full"
            ></span>
            <span
              class="absolute left-1.5 -bottom-4 w-[95%] h-[2px] bg-primary/25 rounded-full"
            ></span>
          </span>
        </h2>
      </div>

      <div
        class="grid grid-cols-1 md:grid-cols-2 gap-10 md:gap-14 items-start relative pb-12 lg:pb-16"
      >
        <!-- Left Column: Building With -->
        <div class="flex flex-col items-start w-full">
          <span
            class="font-mono text-[10px] font-bold text-primary tracking-widest uppercase mb-4 flex items-center gap-1.5"
          >
            <span class="w-1.5 h-1.5 rounded-full bg-primary animate-pulse"></span>
            CURRENTLY BUILDING WITH
          </span>

          <div class="flex flex-wrap gap-2.5 w-full">
            <div
              v-for="(skill, index) in activeSkills"
              :key="skill.name"
              :style="{ transitionDelay: `${index * 50}ms` }"
              :class="[
                'transition-all duration-700 transform',
                isVisible
                  ? 'opacity-100 translate-y-0 scale-100'
                  : 'opacity-0 translate-y-4 scale-95',
              ]"
            >
              <a
                :href="skill.url"
                target="_blank"
                rel="noopener noreferrer"
                class="group relative flex items-center gap-2 px-4 py-2.5 rounded-xl border border-soft-navy bg-card/45 hover:bg-soft-navy/30 hover:border-primary/50 text-accent-white hover:text-primary transition-all duration-300 font-mono text-xs uppercase tracking-wider cursor-pointer shadow-sm hover:shadow-[0_0_15px_rgba(74,158,204,0.15)] hover:-translate-y-1 active:scale-95"
              >
                <span
                  class="flex items-center justify-center w-4 h-4 text-text-muted group-hover:text-primary transition-colors duration-300"
                >
                  <!-- HTML Icon -->
                  <svg
                    v-if="skill.icon === 'html'"
                    class="w-4 h-4"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                    stroke-width="2.5"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      d="M17.25 6.75L22.5 12l-5.25 5.25m-10.5 0L1.5 12l5.25-5.25m7.5-3l-4.5 16.5"
                    />
                  </svg>
                  <!-- CSS Icon -->
                  <svg
                    v-else-if="skill.icon === 'css'"
                    class="w-4 h-4"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                    stroke-width="2.5"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      d="M9.53 16.122l9.37-9.37a2.25 2.25 0 113.182 3.182l-9.372 9.372a4.5 4.5 0 01-1.636 1.055l-3.093 1.031 1.031-3.093a4.5 4.5 0 011.056-1.636z"
                    />
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      d="M18.01 4.975a2.25 2.25 0 113.181 3.183M15.5 8.5l3.5 3.5"
                    />
                  </svg>
                  <!-- JavaScript Icon -->
                  <svg
                    v-else-if="skill.icon === 'js'"
                    class="w-4 h-4"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                    stroke-width="2.5"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      d="M14.25 9.75L16.5 12l-2.25 2.25m-4.5 0L7.5 12l2.25-2.25M6 20.25h12A2.25 2.25 0 0020.25 18V6A2.25 2.25 0 0018 3.75H6A2.25 2.25 0 003.75 6v12A2.25 2.25 0 006 20.25z"
                    />
                  </svg>
                  <!-- Vue 3 Icon -->
                  <svg
                    v-else-if="skill.icon === 'vue'"
                    class="w-4 h-4"
                    viewBox="0 0 24 24"
                    fill="currentColor"
                  >
                    <path d="M24 2.5h-4.5L12 15 4.5 2.5H0L12 22.5 24 2.5z" />
                    <path d="M16.5 2.5H12l-4.5 7.5L3 2.5H0L12 20.5 24 2.5z" opacity="0.65" />
                  </svg>
                  <!-- Tailwind Icon -->
                  <svg
                    v-else-if="skill.icon === 'tailwind'"
                    class="w-4 h-4"
                    viewBox="0 0 24 24"
                    fill="currentColor"
                  >
                    <path
                      d="M12.001,4.8c-3.2,0-5.2,1.6-6,4.8c1.2-1.6,2.6-2.2,4.2-1.8c0.913,0.228,1.565,0.89,2.288,1.624 C13.666,10.618,15.027,12,18.001,12c3.2,0,5.2-1.6,6-4.8c-1.2,1.6-2.6,2.2-4.2,1.8c-0.913-0.228-1.565-0.89-2.288-1.624 C16.336,6.182,14.976,4.8,12.001,4.8z M6.001,12c-3.2,0-5.2,1.6-6,4.8c1.2-1.6,2.6-2.2,4.2-1.8c0.913,0.228,1.565,0.89,2.288,1.624 c1.177,1.194,2.538,2.576,5.512,2.576c3.2,0,5.2-1.6,6-4.8c-1.2,1.6-2.6,2.2-4.2,1.8c-0.913-0.228-1.565-0.89-2.288-1.624 C10.336,13.382,8.976,12,6.001,12z"
                    />
                  </svg>
                  <!-- Git Icon -->
                  <svg
                    v-else-if="skill.icon === 'git'"
                    class="w-4 h-4"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                    stroke-width="2.5"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      d="M18 15a3 3 0 100-6 3 3 0 000 6zm-12-6a3 3 0 100-6 3 3 0 000 6zm0 6v-6m0 6a3 3 0 100 6 3 3 0 000-6zm0-6h6a3 3 0 013 3v0"
                    />
                  </svg>
                  <!-- Python Icon -->
                  <svg
                    v-else-if="skill.icon === 'python'"
                    class="w-4 h-4"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                    stroke-width="2.5"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      d="M19.5 14.25v-2.625a3.375 3.375 0 00-3.375-3.375h-1.5A1.125 1.125 0 0113.5 7.125v-1.5a3.375 3.375 0 00-3.375-3.375H8.25m0 12.75h7.5m-7.5 3H12"
                    />
                  </svg>
                </span>

                <span>{{ skill.name }}</span>
                <div
                  class="absolute bottom-full left-1/2 -translate-x-1/2 mb-2.5 px-3 py-2 bg-dark-navy border border-soft-navy text-accent-white rounded-xl shadow-2xl opacity-0 scale-95 translate-y-1 pointer-events-none group-hover:opacity-100 group-hover:scale-100 group-hover:translate-y-0 transition-all duration-300 z-50 whitespace-nowrap flex flex-col items-center"
                >
                  <span
                    class="font-mono text-[9px] text-primary font-bold uppercase tracking-wider flex items-center gap-1"
                  >
                    open docs
                    <svg
                      class="w-2 h-2"
                      fill="none"
                      viewBox="0 0 24 24"
                      stroke="currentColor"
                      stroke-width="3"
                    >
                      <path
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        d="M4.5 19.5l15-15m0 0H8.25m11.25 0v11.25"
                      />
                    </svg>
                  </span>
                  <span
                    class="font-sans text-[10px] text-ice-blue/80 mt-0.5 max-w-[170px] text-center leading-tight normal-case font-normal whitespace-normal"
                  >
                    {{ skill.desc }}
                  </span>
                  <div
                    class="absolute top-full left-1/2 -translate-x-1/2 w-2 h-2 bg-dark-navy border-r border-b border-soft-navy rotate-45 -mt-[5px]"
                  ></div>
                </div>
              </a>
            </div>
          </div>
        </div>

        <!-- Right Column: Current Obsessions / Currently Learning -->
        <div class="flex flex-col items-start w-full">
          <span
            class="font-mono text-[10px] font-bold text-text-muted tracking-widest uppercase mb-4 flex items-center gap-1.5"
          >
            <span class="w-1.5 h-1.5 rounded-full bg-text-muted animate-pulse"></span>
            CURRENT OBSESSIONS
          </span>

          <div class="flex flex-wrap gap-2.5 w-full">
            <div
              v-for="(skill, index) in learningSkills"
              :key="skill.name"
              :style="{ transitionDelay: `${(index + activeSkills.length) * 50}ms` }"
              :class="[
                'transition-all duration-700 transform',
                isVisible
                  ? 'opacity-100 translate-y-0 scale-100'
                  : 'opacity-0 translate-y-4 scale-95',
              ]"
            >
              <a
                :href="skill.url"
                target="_blank"
                rel="noopener noreferrer"
                class="group relative flex items-center gap-2 px-4 py-2.5 rounded-xl border border-transparent custom-dashed bg-card/20 hover:bg-soft-navy/20 hover:border-primary/40 hover:border-solid text-accent-white hover:text-primary transition-all duration-300 font-mono text-xs uppercase tracking-wider cursor-pointer shadow-sm hover:shadow-[0_0_15px_rgba(74,158,204,0.12)] hover:-translate-y-1 active:scale-95"
              >
                <span
                  class="flex items-center justify-center w-4 h-4 text-text-muted group-hover:text-primary transition-colors duration-300"
                >
                  <!-- Solidity Icon -->
                  <svg
                    v-if="skill.icon === 'solidity'"
                    class="w-4 h-4"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                    stroke-width="2.5"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      d="M12 2L3 12l9 10 9-10L12 2zm0 4.5l5.5 5.5-5.5 5.5-5.5-5.5 5.5-5.5z"
                    />
                  </svg>
                  <!-- Ethers.js Icon -->
                  <svg
                    v-else-if="skill.icon === 'ethers'"
                    class="w-4 h-4"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                    stroke-width="2.5"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      d="M12 21.75l-7.5-4.5 7.5-10.5 7.5 10.5-7.5 4.5zm0-20.25v5.25m0 5.25v5.25M4.5 12h15"
                    />
                  </svg>
                  <!-- Smart Contract UI Icon -->
                  <svg
                    v-else-if="skill.icon === 'contract'"
                    class="w-4 h-4"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                    stroke-width="2.5"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z"
                    />
                  </svg>
                  <!-- Web3 UX Icon -->
                  <svg
                    v-else-if="skill.icon === 'web3ux'"
                    class="w-4 h-4"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                    stroke-width="2.5"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      d="M9.813 15.904L9 21l-.813-5.096L3 15l5.096-.813L9 9l.813 5.096L15 15l-5.187.904zM18 5.25L17 8l-1-2.75L13.25 5 16 4l1-2.75L18 4l2.75 1L18 5.25z"
                    />
                  </svg>
                </span>

                <span>{{ skill.name }}</span>
                <div
                  class="absolute bottom-full left-1/2 -translate-x-1/2 mb-2.5 px-3 py-2 bg-dark-navy border border-soft-navy text-accent-white rounded-xl shadow-2xl opacity-0 scale-95 translate-y-1 pointer-events-none group-hover:opacity-100 group-hover:scale-100 group-hover:translate-y-0 transition-all duration-300 z-50 whitespace-nowrap flex flex-col items-center"
                >
                  <span
                    class="font-mono text-[9px] text-primary font-bold uppercase tracking-wider flex items-center gap-1"
                  >
                    open docs
                    <svg
                      class="w-2 h-2"
                      fill="none"
                      viewBox="0 0 24 24"
                      stroke="currentColor"
                      stroke-width="3"
                    >
                      <path
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        d="M4.5 19.5l15-15m0 0H8.25m11.25 0v11.25"
                      />
                    </svg>
                  </span>
                  <span
                    class="font-sans text-[10px] text-ice-blue/80 mt-0.5 max-w-[170px] text-center leading-tight normal-case font-normal whitespace-normal"
                  >
                    {{ skill.desc }}
                  </span>
                  <div
                    class="absolute top-full left-1/2 -translate-x-1/2 w-2 h-2 bg-dark-navy border-r border-b border-soft-navy rotate-45 -mt-[5px]"
                  ></div>
                </div>
              </a>
            </div>
          </div>
        </div>
        <div
          class="absolute bottom-[-16px] right-2 md:right-8 lg:right-16 flex items-center gap-2 select-none pointer-events-none transform rotate-3"
        >
          <svg
            class="w-10 h-10 md:w-12 md:h-12 text-primary/60 -scale-y-100 -rotate-12 transform"
            viewBox="0 0 100 100"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M15,75 Q40,70 58,40 Q70,20 74,10 M74,10 L63,12 M74,10 L69,21"
              stroke="currentColor"
              stroke-width="2.5"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
          </svg>
          <span
            class="font-handwritten text-base md:text-lg lg:text-xl text-primary/90 leading-none"
          >
            hovering these pills<br />won’t increase my skill issue
          </span>
        </div>
      </div>
    </div>
    <div
      class="absolute bottom-0 md:-bottom-[40px] inset-x-0 h-[200px] md:h-[280px] pointer-events-none select-none z-10"
      style="mask-image: linear-gradient(to bottom, black 0%, black 75%, transparent 100%); -webkit-mask-image: linear-gradient(to bottom, black 0%, black 75%, transparent 100%);"
    >
      <svg
        class="absolute inset-0 w-full h-full"
        viewBox="0 0 1440 320"
        preserveAspectRatio="none"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <defs>
          <linearGradient id="waveGradient" x1="0" y1="0" x2="0" y2="1">
            <stop offset="0%" stop-color="var(--color-primary)" stop-opacity="0.6" />
            <stop offset="20%" stop-color="var(--color-primary)" stop-opacity="0.25" />
            <stop offset="100%" stop-color="var(--color-primary)" stop-opacity="0" />
          </linearGradient>

          <radialGradient id="troughLight" cx="50%" cy="85%" r="45%">
            <stop offset="0%" stop-color="white" stop-opacity="0.6" />
            <stop offset="50%" stop-color="white" stop-opacity="0.15" />
            <stop offset="100%" stop-color="white" stop-opacity="0" />
          </radialGradient>

          <filter id="waveTexture" x="0%" y="0%" width="100%" height="100%">
            <feTurbulence type="fractalNoise" baseFrequency="0.75" numOctaves="4" result="noise" />
            <feColorMatrix type="matrix" values="1 0 0 0 0  0 1 0 0 0  0 0 1 0 0  0 0 0 0.35 0" in="noise" result="coloredNoise" />
            <feComposite operator="in" in="coloredNoise" in2="SourceGraphic" result="composite" />
            <feBlend mode="multiply" in="composite" in2="SourceGraphic" />
          </filter>

          <filter id="edgeBlur">
            <feGaussianBlur stdDeviation="8" />
          </filter>
          <filter id="softHighlight">
            <feGaussianBlur stdDeviation="1.5" />
          </filter>
        </defs>
        <g filter="url(#waveTexture)">
          <path
            d="M 0,140 C 250,140 450,280 720,280 C 990,280 1190,160 1440,160 L 1440,320 L 0,320 Z"
            fill="url(#waveGradient)"
          />
          <path
            d="M 0,140 C 250,140 450,280 720,280 C 990,280 1190,160 1440,160 L 1440,320 L 0,320 Z"
            fill="url(#troughLight)"
            class="opacity-100 dark:opacity-10"
          />
        </g>
        <path
          d="M 0,140 C 250,140 450,280 720,280 C 990,280 1190,160 1440,160"
          fill="none"
          stroke="var(--color-primary)"
          stroke-width="20"
          opacity="0.4"
          filter="url(#edgeBlur)"
          transform="translate(0, 12)"
        />
        <path
          d="M 0,139 C 250,139 450,279 720,279 C 990,279 1190,159 1440,159"
          fill="none"
          stroke="white"
          stroke-width="3"
          opacity="0.4"
          filter="url(#softHighlight)"
        />
      </svg>
    </div>
      <svg
        class="w-12 h-12 md:w-16 md:h-16 text-primary/45 dark:text-primary/25 absolute left-[8%] bottom-5 hidden sm:block select-none pointer-events-none z-20"
        viewBox="0 0 100 100"
        fill="none"
        stroke="currentColor"
        stroke-width="2"
        stroke-linecap="round"
      >
        <circle cx="15" cy="72" r="3" />
        <path d="M 45,78 C 42,56 50,44 54,40" />
        <path d="M 35,74 C 31,52 23,45 18,44" />
        <path d="M 54,76 L 68,74" />
      </svg>
      <svg
        class="w-10 h-10 md:w-14 md:h-14 text-primary/45 dark:text-primary/25 absolute right-[8%] bottom-5 hidden sm:block select-none pointer-events-none z-20"
        viewBox="0 0 100 100"
        fill="none"
        stroke="currentColor"
        stroke-width="2"
        stroke-linecap="round"
        stroke-linejoin="round"
      >
        <path d="M 30,30 Q 30,45 15,45 Q 30,45 30,60 Q 30,45 45,45 Q 30,45 30,30 Z" />
        <path d="M 70,55 Q 70,65 58,65 Q 70,65 70,75 Q 70,65 82,65 Q 70,65 70,55 Z" />
      </svg>
      <div
        class="absolute left-1/2 bottom-5 md:bottom-8 -translate-x-1/2 text-center -rotate-2 z-20"
      >
        <p
          class="font-handwritten text-[12px] md:text-[13px] leading-tight text-primary/75 dark:text-text-muted/75"
        >
          onto the<br />
          fun part
        </p>
        <svg
          class="w-4 h-4 text-primary/75 dark:text-text-muted/70 mt-1 mx-auto animate-bounce-slow"
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="2.5"
          stroke-linecap="round"
          stroke-linejoin="round"
        >
          <line x1="12" y1="5" x2="12" y2="19"></line>
          <polyline points="19 12 12 19 5 12"></polyline>
        </svg>
      </div>
  </section>
</template>

<style scoped>
.custom-dashed {
  background-image: url("data:image/svg+xml,%3csvg width='100%25' height='100%25' xmlns='http://www.w3.org/2000/svg'%3e%3crect width='100%25' height='100%25' fill='none' rx='12' ry='12' stroke='%234a9ecc' stroke-opacity='0.35' stroke-width='1.5' stroke-dasharray='4%2c 10' stroke-dashoffset='0' stroke-linecap='square'/%3e%3c/svg%3e");
  background-size: 100% 100%;
  border-radius: 12px;
}

html.light .custom-dashed {
  background-image: url("data:image/svg+xml,%3csvg width='100%25' height='100%25' xmlns='http://www.w3.org/2000/svg'%3e%3crect width='100%25' height='100%25' fill='none' rx='12' ry='12' stroke='%23b9d3e8' stroke-opacity='0.85' stroke-width='1.5' stroke-dasharray='4%2c 10' stroke-dashoffset='0' stroke-linecap='square'/%3e%3c/svg%3e");
}
.custom-dashed:hover {
  background-image: none !important;
}

@keyframes bounce-slow {
  0%,
  100% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(5px);
  }
}

.animate-bounce-slow {
  animation: bounce-slow 2.4s ease-in-out infinite;
}
</style>
