<template>
  <section
    class="relative min-h-screen flex items-center justify-center bg-transparent"
  >
    <div
      class="absolute top-0 left-0 right-0 -bottom-[200px] pointer-events-none z-20 opacity-[0.08] dark:opacity-[0.12] mix-blend-overlay"
      style="
        background-image: url('data:image/svg+xml,%3Csvg viewBox=%220 0 200 200%22 xmlns=%22http://www.w3.org/2000/svg%22%3E%3Cfilter id=%22noiseFilter%22%3E%3CfeTurbulence type=%22fractalNoise%22 baseFrequency=%220.8%22 numOctaves=%223%22 stitchTiles=%22stitch%22/%3E%3C/filter%3E%3Crect width=%22100%25%22 height=%22100%25%22 filter=%22url(%23noiseFilter)%22/%3E%3C/svg%3E');
        mask-image: linear-gradient(to bottom, black 70%, transparent 100%);
        -webkit-mask-image: linear-gradient(to bottom, black 70%, transparent 100%);
      "
    ></div>

    <div
      class="absolute top-0 left-0 right-0 -bottom-[200px] pointer-events-none z-0 opacity-50 dark:opacity-20 text-primary/70"
      style="
        background-image: radial-gradient(currentColor 1.5px, transparent 1.5px);
        background-size: 28px 28px;
        mask-image: radial-gradient(ellipse at 50% 40%, transparent 45%, black 85%, transparent 100%);
        -webkit-mask-image: radial-gradient(ellipse at 50% 40%, transparent 45%, black 85%, transparent 100%);
      "
    ></div>

    <svg class="absolute top-[25%] left-[8%] md:left-[15%] w-3.5 h-3.5 text-primary/30 dark:text-primary/20 animate-pulse-slow pointer-events-none z-0" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round"><path d="M12 4v16M4 12h16"/></svg>
    <svg class="absolute top-[35%] right-[10%] md:right-[15%] w-3 h-3 text-primary/25 dark:text-primary/15 animate-bounce pointer-events-none z-0" style="animation-duration: 4s;" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><circle cx="12" cy="12" r="10"/></svg>
    <svg class="absolute bottom-[10%] left-[15%] md:left-[22%] w-6 h-6 text-primary/25 dark:text-primary/15 pointer-events-none z-0" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round"><path d="M4 12h.01M12 12h.01M20 12h.01"/></svg>
    <div
      class="absolute -top-[10%] -left-[10%] w-[600px] h-[600px] md:w-[900px] md:h-[900px] rounded-full bg-cyan-400/25 dark:bg-cyan-500/8 blur-[140px] md:blur-[180px] pointer-events-none z-0"
    ></div>
    <div
      class="absolute -bottom-[5%] -right-[5%] w-[500px] h-[500px] md:w-[800px] md:h-[800px] rounded-full bg-blue-300/20 dark:bg-blue-500/8 blur-[130px] md:blur-[170px] pointer-events-none z-0"
    ></div>
    <div
      class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[500px] h-[500px] md:w-[900px] md:h-[900px] rounded-full bg-primary/18 dark:bg-primary/8 blur-[150px] md:blur-[200px] pointer-events-none z-0"
    ></div>
    <div
      class="absolute top-[15%] right-[20%] w-[300px] h-[300px] md:w-[500px] md:h-[500px] rounded-full bg-amber-300/10 dark:bg-amber-500/5 blur-[120px] md:blur-[160px] pointer-events-none z-0"
    ></div>
    <div
      class="absolute bottom-[20%] left-[25%] w-[250px] h-[250px] md:w-[400px] md:h-[400px] rounded-full bg-indigo-300/8 dark:bg-indigo-500/4 blur-[110px] md:blur-[150px] pointer-events-none z-0"
    ></div>

    <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 pointer-events-none z-0">
      <svg class="w-[500px] h-[500px] md:w-[700px] md:h-[700px] opacity-[0.06] dark:opacity-[0.08]" viewBox="0 0 700 700" fill="none" xmlns="http://www.w3.org/2000/svg">
        <circle cx="350" cy="350" r="80" stroke="var(--color-primary)" stroke-width="1"/>
        <circle cx="350" cy="350" r="140" stroke="var(--color-primary)" stroke-width="0.8"/>
        <circle cx="350" cy="350" r="210" stroke="var(--color-primary)" stroke-width="0.6"/>
        <circle cx="350" cy="350" r="290" stroke="var(--color-primary)" stroke-width="0.4"/>
        <circle cx="350" cy="350" r="340" stroke="var(--color-primary)" stroke-width="0.3"/>
      </svg>
    </div>

    <div
      class="absolute top-0 left-0 right-0 -bottom-[300px] pointer-events-none z-0 opacity-35 dark:opacity-70"
      style="background: radial-gradient(circle, transparent 55%, var(--color-background) 100%)"
    ></div>

    <div class="max-w-4xl mx-auto px-6 relative z-10 text-center flex flex-col items-center">
      <div
        class="relative inline-flex items-center gap-2 px-4 py-1.5 mb-6 animate-pulse-slow"
      >
        <svg
          class="absolute -inset-2 w-[calc(100%+16px)] h-[calc(100%+16px)] pointer-events-none z-0 stroke-primary/40"
          viewBox="0 0 200 40"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M6,18 C30,3 170,2 194,18 C206,26 165,36 90,35 C40,34 2,27 10,14"
            stroke-width="1.2"
            stroke-linecap="round"
            stroke-linejoin="round"
          />
        </svg>

        <span class="relative flex h-1.5 w-1.5 z-10">
          <span
            class="animate-ping absolute inline-flex h-full w-full rounded-full bg-primary opacity-75"
          ></span>
          <span class="relative inline-flex rounded-full h-1.5 w-1.5 bg-primary"></span>
        </span>
        <span
          class="font-mono text-[9px] font-semibold tracking-widest text-text-muted uppercase z-10"
        >
          OPEN FOR COOL PROJECTS
        </span>
      </div>

      <div class="relative max-w-3xl">
        <svg
          class="absolute -top-10 -left-6 w-7 h-7 text-primary/45 hidden md:block select-none pointer-events-none animate-pulse-slow"
          viewBox="0 0 24 24"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M12,2 L14.5,9 L22,9 L16,13.5 L18.5,21 L12,16.5 L5.5,21 L8,13.5 L2,9 L9.5,9 Z"
            stroke="currentColor"
            stroke-width="1.2"
            stroke-linecap="round"
            stroke-linejoin="round"
          />
        </svg>
        <div
          class="absolute -left-12 md:-left-20 top-24 hidden md:inline-flex items-center gap-1.5 px-3 py-1 bg-card/20 border border-text-muted/15 rounded-lg shadow-sm backdrop-blur-[2px] -rotate-3 select-none pointer-events-none transition-transform duration-500 hover:rotate-0"
        >
          <span class="font-mono text-[9px] font-medium text-text-muted/80 tracking-wide"
            >made in Semarang</span
          >
        </div>
        <div
          class="absolute -right-16 md:-right-24 top-48 hidden md:inline-flex items-center gap-1.5 px-3 py-1 bg-card/20 border border-text-muted/15 rounded-lg shadow-sm backdrop-blur-[2px] rotate-3 select-none pointer-events-none transition-transform duration-500 hover:-rotate-2"
        >
          <span class="font-mono text-[9px] font-medium text-text-muted/80 tracking-wide"
            >currently overthinking☕</span
          >
        </div>

        <!-- HEADLINE -->
        <h1
          class="font-display font-bold text-3xl sm:text-5xl md:text-6xl tracking-tight text-accent-white mb-6 leading-[1.15] animate-fade-in-up"
        >
          I turn ideas into websites
          <span class="text-primary text-4xl md:text-5xl">people enjoy using.</span>
        </h1>
      </div>

      <p
        class="font-sans text-sm sm:text-base md:text-lg text-text-muted max-w-2xl mb-12 leading-[1.8] font-light animate-fade-in-up"
        style="animation-delay: 0.1s"
      >
        Frontend developer based in Semarang. I love making things that are useful, playful, and
        beautifully detailed.
      </p>

      <div
        class="relative flex flex-col sm:flex-row gap-4 w-full sm:w-auto animate-fade-in-up"
        style="animation-delay: 0.2s"
      >
        <div
          class="absolute -right-16 md:-right-28 bottom-[-56px] hidden md:block select-none pointer-events-none text-primary/30"
        >
          <svg
            class="w-16 h-16 transform -rotate-12"
            viewBox="0 0 100 100"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M15,15 C45,10 65,30 60,50 C55,70 32,65 25,80"
              stroke="currentColor"
              stroke-width="1.3"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
            <path
              d="M17,73 L26,82 L35,73"
              stroke="currentColor"
              stroke-width="1.3"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
          </svg>
          <span
            class="absolute left-16 top-14 font-handwritten text-sm text-text-muted/70 tracking-wide"
            >projects</span
          >
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
      <div
        class="absolute -right-8 md:-right-16 -bottom-2 hidden md:flex flex-col items-center select-none pointer-events-none z-20 animate-float-burger"
      >
        <div
          class="p-2 bg-card/60 border border-text-muted/15 rounded-2xl shadow-[0_8px_30px_rgba(0,0,0,0.3)] backdrop-blur-sm"
        >
          <img
            src="../assets/pixel_burger.png"
            alt="Pixel Burger Mascot"
            class="w-12 h-12 object-contain"
            loading="lazy"
          />
        </div>
        <span class="mt-1 font-handwritten text-[11px] text-text-muted/65 tracking-wide"
          >jimy's mascot 🍔</span
        >
      </div>
    </div>
    <a
      href="#about"
      class="absolute bottom-8 left-1/2 -translate-x-1/2 flex flex-col items-center gap-2 text-text-muted hover:text-primary transition-colors duration-500 z-10 opacity-70 hover:opacity-100"
    >
      <span class="font-handwritten text-sm tracking-wide text-text-muted/80">scroll down</span>
      <svg
        xmlns="http://www.w3.org/2000/svg"
        class="w-4 h-4 animate-bounce"
        fill="none"
        viewBox="0 0 24 24"
        stroke="currentColor"
        stroke-width="1.5"
      >
        <path stroke-linecap="round" stroke-linejoin="round" d="M19 14l-7 7m0 0l-7-7m7 7V3" />
      </svg>
    </a>

    <svg
      class="absolute bottom-0 left-[28%] w-8 h-20 text-primary/25 pointer-events-none select-none hidden md:block z-20"
      viewBox="0 0 100 200"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
    >
      <path
        d="M 30,0 Q 60,100 50,200"
        stroke="currentColor"
        stroke-width="1.8"
        stroke-linecap="round"
        stroke-dasharray="5 5"
      />
    </svg>

    <svg
      class="absolute bottom-0 right-[24%] w-6 h-14 text-primary/20 pointer-events-none select-none hidden md:block z-20"
      viewBox="0 0 100 200"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
    >
      <path
        d="M 70,0 C 40,80 60,140 50,200"
        stroke="currentColor"
        stroke-width="1.5"
        stroke-linecap="round"
      />
    </svg>
  </section>
</template>

<style scoped>
@keyframes float {
  0%,
  100% {
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
