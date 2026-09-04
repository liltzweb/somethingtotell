# 𓏲 I Have Something to Tell You ♡
> An intimate, interactive romantic confession website crafted for **Frans Philoh** to confess his feelings to **Amaia Luna**.

[![Live Demo](https://img.shields.io/badge/Live_Demo-somethingtotell.netlify.app-BD4558?style=for-the-badge&logo=netlify&logoColor=white)](https://somethingtotell.netlify.app)
[![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge)](https://somethingtotell.netlify.app)
[![Responsive](https://img.shields.io/badge/Mobile--First-Responsive-FAF6F0?style=for-the-badge&colorA=2E1B1E&colorB=BD4558)](https://somethingtotell.netlify.app)
[![Audio](https://img.shields.io/badge/Web_Audio-Synthesized_Organic_SFX-black?style=for-the-badge&logo=webrtc&logoColor=white)](https://somethingtotell.netlify.app)

---

## ✦ Live Preview

🌐 **Website Link**: [https://somethingtotell.netlify.app](https://somethingtotell.netlify.app)  
💌 **Direct Telegram Response**: [https://t.me/mirssy](https://t.me/mirssy)

---

## ✦ About The Project

**“I Have Something to Tell You”** (`somethingtotell`) adalah website pengakuan perasaan (*romantic confession website*) interaktif yang didesain secara intim, hangat, dan personal. Berbeda dari template romantis umum yang klise, website ini dibangun dengan pendekatan bercerita (*storytelling experience*) yang mendalam, membimbing penerima melewati rangkaian surat emosional, foto kenangan polaroid 3D, dan pengakuan yang tulus.

### Detail Personalisasi:
- **Pengirim (Shooter)**: Frans Philoh
- **Penerima (Crush)**: Amaia Luna
- **Pertanyaan Inti**: *"will you be mine?"*
- **Tanda Tangan**: *— frans philoh*
- **Tujuan Respon**: [t.me/mirssy](https://t.me/mirssy) (Otomatis menyalin jawaban dan membuka obrolan Telegram)

---

## ✦ Alur Pengalaman & Fitur Utama

```text
[Step 1: Opening Card] ──> [Step 2: Layered Envelope] ──> [Step 3: Letter Part 1]
                                                                    │
[Step 6: Polaroid #2]  <── [Step 5: Letter Part 2]   <── [Step 4: Polaroid #1]
       │
       ▼
[Step 7: Final Confession & Proposal] ──> [Copy to Clipboard] ──> [Redirect to Telegram]
```

1. **Step 1 — Opening (Stationery Cover Card)**  
   Emblem bunga mawar vintage dengan judul yang mengundang: *"there’s something i’ve been wanting to tell you. and i don’t really know how to say it."*
2. **Step 2 — The Physical Layered Envelope**  
   Amplop surat berlapis vektor yang realistis, dilengkapi **vintage perforated postage stamp**, cap pos stempel pos udara (*"AIR MAIL · SPECIAL DELIVERY"*), dan sapaan tulisan tangan *"dear amaia luna,"*.
3. **Step 3 — Confession Letter Part 1 (Yearning & Tender)**  
   Kertas surat bergaris dengan watermark botanical flourish di sudut kertas, memuat satu paragraf mengalir penuh kerinduan dan apresiasi tulus atas kehadiran Amaia.
4. **Step 4 — Memory Polaroid #1 (3D Flip Card)**  
   Foto polaroid kenangan pertama berbingkai putih dengan tekstur selotip washi tape transparan. Saat ditekan, foto akan berputar 3D disertai efek suara klik dan menampilkan pesan rahasia di baliknya.
5. **Step 5 — Confession Letter Part 2 (Vulnerable & Sincere)**  
   Paragraf pengakuan yang lebih mendalam dan rentan mengenai keberanian untuk mengungkapkan perasaan yang telah lama disimpan.
6. **Step 6 — Memory Polaroid #2 (3D Flip Card)**  
   Foto polaroid kedua dengan interaksi flip 3D dan pesan tulisan tangan rahasia kedua.
7. **Step 7 — Final Confession & The Proposal**  
   Kalimat penutup dengan tanda tangan *— frans philoh*, disusul pertanyaan:
   > **"will you be mine?"**
8. **Interactive Typographic Answers (Zero Emojis)**  
   - Tombol pilihan: **`YES, I WILL BE YOURS`** atau **`NO, SORRY`**.
   - Ketika ditekan, jawaban otomatis tersalin ke clipboard, notifikasi halus (*toast*) muncul, dan penerima secara otomatis dialihkan ke Telegram Frans Philoh (**`https://t.me/mirssy`**).
9. **Organic Sound Design (Web Audio API)**  
   - Efek suara bawaan yang disintesis secara real-time di browser (suara gesekan kertas, membuka amplop, memutar foto polaroid, dan nada konfirmasi).
   - **Tanpa tombol toggle musik yang mengganggu.** Suara hanya berbunyi secara alami saat ada interaksi fisik.

---

## ✦ Struktur Repositori

```text
SOMETHINGTOTELL/
│
├── index.html              # Struktur utama & markup semantik pengalaman interaktif
├── README.md               # Dokumentasi lengkap proyek & panduan deploy
│
├── css/
│   └── style.css           # Desain visual velvet rose, tipografi editorial, 3D flip, responsive layout
│
├── js/
│   ├── config.js           # PENGATURAN UTAMA: nama, teks surat, foto, pesan rahasia & link chat
│   ├── audio.js            # Generator sound effects organik berbasis Web Audio API
│   └── app.js              # Logika transisi layar, interaksi flip foto, clipboard & navigasi
│
└── assets/
    └── photos/
        ├── photo-1.jpg     # Foto polaroid kenangan 1 (Cafe hangat)
        └── photo-2.jpg     # Foto polaroid kenangan 2 (Evening walk)
```

---

## ✦ Panduan Kustomisasi

Seluruh isi konten teks, nama, dan link tujuan dapat diubah dengan sangat mudah melalui satu file konfigurasi: [`js/config.js`](file:///d:/LILTZ/SOMETHINGTOTELL/js/config.js).

### 1. Mengubah Identitas & Link Telegram
Buka `js/config.js` dan sesuaikan variabel berikut:
```javascript
const CONFIG = {
  senderName: "frans philoh",
  recipientName: "amaia luna",
  chatLink: "https://t.me/mirssy", // Ganti dengan link Telegram kamu
  // ...
};
```

### 2. Mengganti Foto Polaroid
1. Siapkan 2 foto dengan rasio **4:5** (portrait) atau **1:1** (square).
2. Simpan foto ke dalam folder `assets/photos/` dengan nama:
   - `assets/photos/photo-1.jpg` (foto pertama)
   - `assets/photos/photo-2.jpg` (foto kedua)
3. Pesan di balik foto dapat disesuaikan pada bagian `photo1.message` dan `photo2.message` di `js/config.js`.

---

## ✦ Cara Publikasi Online (Deployment)

### Opsi A: Netlify (Direkomendasikan — Sama Seperti Demo)
Website ini saat ini aktif di [somethingtotell.netlify.app](https://somethingtotell.netlify.app). Untuk mendeploy versimu sendiri:
1. Buka [app.netlify.com/drop](https://app.netlify.com/drop).
2. Seret dan lepas (*drag & drop*) seluruh folder `SOMETHINGTOTELL`.
3. Dalam hitungan detik website akan langsung online.
4. Kamu dapat mengubah nama subdomain (misal `somethingtotell.netlify.app`) di menu **Site configuration > Change site name**.

### Opsi B: GitHub Pages
1. Buat repository baru di [GitHub](https://github.com/new) bernama `somethingtotell`.
2. Upload semua file dan folder (`index.html`, `css/`, `js/`, `assets/`, `README.md`) ke repository tersebut:
   ```bash
   git init
   git add .
   git commit -m "feat: initial commit of romantic confession website"
   git branch -M main
   git remote add origin https://github.com/<username>/somethingtotell.git
   git push -u origin main
   ```
3. Buka tab **Settings** di repository GitHub kamu.
4. Di panel sebelah kiri, pilih menu **Pages**.
5. Pada bagian **Build and deployment > Branch**, pilih branch `main` dan folder `/ (root)`.
6. Klik **Save**. Dalam 1–2 menit website akan live di:
   ```text
   https://<username>.github.io/somethingtotell/
   ```

---

## ✦ Teknologi & Desain Sistem

- **Tipografi**:
  - *Display / Serif*: [Playfair Display](https://fonts.google.com/specimen/Playfair+Display) (Elegan, puitis, dan berjiwa klasik)
  - *Body / Sans*: [Plus Jakarta Sans](https://fonts.google.com/specimen/Plus+Jakarta+Sans) (Modern, hangat, dan sangat nyaman dibaca di layar ponsel)
- **Color Palette (Velvet Rose & Soft Linen)**:
  - Cream Canvas: `#FAF6F0`
  - Velvet Rose Accent: `#BD4558`
  - Soft Petal Blush: `#F4CCD1`
  - Espresso Berry Ink: `#2E1B1E`
  - Muted Mauve Stone: `#82666A`
  - Vintage Parchment Border: `#EFE4D6`
- **Zero Framework & Zero Dependencies**: Murni HTML5, CSS3, dan Vanilla JavaScript ringan tanpa beban loading library eksternal.
- **Audio Sintesis**: Menggunakan **Web Audio API** native browser, memastikan audio selalu dapat diputar tanpa ketergantungan file MP3 eksternal.

---

## ✦ Catatan Privasi & Penggunaan

- Website ini bersifat statis dan aman. Jawaban penerima tidak disimpan di server pihak ketiga mana pun, melainkan disalin langsung ke clipboard perangkat mereka dan diarahkan secara pribadi ke chat Telegram yang telah ditentukan.
- Desain dan konten orisinal dipersembahkan dengan ketulusan dan kehangatan oleh @liltz / catamourie.

---
<p align="center">
  <i>crafted with sincerity & warmth for frans philoh & amaia luna ♡</i>
</p>
