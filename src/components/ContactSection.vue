<template>
  <section id="contact" class="py-24 md:py-32 bg-background border-t border-soft-navy/40 relative overflow-hidden">
    <!-- Extremely subtle ambient glow background overlay (Max 1x per section rule) -->
    <div class="absolute bottom-0 left-1/3 translate-y-1/2 w-[250px] h-[250px] rounded-full bg-primary/2 blur-[80px] pointer-events-none z-0"></div>

    <div class="max-w-4xl mx-auto px-6 relative z-10 text-center flex flex-col items-center">
      <!-- Kicker Label -->
      <span class="font-mono text-xs font-semibold tracking-widest text-primary uppercase mb-4 block">
        // LET'S TALK
      </span>

      <!-- Headline (Poppins, bold, cinematic) -->
      <h2 class="font-display font-bold text-3xl md:text-5xl text-accent-white mb-6 leading-tight max-w-2xl tracking-tight">
        Got an idea, brand, or weird project in mind? <span class="text-primary">Let's talk.</span>
      </h2>

      <!-- Subtext (line-height: 1.8, max-width: 65ch) -->
      <p class="font-sans text-sm sm:text-base text-text-muted max-w-[65ch] mb-12 leading-[1.8] font-light">
        Saya terbuka untuk freelance project, landing page, frontend collaboration, atau sekadar ngobrol soal internet dan kopi.
      </p>

      <!-- Pill Buttons Container (Subtle border, clean spacing, smooth hover) -->
      <div class="flex flex-wrap justify-center gap-3.5 max-w-xl">
        <!-- Email -->
        <a
          href="mailto:jimy@example.com"
          class="inline-flex items-center gap-2 px-6 py-3 rounded-full border border-soft-navy bg-card/10 backdrop-blur-sm text-primary font-mono text-xs tracking-wider uppercase transition-all duration-300 hover:bg-primary hover:border-primary hover:text-dark-navy hover:-translate-y-0.5 cursor-pointer"
        >
          <svg xmlns="http://www.w3.org/2000/svg" class="w-3.5 h-3.5" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
            <path stroke-linecap="round" stroke-linejoin="round" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
          </svg>
          Email
        </a>

        <!-- GitHub -->
        <a
          href="#"
          target="_blank"
          class="inline-flex items-center gap-2 px-6 py-3 rounded-full border border-soft-navy bg-card/10 backdrop-blur-sm text-primary font-mono text-xs tracking-wider uppercase transition-all duration-300 hover:bg-primary hover:border-primary hover:text-dark-navy hover:-translate-y-0.5 cursor-pointer"
        >
          <svg class="w-3.5 h-3.5" fill="currentColor" viewBox="0 0 24 24">
            <path fill-rule="evenodd" d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.53 1.032 1.53 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482C19.138 20.193 22 16.435 22 12.017 22 6.484 17.522 2C12 2z" clip-rule="evenodd" />
          </svg>
          GitHub
        </a>

        <!-- Telegram -->
        <a
          href="#"
          target="_blank"
          class="inline-flex items-center gap-2 px-6 py-3 rounded-full border border-soft-navy bg-card/10 backdrop-blur-sm text-primary font-mono text-xs tracking-wider uppercase transition-all duration-300 hover:bg-primary hover:border-primary hover:text-dark-navy hover:-translate-y-0.5 cursor-pointer"
        >
          <svg class="w-3.5 h-3.5" fill="currentColor" viewBox="0 0 24 24">
            <path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm4.64 6.8c-.15 1.58-.8 5.42-1.13 7.19-.14.75-.42 1-.68 1.03-.58.05-1.02-.38-1.58-.75-.88-.58-1.38-.94-2.23-1.5-.99-.65-.35-1.01.22-1.59.15-.15 2.71-2.48 2.76-2.69.01-.03.01-.14-.07-.2-.08-.06-.19-.04-.27-.02-.12.02-1.96 1.25-5.54 3.69-.52.36-1 .53-1.42.52-.47-.01-1.37-.26-2.03-.48-.82-.27-1.47-.42-1.42-.88.03-.24.35-.49.97-.74 3.79-1.65 6.32-2.74 7.59-3.27 3.61-1.5 4.36-1.76 4.85-1.77.11 0 .35.03.5.16.13.12.17.29.18.41 0 .07-.01.23-.02.29z" />
          </svg>
          Telegram
        </a>

        <!-- Instagram -->
        <a
          href="#"
          target="_blank"
          class="inline-flex items-center gap-2 px-6 py-3 rounded-full border border-soft-navy bg-card/10 backdrop-blur-sm text-primary font-mono text-xs tracking-wider uppercase transition-all duration-300 hover:bg-primary hover:border-primary hover:text-dark-navy hover:-translate-y-0.5 cursor-pointer"
        >
          <!-- Instagram Icon SVG -->
          <svg class="w-3.5 h-3.5" fill="currentColor" viewBox="0 0 24 24">
            <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zM12 0C8.741 0 8.333.014 7.053.072 2.695.272.273 2.69.073 7.051C.014 8.333 0 8.741 0 12c0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98C15.668.014 15.259 0 12 0zm0 5.838a6.162 6.162 0 100 12.324 6.162 6.162 0 000-12.324zM12 16a4 4 0 110-8 4 4 0 010 8zm6.406-11.845a1.44 1.44 0 100 2.881 1.44 1.44 0 000-2.881z" />
          </svg>
          Instagram
        </a>
      </div>
    </div>
  </section>
</template>
