# Portfolio Project Plan — jimy.

## Overview
Personal portfolio website dengan vibe **playful + techy + cinematic**.

Didesain untuk menampilkan project frontend dengan identitas visual kuat,
clean interaction, dan storytelling personal.

Bukan sekadar portfolio developer biasa,
tetapi ruang digital yang terasa hidup, punya karakter,
dan meninggalkan impresi.

Stack:
Vue 3 + Vite + Tailwind CSS

Focus:
Frontend development, landing page design, UI storytelling,
dan eksplorasi Web3 interface.

---

## Brand Direction

### Personality
- Playful
- Calm
- Confident
- Slightly experimental
- Human, not corporate

### Design Principle
- Big typography
- Strong spacing
- Minimal accent usage
- Atmospheric dark mode
- Motion secukupnya
- Fokus pada readability & rhythm

### Keywords
```txt
clean
cinematic
modern
interactive
personal
not generic

---

### Color Palette

| Token          | Hex         |
|----------------|-------------|
| Background     | `#0F1721`   |
| Surface / Card | `#0A0F18`   |
| Primary blue   | `#4A9ECC`   |
| Ice blue       | `#D4EEFF`   |
| Soft Navy      | `#152232`   |
| Dark Navy      | `#060C14`   |
| Accent White   | `#F0F8FF`   |
| Text Body      | `#F0F8FF`   |
| Text Muted     | `#7EC4E8`   |

### Rules

Accent blue hanya untuk elemen penting
Glow effect maksimal 1× per section
Background grid opacity rendah
Prioritaskan kontras & readability

Default:
Dark mode. tersedia light mode toggle.

---

## Struktur Komponen
src/
├── components/
│   ├── NavBar.vue
│   ├── HeroSection.vue
│   ├── AboutSection.vue
│   ├── SkillsSection.vue
│   ├── ProjectsSection.vue
│   ├── ContactSection.vue
│   └── FooterSection.vue
├── App.vue
└── main.js

---

## Typography

### Heading
Font:Poppins / Satoshi / Plus Jakarta Sans

Style:
- Bold
- Tight spacing
- Clean modern feel

### Body
- Readable, airy, comfortable.

### Recommended:
- line-height: 1.8;
- max-width: 65ch;

---

## Sections

### 1. NavBar

- Logo
    - jimy.
    - Warna: #4A9ECC
- Links
    - About
    - Skills
    - Projects
    - Contact

### Features
- sticky navbar
- backdrop blur saat scroll
- mobile menu slide-in
- smooth hover transition

### Style
- Minimal dan clean.
- Navbar tidak terlalu dominan.

---

### 2. Hero Section

#### Badge
AVAILABLE FOR WORK

#### Headline
I turn ideas into websites people actually enjoy using.

#### Subheadline
Frontend developer from Semarang.
Crafting clean interfaces, playful experiences,
and digital spaces people remember.

#### CTA
- Primary
    - View Projects
- Secondary
    - About Me

#### Visual Direction
- Big bold typography
- Grid background opacity rendah
- Sedikit floating glow
- Motion subtle
- Fokus readability

#### Notes
- Jangan terlalu banyak: glow, particle, neon effect, animated decoration.
- Hero harus impactful, bukan melelahkan.

---

### 3. About Section

#### Label
// ABOUT ME

#### Heading
I make websites that people actually enjoy using.

#### Body
Growing up between Temanggung and Kalimantan,
I am the son of a farmer who is much more skilled
at growing plants than launching projects on time.

My journey into the digital world started out of curiosity.
I once helped build a coffee shop actually —
discussing menus,
and eventually being trusted to create their website too.

Then I realized:
a website isn't just about code,
it's 'bout building experiences and character.

My other hobbies include pixel art,
visual storytelling,
and secretly have a strong interest
in Web3 interfaces &
future internet experiences.

#### Side Card
- Mini identity card
- FARMER </> COFFEE </> CODE
- Data:
    - Born in Kalimantan
    - Based in Semarang

Style:
dark futuristic card,
still subtle.

---

### 4. Skills Section

#### Heading
Things I build with.

#### Layout
- 2 kolom.

