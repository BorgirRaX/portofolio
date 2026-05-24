<template>
  <footer class="bg-background border-t border-soft-navy/40 py-12 relative z-10">
    <div class="max-w-5xl mx-auto px-6">
      <!-- Upper Footer Row -->
      <div
        class="flex flex-col md:flex-row justify-between items-start md:items-center gap-6 pb-8 border-b border-soft-navy/20"
      >
        <!-- Left Side -->
        <div class="flex flex-col items-start text-left">
          <span class="font-display font-semibold text-sm text-accent-white tracking-wide">
            Built by BorgirRax.
          </span>
        </div>

        <!-- Right Side -->
        <div class="flex flex-col items-start md:items-end text-left md:text-right">
          <p
            class="font-sans text-[11px] text-text-muted tracking-wide max-w-[280px] md:max-w-none leading-relaxed"
          >
            Frontend developer, coffee enjoyer, future internet enthusiast.
          </p>
        </div>
      </div>

      <!-- Lower Footer Row -->
      <div
        class="flex flex-col sm:flex-row justify-between items-center gap-4 pt-6 text-[10px] font-mono text-text-muted"
      >
        <span> © 2026 — Made with Vue &amp; too much coffee. </span>
        <div class="flex gap-4">
          <a href="#" class="hover:text-primary transition-colors">Privacy</a>
          <a href="#" class="hover:text-primary transition-colors">Terms</a>
        </div>
      </div>
    </div>
  </footer>
</template>
