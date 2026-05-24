<template>
  <section
    id="about"
    class="pt-12 pb-32 bg-background border-t border-soft-navy/40 relative overflow-hidden"
  >
    <div
      class="absolute inset-0 z-0 opacity-[0.014] dark:opacity-[0.05] pointer-events-none"
      style="
        mask-image: radial-gradient(circle at center, black 30%, transparent 80%);
        -webkit-mask-image: radial-gradient(circle at center, black 30%, transparent 80%);
      "
    >
      <svg width="100%" height="100%" xmlns="http://www.w3.org/2000/svg">
        <pattern id="grid-about" width="40" height="40" patternUnits="userSpaceOnUse">
          <path d="M 40 0 L 0 0 0 40" fill="none" stroke="#4a9ecc" stroke-width="0.35" />
        </pattern>
        <rect width="100%" height="100%" fill="url(#grid-about)" />
      </svg>
    </div>

    <!-- Cloudy blobs, not fog -->
    <div
      class="absolute left-[-90px] top-24 w-[220px] h-[160px] rounded-full bg-primary/30 blur-[35px] pointer-events-none z-0"
    ></div>
    <div
      class="absolute left-[-30px] top-40 w-[140px] h-[100px] rounded-full bg-primary/12 blur-[28px] pointer-events-none z-0"
    ></div>
    <div
      class="absolute right-[-80px] top-36 w-[240px] h-[170px] rounded-full bg-primary/20 blur-[38px] pointer-events-none z-0"
    ></div>
    <div
      class="absolute right-[30px] top-56 w-[120px] h-[90px] rounded-full bg-primary/10 blur-[26px] pointer-events-none z-0"
    ></div>

    <svg
      class="absolute inset-0 w-full h-full opacity-[0.22] dark:opacity-[0.07] pointer-events-none z-10"
      xmlns="http://www.w3.org/2000/svg"
    >
      <filter id="grainyNoiseAbout">
        <feTurbulence
          type="fractalNoise"
          baseFrequency="0.75"
          numOctaves="3"
          stitchTiles="stitch"
        />
      </filter>
      <rect width="100%" height="100%" filter="url(#grainyNoiseAbout)" />
    </svg>

    <div class="max-w-5xl mx-auto px-6 relative z-20">
      <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 lg:gap-16 items-center">
        <div class="lg:col-span-7 flex flex-col items-start text-left relative">
          <!-- ABOUT ME -->
          <svg
            class="absolute -left-18 -top-5 w-15 h-15 -rotate-15 text-primary/50 hidden md:block select-none pointer-events-none animate-pulse-slow"
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
            <circle cx="21" cy="80" r="2.2" fill="currentColor" opacity="0.85" />
          </svg>
          <span class="font-mono text-xs font-semibold tracking-widest text-primary uppercase mb-4">
            // MY LITLE STORY
          </span>

          <div class="relative w-full">
            <svg
              class="absolute -right-2 -top-8 w-8 h-8 text-primary/30 hidden md:block select-none pointer-events-none"
              viewBox="0 0 100 100"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M10,50 L30,20 L50,60 L70,30 L90,60"
                stroke="currentColor"
                stroke-width="1.5"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
            </svg>
            <h2
              class="font-display font-bold text-2xl md:text-4xl text-accent-white mb-8 leading-[1.2] tracking-tight"
            >
              making websites<br />instead of<br />
              <span class="relative inline-block text-primary">
                touching grass.
                <span
                  class="absolute left-0 -bottom-2 w-full h-[4px] bg-primary/45 rounded-full"
                ></span>
                <span
                  class="absolute left-1 -bottom-3.5 w-[96%] h-[2px] bg-primary/30 rounded-full"
                ></span>
              </span>
            </h2>
          </div>

          <!-- STORYTELLING PARAGRAPHS -->
          <div
            class="font-sans text-sm sm:text-base text-text-muted space-y-6 leading-[1.8] font-light max-w-[65ch]"
          >
            <p>
              I grew up between
              <span class="text-accent-white/95 font-medium">Temanggung </span> and
              <span class="text-accent-white/95 font-medium"> Kalimantan </span> as the son of a
              farmer—someone far better at taking care of crops than I am at shipping projects on
              time.
            </p>
            <p>
              My journey into the digital world started from simple curiosity. I once helped build a
              <span class="text-primary font-medium relative"
                >real coffee shop<span
                  class="absolute left-0 -bottom-0.5 w-full h-px bg-primary/30"
                ></span
              ></span>
              from the ground up: discussing menus, arranging interiors, and eventually designing
              their website.
            </p>
            <p>
              That experience made me realize: websites are not just lines of code, but
              <span class="relative inline-block font-medium text-primary">
                experiences people can actually feel.
                <span
                  class="absolute left-0 -bottom-0.5 w-full h-[3px] bg-primary/35 rounded-full"
                ></span>
              </span>
            </p>
            <p>
              Outside of work, I enjoy
              <span
                class="text-primary hover:text-primary/80 transition-colors duration-300 font-medium"
                >pixel art</span
              >, visual storytelling, and geeking out over the latest in Web3 and the future of the
              internet.
            </p>
          </div>
        </div>

        <!-- IDENTITY CARD COMPONENT -->
        <div class="lg:col-span-5 flex justify-center relative py-8">
          <div
            class="absolute -right-16 top-16 hidden md:flex items-center gap-2 select-none pointer-events-none text-primary/45 rotate-6 z-20"
          >
            <svg
              class="w-10 h-10 transform -scale-x-100 rotate-[-20deg]"
              viewBox="0 0 100 100"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M15,15 C35,10 50,30 40,55"
                stroke="currentColor"
                stroke-width="1.5"
                stroke-linecap="round"
              />
              <path
                d="M28,49 L43,58 L39,41"
                stroke="currentColor"
                stroke-width="1.5"
                stroke-linecap="round"
              />
            </svg>
            <span class="font-handwritten text-sm text-text-muted/80 tracking-wide text-left"
              >coffe<br />&amp; code</span
            >
          </div>
          <div
            class="absolute -left-20 -bottom-10 hidden md:flex items-center gap-1 z-20 select-none rotate-[-4deg]"
          >
            <svg
              class="w-10 h-10 text-primary/35 transform -rotate-135"
              viewBox="0 0 100 100"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M20,20 C40,15 65,30 55,60"
                stroke="currentColor"
                stroke-width="1.3"
                stroke-linecap="round"
              />
              <path
                d="M43,53 L58,63 L53,46"
                stroke="currentColor"
                stroke-width="1.3"
                stroke-linecap="round"
              />
            </svg>
            <div
              class="bg-card/75 border border-soft-navy/80 px-3 py-1.5 rounded-lg shadow-md font-handwritten text-xs text-text-muted/95 flex items-center gap-1.5 backdrop-blur-[1px]"
            >
              probably tweaking<br />padding rn 🤷‍♂️
            </div>
          </div>
          <div
            class="absolute -right-14 -bottom-6 hidden md:block select-none pointer-events-none text-primary/45 rotate-[4deg] z-20"
          >
            <div class="relative w-[145px] h-[60px] flex items-center justify-center">
              <svg
                class="absolute inset-0 w-full h-full stroke-primary/50"
                viewBox="0 0 140 60"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
                preserveAspectRatio="none"
              >
                <path
                  d="M10,30 C10,12 50,8 90,10 C130,12 135,32 110,45 C85,58 30,55 15,45 C5,38 8,25 40,18"
                  stroke-width="1.2"
                  stroke-linecap="round"
                />
              </svg>
              <span
                class="font-handwritten text-sm text-text-muted/80 tracking-wide relative z-10 text-center leading-tight select-none pointer-events-none"
                >certified<br />overthinker</span
              >
            </div>
          </div>

          <div
            class="relative w-full max-w-[325px] aspect-4/5 rounded-3xl border border-soft-navy/80 bg-card/45 backdrop-blur-md p-6 flex flex-col justify-between overflow-visible group hover:border-primary/30 transition-all duration-500 shadow-[0_20px_50px_rgba(10,15,24,0.3)] z-10"
          >
            <div class="flex justify-between items-center z-10 border-b border-soft-navy/50 pb-3">
              <span class="font-mono text-[9px] tracking-widest text-text-muted uppercase"
                >IDENTITY CARD</span
              >
              <span class="w-1.5 h-1.5 rounded-full bg-primary animate-pulse"></span>
            </div>
            <div class="my-auto flex flex-col items-center justify-center z-10 py-4 relative">
              <div
                class="relative bg-white/95 dark:bg-white p-3.5 pb-8 shadow-[0_12px_35px_rgba(0,0,0,0.3)] border border-neutral-200/50 rotate-[-2.5deg] group-hover:rotate-[0.5deg] group-hover:scale-[1.01] transition-all duration-500 w-full max-w-[215px]"
              >
                <svg
                  class="absolute -top-6 left-1/2 -translate-x-1/2 w-24 h-10 -rotate-2 pointer-events-none z-20 text-primary/60"
                  viewBox="0 0 100 35"
                  fill="currentColor"
                  opacity="0.8"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    d="M 12 8 C 30 6, 65 7, 88 6 L 89 9 L 87 12 L 90 15 L 88 18 L 91 21 L 87 24 L 89 27 C 65 29, 30 27, 11 28 L 13 25 L 10 22 L 13 19 L 11 16 L 14 13 Z"
                  />
                  <path
                    d="M 16 11 Q 48 10 84 9.5"
                    stroke="white"
                    stroke-width="0.8"
                    stroke-linecap="round"
                    opacity="0.35"
                  />
                  <path
                    d="M 14 24 Q 48 23.5 86 24"
                    stroke="black"
                    stroke-width="0.6"
                    stroke-linecap="round"
                    opacity="0.15"
                  />
                </svg>
                <div
                  class="relative w-full aspect-square overflow-hidden bg-neutral-100 rounded-sm"
                >
                  <img
                    src="../assets/profil_pic1.png"
                    alt="Jimy Profile"
                    class="w-full h-full object-contain filter contrast-[1.02] grayscale-10 saturate-[0.96] brightness-[0.98] group-hover:grayscale-0 transition-all duration-500"
                    loading="lazy"
                  />
                  <div
                    class="absolute inset-0 pointer-events-none bg-neutral-950/2 mix-blend-overlay"
                  ></div>
                </div>
                <div class="mt-4 text-center select-none">
                  <h2
                    class="font-display font-bold text-sm text-neutral-900 tracking-wide uppercase leading-none"
                  >
                    JIMY.
                  </h2>
                  <p class="font-mono text-[7px] text-neutral-500 tracking-wide mt-1">
                    FARMER &lt;/&gt; COFFEE &lt;/&gt; CODE
                  </p>
                </div>
                <img
                  src="../assets/accent.png"
                  alt="Pixel Burger Mascot Sticker"
                  class="absolute -right-4 -bottom-4 w-16 h-16 object-contain rotate-14 opacity-90 saturate-90 brightness-95 drop-shadow-sm hover:-rotate-6 hover:scale-110 transition-all duration-500 pointer-events-auto z-30"
                />
              </div>
            </div>
            <div class="border-t border-soft-navy/50 pt-3.5 z-10 space-y-2.5">
              <div class="flex justify-between items-center text-[10px] font-mono">
                <span class="text-text-muted uppercase">BORN IN</span>
                <span class="text-ice-blue">Temanggung</span>
              </div>
              <div class="flex justify-between items-center text-[10px] font-mono">
                <span class="text-text-muted uppercase">BASED IN</span>
                <span class="text-ice-blue">Semarang</span>
              </div>
              <div class="flex justify-between items-center text-[10px] font-mono">
                <span class="text-text-muted uppercase">STATUS</span>
                <div class="flex items-center gap-1.5 text-ice-blue">
                  <span class="w-1.5 h-1.5 rounded-full bg-primary animate-pulse"></span>
                  <span>currently building weird interfaces</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
