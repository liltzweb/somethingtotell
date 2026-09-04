# 🎟️ TUMBLRONE ✦ Order Form & Tumblr Feed Website Documentation

> **Website Digital Gift & Interactive Tumblr Dashboard Feed for Couples**  
> *Harga Template / Jasa:* **Rp 10.000**  
> *Desain & Kode:* `@liltz` / Catamourie  
> *Live Form Pemesanan:* [`form.html`](form.html) atau via Telegram [`t.me/mirssy`](https://t.me/mirssy)

`tumblrone` adalah template website perayaan hubungan (mensive, anniversary, birthday, atau private love confession) dengan konsep **Tumblr Dashboard Feed (Midnight Blue)** yang estetik, modern, romantis, dan bebas dari klise AI (*anti-slop*).

Website ini membawa pasanganmu menyusuri 5 postingan dashboard Tumblr yang penuh interaksi personal: mulai dari masterpost pembuka, daftar hal favorit interaktif (*tap-to-reveal*), polling Tumblr yang membuka potret candid tercantik, garis waktu 3 bulan interaktif, hingga surat cinta penutup yang hangat dan mengalir.

---

## ✨ Alur Interaktif 5 Postingan Tumblr (User Journey)

1. **Post 01 — Masterpost Cover (`#scene-entry`)**  
   Postingan pembuka arsip privat dengan kutipan romantis berbobot (*"made this whole page because you somehow made my whole world so much softer."*), foto tatapan pembuka (`photo-entry.jpg`), dan tombol untuk membuka 4 arsip berikutnya.
2. **Post 02 — The Favorites List (`#scene-list`)**  
   Postingan daftar 4 hal favorit (*evidence items*) yang bisa diklik satu per satu untuk membuka rahasia manis (termasuk *"person i'd choose over and over again"* → *"keisha!!!"*), dilengkapi foto candid menggemaskan (`photo-list.jpg`).
3. **Post 03 — Tumblr Poll & Portrait Reveal (`#scene-quiz`)**  
   Polling interaktif bergaya khas Tumblr (*"who is literally all i think about lately?"*). Saat pasangan memilih opsi, persentase suara (98.4%) langsung terisi dan seketika membuka potret foto tercantik dirinya (`photo-01.jpg`).
4. **Post 04 — 3 Months Timeline Stepper (`#scene-counter`)**  
   Garis waktu bulanan interaktif (Bulan 01, Bulan 02, Bulan 03) yang bisa diklik bertahap hingga membuka kartu perayaan milestone hari ini (*"03 MONTHS WITH YOU"*) dan foto kencan malam yang hangat (`photo-02.jpg`).
5. **Post 05 — Final Love Note & Confession (`#scene-final`)**  
   Pengakuan penutup terverifikasi (*"VERIFIED TRUTH"* → *"keisha!"*) yang menyajikan surat cinta tulus tanpa tombol tersembunyi, ditutup dengan foto berpelukan manis (`photo-final.jpg`) dan tanda tangan Keith.
6. **Fitur Tambahan — Tumblr Drawer Komentar & Auto-Reply**  
   Setiap postingan dilengkapi tombol *Notes/Comments*. Pasangan bisa mengetik komentar apa saja dan sistem akan merespon dengan balasan manis (*Keith's auto-reply*) yang nyambung secara natural.
7. **Fitur Audio — Web Audio API Synthesizer**  
   Efek suara prosedural yang lembut saat menyukai postingan (*heart pop*), memilih polling, dan melangkah di timeline (bebas lag, native tanpa file MP3 eksternal).

---

## 🎨 Tipografi & Palet Warna Aktif

* **Display & Title**: `Favorit`, `-apple-system`, `BlinkMacSystemFont`, `Helvetica Neue`, sans-serif (Khas UI Tumblr modern)
* **Body / Text**: Inter / Sans-serif geometris
* **Accents & Notes**: Italic Serif & Monospace tech

### 💙 Palet Warna Tumblr Midnight Blue
* **Background (Canvas)**: `#001935` (Deep Navy Tumblr)
* **Post Card / Surface**: `#0A2540` / `#001935`
* **Primary Text**: `#FFFFFF`
* **Secondary / Faded Text**: `#8B98A5` / `#94A3B8`
* **Tumblr Blue Accent**: `#00B8FF` (Hover: `#38C9FF`)
* **Love / Heart Red**: `#FF492F`
* **Border & Dividers**: `#1C2631`

---

## 📸 Panduan Memasang 7 Foto (Assets)

Letakkan 7 file foto di folder `assets/` dengan nama dan spesifikasi berikut:

| Foto | Lokasi & Nama File | Format / Rasio Rekomendasi | Keterangan |
| :--- | :--- | :--- | :--- |
| **Avatar Pembuat** | `assets/avatar-keith.jpg` | 1:1 Persegi (500×500 px) | Foto profil Keith (`Keith.` / `@keonho`) |
| **Avatar Pasangan** | `assets/avatar-keisha.jpg` | 1:1 Persegi (500×500 px) | Foto profil Keisha (`keisha!` / `@kya`) |
| **Foto Post 1** | `assets/photo-entry.jpg` | 4:5 Portrait (800×1000 px) | Foto tatapan manis / cover masterpost |
| **Foto Post 2** | `assets/photo-list.jpg` | 4:5 Portrait (800×1000 px) | Foto candid makan snack / pizza di sofa |
| **Foto Post 3** | `assets/photo-01.jpg` | 4:5 Portrait (800×1000 px) | Foto solo tercantik hasil polling |
| **Foto Post 4** | `assets/photo-02.jpg` | 4:5 Portrait (800×1000 px) | Foto kencan malam / lampu hangat |
| **Foto Post 5** | `assets/photo-final.jpg` | 4:5 Portrait (800×1000 px) | Foto merentangkan tangan / pelukan |

> **Tips:** Gunakan format file `.jpg` atau `.jpeg` dengan ukuran kompresi yang baik agar loading website cepat di semua perangkat.

---

## 📝 Cara Kustomisasi Konten (`script.js`)

Semua data teks, judul, caption foto, nama akun, dan isi surat cinta disimpan dalam satu objek konfigurasi:
👉 **[`script.js`](script.js)** pada variabel **`siteData`**:

```javascript
const siteData = {
  // Identitas Akun Tumblr
  senderName: "Keith.",
  senderShort: "keith",
  senderHandle: "@keonho",
  senderAvatar: "assets/avatar-keith.jpg",

  recipientName: "keisha!",
  recipientShort: "keisha",
  recipientHandle: "@kya",
  recipientAvatar: "assets/avatar-keisha.jpg",

  dateFormatted: "September 1, 2026",
  occasion: "3 Months / Mensive",

  // Post 01 - Masterpost Cover
  entry: {
    title: "KEITH'S FAVORITES",
    subtitle: "a ridiculously biased list.",
    quote: "“made this whole page because you somehow made my whole world so much softer.”",
    photoCaption: "the face that started it all, still my favorite view"
  },

  // Post 02 - The List (4 Items Reveal)
  listScene: {
    title: "THE LIST",
    sublabel: "the person behind every single good thing lately",
    items: [
      { id: "01", prompt: "person i text the second i wake up", reveal: "you, obviously." },
      { id: "02", prompt: "person whose snacks i always share", reveal: "still you." },
      { id: "03", prompt: "person i miss even when you just left", reveal: "you already knew that." },
      { id: "04", prompt: "person i'd choose over and over again", reveal: "keisha!!!" }
    ],
    photoCaption: "eating pizza and looking this cute should actually be illegal"
  },

  // Post 03 - Tumblr Poll
  quizScene: {
    question: "who is literally all i think about lately?",
    options: [
      { key: "keisha!", label: "keisha!", percentage: "98.4%", response: "obviously." },
      { key: "someone_else", label: "someone else", percentage: "0.8%", response: "be serious right now." },
      { key: "no_idea", label: "no idea tell me", percentage: "0.8%", response: "as if you don't already know." }
    ],
    resolutionTitle: "it's keisha!",
    photoCaption: "the prettiest girl in my camera roll, no competition"
  },

  // Post 04 - 3 Months Timeline Stepper
  counterScene: {
    steps: [
      { count: 1, display: "01", microcopy: "the day everything started making sense." },
      { count: 2, display: "02", microcopy: "falling for you a little more every day." },
      { count: 3, display: "03", microcopy: "still us, and you still light up every room you're in." }
    ],
    milestoneBadge: "03 MONTHS WITH YOU",
    milestoneDate: "SEPTEMBER 01, 2026",
    photoCaption: "three months of late night dates and i still get butterflies"
  },

  // Post 05 - Final Love Note
  finalScene: {
    question: "who's the only one keith will ever want?",
    acceptedAnswer: "keisha!",
    finalLines: [
      "happy 3 months, keisha!",
      "you're my favorite person in the entire world, hands down.",
      "Keith."
    ],
    photoCaption: "always running straight into my arms, forever my favorite person"
  }
};
```

---

## 📋 Formulir Pemesanan (`form.html`)

Website ini dilengkapi dengan formulir pemesanan online bergaya tiket: **[`form.html`](form.html)**.

### Fitur Formulir:
1. **Sistem Kalkulasi Harga Otomatis**:
   * Harga Dasar: **Rp 10.000**
   * Custom Color Palette (Recolor): **+Rp 2.000**
   * Rush Fee (Selesai dalam 24 Jam): **+Rp 4.000**
2. **Validasi Lengkap**: Form menandai kolom yang belum terisi dan menggulir otomatis ke kolom tersebut.
3. **Kirim Pesanan Otomatis ke Telegram**:
   * Menekan tombol **`submit`** akan menyalin rekap teks pesanan ke *clipboard* dan langsung membuka chat Telegram **`t.me/mirssy`**. Pembeli tinggal *paste* dan melampirkan 7 foto langsung di chat.

---

## 🚀 Cara Menjalankan & Deploy Website

### 1. Menjalankan di Komputer / Laptop Lokal
Cukup klik ganda file `index.html` untuk membuka langsung di Google Chrome / browser apa pun, atau jalankan server lokal:
```bash
# Python
python -m http.server 3000

# Node.js
npx serve .
```

### 2. Deploy Online Gratis ke Netlify (Direkomendasikan)
1. Buka [Netlify Drop](https://app.netlify.com/drop).
2. Seret (*drag-and-drop*) folder **`TUMBLRONE`** ke area browser.
3. Masuk ke **Site configuration** → **Change site name** untuk menentukan link custom (misal: `keonho-kya.netlify.app`).

---

## 📂 Struktur File Proyek

```text
TUMBLRONE/
├── index.html           # Website utama feed Tumblr interaktif
├── form.html            # Formulir pemesanan online bergaya tiket (Rp 10.000)
├── style.css            # Styling tema Tumblr Midnight Blue & Mobile Responsive
├── script.js            # Engine logika 5 postingan, data siteData & auto-reply
├── README.md            # Dokumentasi lengkap proyek
└── assets/              # Tempat menyimpan 7 foto
    ├── avatar-keith.jpg # Foto profil pembuat (Keith. / @keonho)
    ├── avatar-keisha.jpg# Foto profil pasangan (keisha! / @kya)
    ├── photo-entry.jpg  # Foto post 1 (cover masterpost)
    ├── photo-list.jpg   # Foto post 2 (daftar favorit / candid)
    ├── photo-01.jpg     # Foto post 3 (hasil polling)
    ├── photo-02.jpg     # Foto post 4 (momen 3 bulan)
    └── photo-final.jpg  # Foto post 5 (penutup / pelukan)
```

---

## 🏷️ Lisensi & Hak Cipta
Didesain dan dikembangkan oleh Catamourie (`@liltz`). Template ini dijual dengan harga **Rp 10.000**. Dilarang memperjualbelikan ulang atau mendistribusikan ulang kode ini tanpa izin.