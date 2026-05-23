---
name: jimy. Cinematic Design System
description: Visual system for jimy's playful, techy, and cinematic developer portfolio.
colors:
  primary: "#4a9ecc"
  neutral-bg: "#0f1721"
  neutral-card: "#0a0f18"
  ice-blue: "#d4eeff"
  soft-navy: "#152232"
  dark-navy: "#060c14"
  accent-white: "#f0f8ff"
  text-muted: "#7ec4e8"
typography:
  display:
    fontFamily: "Poppins, sans-serif"
    fontSize: "clamp(2rem, 5vw, 3.2rem)"
    fontWeight: 700
    lineHeight: "1.2"
    letterSpacing: "-0.03em"
  body:
    fontFamily: "Poppins, sans-serif"
    fontSize: "1rem"
    fontWeight: 400
    lineHeight: "1.8"
  label:
    fontFamily: "JetBrains Mono, monospace"
    fontSize: "0.85rem"
    fontWeight: 500
    lineHeight: "1.5"
    letterSpacing: "0.05em"
rounded:
  sm: "6px"
  md: "12px"
  lg: "24px"
  full: "9999px"
spacing:
  xs: "4px"
  sm: "8px"
  md: "16px"
  lg: "24px"
  xl: "56px"
  xxl: "96px"
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.dark-navy}"
    rounded: "{rounded.md}"
    padding: "12px 24px"
  button-secondary:
    backgroundColor: "transparent"
    textColor: "{colors.primary}"
    rounded: "{rounded.md}"
    padding: "12px 24px"
  chip-speak:
    backgroundColor: "transparent"
    textColor: "{colors.accent-white}"
    rounded: "{rounded.full}"
    padding: "6px 14px"
  chip-loading:
    backgroundColor: "transparent"
    textColor: "{colors.text-muted}"
    rounded: "{rounded.full}"
    padding: "6px 14px"
---

# Design System: jimy. Cinematic Design System

## 1. Overview

**Creative North Star: "The Minimalist Cine-Slate"**

Sistem desain ini merangkum suasana sinematik yang tenang, berkarakter, dan sangat memperhatikan keterbacaan serta spasi kosong (`spacing`). Kami menghindari penumpukan semua efek visual sekaligus dan menggantinya dengan keindahan tipografi Poppins tebal berspasi rapat, latar belakang pekat yang teduh, spasi antarkomponen yang lapang, serta interaksi penunjuk arah yang super halus. Ini adalah ruang digital yang hidup dan membuktikan kepiawaian desainer pengembang.

**Key Characteristics:**
- **Cinematic Rhythm**: Spasi kosong yang lega (`xl` dan `xxl`) serta ukuran display font tebal berspasi rapat untuk sensasi bioskop.
- **Low-Opacity Grid**: Garis petak latar belakang tipis berpiksel rendah yang menyatu lembut dengan background gelap.
- **Subtle Interactions**: Animasi yang sangat minim, glow redup maksimal 1x per section, kursor dengan inersia lag gerakan yang lembut.

## 2. Colors

Atmosfer gelap malam pekat yang hening dibentuk dari gradasi warna malam pekat yang disesuaikan secara berhati-hati. Biru aksen dipakai secara sangat langka dan berharga.

### Primary
- **Primary Blue** (`#4A9ECC`): Warna biru aksen krusial, digunakan secara eksklusif hanya untuk elemen aksi terpenting dan titik fokus utama.

### Neutral
- **Background** (`#0F1721`): Kegelapan malam yang lapang dan sejuk sebagai basis antarmuka.
- **Surface / Card** (`#0A0F18`): Latar belakang bento card proyek, menyatu halus di atas background.
- **Soft Navy** (`#152232`): Digunakan untuk garis pembatas solid atau dashed tipis.
- **Dark Navy** (`#060C14`): Warna terdalam, pembungkus tombol toggle.
- **Accent White** (`#F0F8FF`): Putih kebiruan terang berdaya kontras tinggi untuk kenyamanan membaca.
- **Teks Muted** (`#7EC4E8`): Biru muda teduh untuk label informasi sekunder.

### Named Rules
**The Single-Glow Rule.** Efek bersinar (glow) hanya boleh muncul maksimal 1 kali dalam satu section utuh saat elemen disorot, dengan kepekatan sangat rendah (`opacity: 0.08` atau kurang) agar tidak mengaburkan teks.

## 3. Typography

