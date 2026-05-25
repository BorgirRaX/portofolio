<script setup>
</script>

<template>
  <footer class="bg-transparent pt-6 pb-8 md:pt-8 md:pb-10 relative overflow-hidden z-10">
    <div class="absolute inset-0 bg-linear-to-b from-transparent via-primary/3 to-primary/10 dark:via-primary/10 dark:to-primary/20 pointer-events-none z-0"></div>
    <div class="absolute top-0 left-1/2 -translate-x-1/2 w-2/3 max-w-xl h-px bg-linear-to-r from-transparent via-primary/15 dark:via-primary/25 to-transparent pointer-events-none z-0"></div>

    <div class="max-w-5xl mx-auto px-6 relative z-10">
      <!-- TOP ROW -->
      <div
        class="flex flex-col md:flex-row justify-between items-start md:items-center gap-4 pb-6"
      >
        <!-- Left Side: Bold logo-like text with tiny doodle star -->
        <div class="flex items-center gap-2 select-none">
          <span class="font-display font-bold text-base text-neutral-900 dark:text-accent-white tracking-tight">
            Built by BorgirRaX.
          </span>
          <svg
            class="w-3.5 h-3.5 text-primary/35 animate-pulse-slow"
            viewBox="0 0 100 100"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M 50,35 Q 50,50 65,50 Q 50,50 50,65 Q 50,50 35,50 Q 50,50 50,35 Z"
              stroke="currentColor"
              stroke-width="3"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
          </svg>
        </div>

        <!-- Right Side: Small subtle personal descriptor -->
        <div>
          <p
            class="font-sans text-[11px] text-text-muted/65 tracking-wide max-w-[280px] md:max-w-none leading-relaxed text-left md:text-right"
          >
            Frontend developer, coffee enjoyer, future internet enthusiast.
          </p>
        </div>
      </div>
      <div class="border-t border-soft-navy/35 w-full"></div>

      <!-- BOTTOM ROW -->
      <div
        class="flex flex-col sm:flex-row justify-between items-center gap-3 pt-5 text-[9px]"
      >
        <!-- Left Side: Coded style text -->
        <span class="font-mono text-text-muted/45 tracking-wider text-left w-full sm:w-auto">
          © 2026 — Made with Vue &amp; too much coffee.
        </span>

        <!-- Right Side: Handwritten scrolling thanks -->
        <div class="flex items-center gap-1.5 font-handwritten text-[13px] text-text-muted/25 select-none w-full sm:w-auto justify-start sm:justify-end">
          <span>thanks for scrolling this far</span>
          <svg
            class="w-3.5 h-3.5 text-primary/20 transform translate-y-px"
            viewBox="0 0 24 24"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M6,6 L18,18 M18,10 L18,18 L10,18"
              stroke="currentColor"
              stroke-width="1.8"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
          </svg>
        </div>
      </div>
    </div>
  </footer>
</template>
