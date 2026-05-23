<template>
  <section class="relative min-h-screen flex items-center justify-center overflow-hidden bg-background">
    <svg class="absolute inset-0 w-full h-full opacity-[0.08] dark:opacity-[0.025] pointer-events-none z-0" xmlns="http://www.w3.org/2000/svg">
      <filter id="grainyNoise">
        <feTurbulence type="fractalNoise" baseFrequency="0.75" numOctaves="3" stitchTiles="stitch" />
      </filter>
      <rect width="100%" height="100%" filter="url(#grainyNoise)" />
    </svg>

    <div
      class="absolute inset-0 z-0 opacity-[0.22] dark:opacity-[0.10] pointer-events-none"
      style="mask-image: radial-gradient(circle at center, black 40%, transparent 85%); -webkit-mask-image: radial-gradient(circle at center, black 40%, transparent 85%);"
    >
      <svg width="100%" height="100%" xmlns="http://www.w3.org/2000/svg">
        <defs>
          <pattern id="grid-subtle" width="80" height="80" patternUnits="userSpaceOnUse">
            <path d="M 80 0 L 0 0 0 80" fill="none" stroke="#4a9ecc" stroke-width="1.0" />
          </pattern>
        </defs>
        <rect width="100%" height="100%" fill="url(#grid-subtle)" />
      </svg>
    </div>

    <div class="absolute top-0 left-0 w-[500px] h-[500px] md:w-[800px] md:h-[800px] rounded-full bg-cyan-400/18 dark:bg-cyan-500/5 blur-[130px] md:blur-[170px] pointer-events-none z-0"></div>
    <div class="absolute bottom-0 right-0 w-[400px] h-[400px] md:w-[700px] md:h-[700px] rounded-full bg-blue-300/14 dark:bg-blue-500/5 blur-[120px] md:blur-[160px] pointer-events-none z-0"></div>
    <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[400px] h-[400px] md:w-[800px] md:h-[800px] rounded-full bg-primary/14 dark:bg-primary/5 blur-[140px] md:blur-[190px] pointer-events-none z-0"></div>
    <div class="absolute inset-0 pointer-events-none z-0 opacity-35 dark:opacity-70"
         style="background: radial-gradient(circle, transparent 55%, var(--color-background) 100%);">
    </div>

    <div class="max-w-4xl mx-auto px-6 relative z-10 text-center flex flex-col items-center">
      <div class="relative inline-flex items-center gap-2 px-4 py-1.5 rounded-full border border-soft-navy bg-card/40 backdrop-blur-sm mb-6 shadow-sm animate-pulse-slow">
        <svg class="absolute -inset-2 w-[calc(100%+16px)] h-[calc(100%+16px)] pointer-events-none z-0 stroke-primary/30" viewBox="0 0 200 40" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M6,18 C30,3 170,2 194,18 C206,26 165,36 90,35 C40,34 2,27 10,14" stroke-width="1" stroke-linecap="round" stroke-linejoin="round" />
        </svg>

        <span class="relative flex h-1.5 w-1.5 z-10">
          <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-primary opacity-75"></span>
          <span class="relative inline-flex rounded-full h-1.5 w-1.5 bg-primary"></span>
        </span>
        <span class="font-mono text-[9px] font-semibold tracking-widest text-text-muted uppercase z-10">
          OPEN FOR COOL PROJECTS
        </span>
      </div>

      <div class="relative max-w-3xl">
        <svg class="absolute -top-10 -left-6 w-7 h-7 text-primary/45 hidden md:block select-none pointer-events-none animate-pulse-slow" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M12,2 L14.5,9 L22,9 L16,13.5 L18.5,21 L12,16.5 L5.5,21 L8,13.5 L2,9 L9.5,9 Z" stroke="currentColor" stroke-width="1.2" stroke-linecap="round" stroke-linejoin="round" />
        </svg>
        <div class="absolute -left-12 md:-left-20 top-24 hidden md:inline-flex items-center gap-1.5 px-3 py-1 bg-card/20 border border-text-muted/15 rounded-lg shadow-sm backdrop-blur-[2px] -rotate-3 select-none pointer-events-none transition-transform duration-500 hover:rotate-0">
          <span class="font-mono text-[9px] font-medium text-text-muted/80 tracking-wide">made in Semarang</span>
        </div>
        <div class="absolute -right-16 md:-right-24 top-48 hidden md:inline-flex items-center gap-1.5 px-3 py-1 bg-card/20 border border-text-muted/15 rounded-lg shadow-sm backdrop-blur-[2px] rotate-3 select-none pointer-events-none transition-transform duration-500 hover:-rotate-2">
          <span class="font-mono text-[9px] font-medium text-text-muted/80 tracking-wide">currently overthinking☕</span>
        </div>

        <!-- HEADLINE -->
        <h1 class="font-display font-bold text-3xl sm:text-5xl md:text-6xl tracking-tight text-accent-white mb-6 leading-[1.15] animate-fade-in-up">
          I turn ideas into websites <span class="text-primary text-4xl md:text-5xl">people enjoy using.</span>
        </h1>
      </div>

      <p class="font-sans text-sm sm:text-base md:text-lg text-text-muted max-w-2xl mb-12 leading-[1.8] font-light animate-fade-in-up" style="animation-delay: 0.1s;">
        Frontend developer based in Semarang. I love making things that are useful, playful, and beautifully detailed.
      </p>

      <div class="relative flex flex-col sm:flex-row gap-4 w-full sm:w-auto animate-fade-in-up" style="animation-delay: 0.2s;">
        <div class="absolute -right-16 md:-right-28 bottom-[-56px] hidden md:block select-none pointer-events-none text-primary/30">
          <svg class="w-16 h-16 transform -rotate-12" viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M15,15 C45,10 65,30 60,50 C55,70 32,65 25,80" stroke="currentColor" stroke-width="1.3" stroke-linecap="round" stroke-linejoin="round" />
            <path d="M17,73 L26,82 L35,73" stroke="currentColor" stroke-width="1.3" stroke-linecap="round" stroke-linejoin="round" />
          </svg>
          <span class="absolute left-16 top-14 font-handwritten text-sm text-text-muted/70 tracking-wide">projects</span>
        </div>

        <!-- CTA -->
        <a
          href="#projects"
          class="inline-flex justify-center items-center px-8 py-3.5 rounded-xl bg-primary text-dark-navy font-sans font-semibold text-xs tracking-wider uppercase transition-all duration-500 hover:-translate-y-2 hover:rotate-3 hover:text-white shadow-[0_0_20px_rgba(74,158,204,0.15)] cursor-pointer"
        >
          See What I've Built
        </a>

        <a
          href="#about"
          class="inline-flex justify-center items-center px-8 py-3.5 rounded-xl border border-text-muted/30 hover:border-primary/50 text-text-muted hover:text-accent-white font-sans font-semibold text-xs tracking-wider uppercase bg-card/10 backdrop-blur-sm transition-all duration-500 hover:-translate-y-2 hover:-rotate-3 cursor-pointer"
        >
          My Little Story
        </a>
      </div>

      <!-- Pixel Burger Mascot Sticker -->
      <div class="absolute -right-8 md:-right-16 -bottom-2 hidden md:flex flex-col items-center select-none pointer-events-none z-20 animate-float-burger">
        <div class="p-2 bg-card/60 border border-text-muted/15 rounded-2xl shadow-[0_8px_30px_rgba(0,0,0,0.3)] backdrop-blur-sm">
          <img
            src="../assets/pixel_burger.png"
            alt="Pixel Burger Mascot"
            class="w-12 h-12 object-contain"
            loading="lazy"
          >
        </div>
        <span class="mt-1 font-handwritten text-[11px] text-text-muted/65 tracking-wide">jimy's mascot 🍔</span>
      </div>
    </div>
    <a
      href="#about"
      class="absolute bottom-8 left-1/2 -translate-x-1/2 flex flex-col items-center gap-2 text-text-muted hover:text-primary transition-colors duration-500 z-10 opacity-70 hover:opacity-100"
    >
      <span class="font-handwritten text-sm tracking-wide text-text-muted/80">scroll down</span>
      <svg xmlns="http://www.w3.org/2000/svg" class="w-4 h-4 animate-bounce" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
        <path stroke-linecap="round" stroke-linejoin="round" d="M19 14l-7 7m0 0l-7-7m7 7V3" />
      </svg>
    </a>
  </section>
</template>

<style scoped>
@keyframes float {
  0%, 100% {
    transform: translateY(0) rotate(-6deg);
  }
  50% {
    transform: translateY(-6px) rotate(-4deg);
  }
}

.animate-float-burger {
  animation: float 5s ease-in-out infinite;
}
</style>