**Display Font:** Poppins (dengan fallback sans-serif)  
**Body Font:** Poppins (dengan fallback sans-serif)  
**Label/Mono Font:** JetBrains Mono (dengan fallback monospace)  

Seluruh judul dan paragraf disatukan di bawah keluarga font Poppins. Judul menggunakan gaya super tebal (Bold) dengan spasi huruf yang dirapatkan (tight letter-spacing), sementara teks body dibiarkan berspasi lapang dengan `line-height: 1.8` dan batas lebar kolom `65ch` demi estetika majalah modern.

### Hierarchy
- **Display** (`Poppins 700`, `clamp(2rem, 5vw, 3.2rem)`, `1.2`, `-0.03em`): Judul utama Hero.
- **Headline** (`Poppins 700`, `clamp(1.5rem, 3.5vw, 2.2rem)`, `1.3`, `-0.02em`): Judul-judul section.
- **Title** (`Poppins 600`, `1.2rem`, `1.4`): Judul Bento Card.
- **Body** (`Poppins 400`, `1rem`, `1.8`, `max-width: 65ch`): Narasi biografi, paragraf pendukung, penjelasan proyek.
- **Label** (`JetBrains Mono 500`, `0.85rem`, `1.5`, `uppercase`): Chip keahlian, teknologi proyek.

### Named Rules
**The Airy Measure Rule.** Semua kolom teks paragraf wajib memiliki batas lebar maksimal `65ch` (sekitar 60-70 karakter per baris) agar mata pengunjung tidak lelah saat membaca.

## 4. Elevation

Sistem ini flat secara rest. Tidak ada bayangan 3D yang mengambang. Struktur antarmuka digambarkan secara presisi lewat border tipis berwarna Soft Navy (`#152232`).

### Shadow Vocabulary
- **Subtle Glow Accent** (`box-shadow: 0 0 25px rgba(74, 158, 204, 0.08)`): Pendaran sangat tipis yang muncul sebagai respons hover pada Bento Card proyek.

### Named Rules
**The Border-Led Depth Rule.** Kedalaman visual hanya digambarkan lewat garis pembatas 1px berwarna `#152232`. Bayangan tebal dilarang keras.

## 5. Components

### Buttons
- **Shape:** Sudut tumpul sedang (12px radius).
- **Primary:** Solid `#4A9ECC`, teks `#060C14` tebal. Hover: bergeser ke atas 1.5px dengan transisi lambat, pendaran glow ultra tipis.
- **Secondary:** Transparent, border `#152232`, teks `#4A9ECC`. Hover: border `#4A9ECC`, teks `#F0F8FF`.

### Chips
- **Building With:** Border solid `#152232` (1px), teks `#F0F8FF` (cerah), background transparan.
- **Learning:** Border putus-putus `#152232` (1px), teks `#7EC4E8` (redup), background transparan.

### Bento Cards
- **Corner Style:** Radius lebar 24px (`rounded-3xl` kustom).
- **Background:** `#0A0F18`.
- **Border:** Solid `#152232`. Hover berubah ke `#4A9ECC` dengan bayangan glow ultra redup.
- **Sizing:** Pratinjau visual besar dengan hierarchy asimetris yang lega.

### Navigation (NavBar)
- **Style:** Sticky minimalis, tinggi tetap (64px) yang tipis dan tidak dominan, latar belakang semi-transparan dengan filter blur backdrop (`backdrop-filter: blur(8px)`).
- **Links:** Font Poppins 0.9rem, teks `#7EC4E8`. Hover: berubah menjadi `#F0F8FF`.

## 6. Do's and Don'ts

### Do:
- **Do** atur garis grid latar belakang dengan opacity super rendah (`opacity-3` atau `opacity-5`) agar hanya terlihat samar.
- **Do** pastikan custom kursor memiliki jeda inersia lag gerakan yang lembut untuk rasa cinematic.
- **Do** gunakan batas kolom `max-width: 65ch` pada paragraf utama About.

### Don't:
- **Don't** gunakan terlalu banyak partikel melayang, efek neon berlebih, atau hiasan dekoratif yang membuat situs terlihat berisik.
- **Don't** gunakan bayangan hitam tebal konvensional; pertahankan layout bersih.
- **Don't** buat grid Bento berskala simetris; susun 3 proyek secara asimetris dengan spasi lega.
- **Don't** biarkan teks paragraf berjalan terlalu panjang melampaui lebar kolom baca ideal.