#### Data
Building With	         | Learning
-------------------------|----------
HTML	                 | Solidity
CSS	                     | ethers.js
JavaScript	             | Smart Contract UI
Vue 3	                 | Web3 UX
Tailwind CSS	         |
Git	                     |
Python	                 |

#### Style
- Building With:
    - solid border
    - brighter text
- Learning:
    - dashed border
    - muted text

#### Notes
- Fokus readability.
- Jangan terlalu banyak hover effect.

---

### 5. Projects Section

#### Heading
Selected Projects.

#### Subtext
A few things I've designed,
built,
and occasionally debugged at 2AM.

#### Layout
- Bento grid asimetris.

#### Prioritas:
- visual preview besar
- hierarchy jelas
- spacing lega

#### Projects

##### Naka Coffee
Landing page untuk coffee shop di Semarang
dengan pendekatan emotional branding
dan clean storytelling.

##### Tech:
HTML · CSS · JavaScript

##### Personal Portfolio
Cinematic portfolio with focus on
frontend interaction, typography,
dan visual rhythm.

##### Tech:
Vue 3 · Tailwind · Vite

##### Odin Recipes
Early project to understand
foundational HTML semantics
dan basic layout.

##### Tech:
HTML · CSS

#### Card Interaction

##### Hover:
- slight scale
- subtle border glow
- smooth transition

##### NO:
- excessive animation
- crazy tilt effect
- over-glow

---

### 6. Contact Section

#### Heading
Got an idea,
brand,
or weird project in mind?
Let's talk.

#### Subtext
I am open to freelance work,
landing pages,
frontend collaborations,
or just chatting about
internet & coffee.

#### Platforms
Email
GitHub
Telegram
Instagram

#### Style
#### Pill buttons
- subtle border
- smooth hover
- clean spacing

#### Subtext
Saya terbuka untuk freelance project,
landing page,
frontend collaboration,
atau sekadar ngobrol soal internet dan kopi.

#### Platforms
Email
GitHub
Telegram
Instagram

#### Style

- Pill buttons:
    - subtle border
    - smooth hover
    - clean spacing

---

### 7. Footer

#### Left
Built by BorgirRax.

#### Right
Frontend developer,
coffee enjoyer,
future internet enthusiast.

#### Bottom
© 2026 — Made with Vue & too much coffee.

---

### Animation Direction

#### Allowed
- fade-in
- stagger reveal
- smooth hover
- subtle glow
- soft parallax
- cursor follow (very subtle)

#### Avoid
- aggressive motion
- too many particles
- constant animation
- overuse blur/glow
- distracting transitions

#### Rule:
- Animation should support the content,
- not compete with it.

---

### SEO

#### Checklist:

- semantic HTML
- meta title & description
- Open Graph tags
- Twitter card
- sitemap
- robots.txt
- favicon
- optimized images
- descriptive alt text

---

### Deploy

#### Preview:
Netlify / Vercel

#### Final:
Custom domain.

---

### Goal

Portfolio ini harus terasa seperti:

- frontend developer yang punya taste, karakter, dan ngerti cara membuat website terasa hidup.

Bukan:

- developer yang menaruh semua efek visual sekaligus.

---

## Next Steps

1. Setup project Vue + Tailwind
2. Buat color palette & typography
3. Implement layout & components
4. Integrasikan konten & project
5. Review, polish, dan deploy

---

## Optional Ideas

- Mini pixel animation di logo
- Hover sound kecil
- Dark mode / light mode toggle
- easter egg tersembunyi
- Scroll progress indicator
- Custom cursor
- Responsive breakpoint testing
- Performance optimization

---

## Resources

- Vue 3 official docs
- Tailwind CSS docs
- Coolors.co
- Google Fonts
- UI gradients
- Microinteractions examples

---

## Notes

- Jangan copy template.
- Utamakan keunikan.
- Detail kecil menentukan.
- Jangan takut bereksperimen, tapi
tetap harus fungsional.

---

Happy coding!

---

## Progress

- [x] Diskusi desain & konten
- [x] Setup Vue 3 + Vite + Tailwind
- [x] Struktur komponen
- [x] NavBar
- [ ] HeroSection
- [ ] AboutSection
- [ ] SkillsSection
- [ ] ProjectsSection
- [ ] ContactSection
- [ ] Light mode toggle
- [ ] Animasi
- [ ] Deploy
