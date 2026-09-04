# 𓏲 somethingtotell ‧ order form & website ♡

> **SOMETHINGTOTELL** adalah katalog website interaktif bertema *"i have something to tell you"* (romantic confession website & proposal) karya [@liltz](https://t.me/mirssy) / **catamourie**. Repositori ini memuat source code website utama serta halaman **Order Form** resmi yang siap dideploy ke GitHub Pages / Netlify.

---

## 📌 Demo & Live Links

- **Live Website**: [https://somethingtotell.netlify.app](https://somethingtotell.netlify.app)
- **Form Pemesanan**: `https://<username>.github.io/somethingtotell/form.html` (atau rename ke `index.html` jika repo khusus form)
- **Website Utama**: `https://<username>.github.io/somethingtotell/` (atau [somethingtotell.netlify.app](https://somethingtotell.netlify.app))
- **Official Telegram**: [@mirssy](https://t.me/mirssy)

---

## 💸 Struktur Harga (Pricing)

- **Harga Dasar (Base Website)**: `Rp7.000`
- **Recolor Custom Color Palette**: `+Rp2.000`
- **Rush Fee (Deadline <24 Jam)**: `+Rp4.000`
- **Metode Pembayaran**: QRIS (No Rate Fee)

---

## 🎨 Color Palette Default (Velvet Rose & Soft Linen)

| Warna | Hex Code | Deskripsi |
| :--- | :--- | :--- |
| **Cream Linen** | `#FAF6F0` | Background utama & kertas surat |
| **Velvet Rose** | `#BD4558` | Warna aksen utama / wax seal & tombol |
| **Soft Petal** | `#F4CCD1` | Background badge / border halus / glow |
| **Berry Espresso** | `#2E1B1E` | Teks utama dan elemen kontras tinggi |
| **Muted Mauve** | `#82666A` | Teks sekunder, label, & garis halus |
| **Parchment Line** | `#EFE4D6` | Garis pembatas lipatan amplop & tekstur |

---

## ✨ Fitur Order Form (`form.html`)

1. **Ticket Stub Header**:
   - Tampilan tiket estetik dengan perforasi garis putus-putus.
   - Total harga terkalkulasi secara otomatis dan real-time (`Rp7.000` base).

2. **Validasi & Color Picker Dinamis**:
   - Pilihan recolor interaktif dengan 6 color picker terhubung ke input kode HEX.
   - Validasi format HEX regex otomatis (`#RRGGBB`).

3. **12 Bagian Form Terstruktur**:
   - `00` ୵ **Customer Identity** (Nama, Username Telegram, QRIS, Tanggal Deadline, Checkbox Rush Fee).
   - `01` ୵ **Custom Color Palette** (Pilihan no/yes + 6 color picker & hex input).
   - `02` ୵ **Core Identity** (Nama Penembak / Pengirim, Panggilan Pengirim, Nama Crush / Penerima, Panggilan Penerima, Link Telegram Respon).
   - `03` ୵ **Step 1 — Opening** (Stationery Card: Judul headline, subteks prompt, label tombol pembuka).
   - `04` ୵ **Step 2 — The Envelope** (Instruksi buka amplop, sapaan di dalam surat amplop, tombol buka surat).
   - `05` ୵ **Step 3 — Confession Letter Part 1** (Salutation header, isi paragraf mengalir penuh kerinduan & apresiasi tulus, tombol lanjut).
   - `06` ୵ **Step 4 — Photo Memory 01** (Instruksi tap foto polaroid 3D, caption depan foto, pesan tulisan tangan rahasia di balik foto, tombol lanjut).
   - `07` ୵ **Step 5 — Confession Letter Part 2** (Salutation kelanjutan, isi paragraf pengakuan rentan & niat tulus, tombol lanjut).
   - `08` ୵ **Step 6 — Photo Memory 02** (Instruksi tap polaroid ke-2, caption depan foto, pesan rahasia di balik foto ke-2, tombol lanjut).
   - `09` ୵ **Step 7 — Final Confession & Proposal** (Lead quote, kalimat penutup cinta, tanda tangan penembak, jeda, pertanyaan pengakuan *"will you be mine?"*, tombol pilihan *"YES, I WILL BE YOURS"* & *"NO, SORRY"*).
   - `10` ୵ **Lampiran Foto & Musik** (Catatan instruksi melampirkan 2 foto portrait/square & 1 lagu format .mp3 langsung via Telegram).
   - `11` ୵ **Link Website** (Judul tab browser, 2 pilihan custom subdomain `.netlify.app`).

4. **Satu Klik Salin & Buka Telegram**:
   - Validasi input wajib.
   - Merangkum form ke dalam teks rapi dengan simbol unicode (`𓏲 somethingtotell form ♡`).
   - Teks otomatis tersalin ke clipboard pengguna.
   - Membuka link `https://t.me/mirssy?text=...` dengan teks pesanan terisi otomatis.

---

## 📁 Struktur File

```text
SOMETHINGTOTELL/
├── index.html          # Website interaktif utama SOMETHINGTOTELL (7 Step Confession)
├── form.html           # Halaman Form Pemesanan SOMETHINGTOTELL (Harga 7k)
├── order.html          # Salinan form.html (opsi routing alternatif)
├── README.md           # Dokumentasi repositori
├── css/
│   └── style.css       # Styling CSS lengkap & responsif mobile/desktop
├── js/
│   ├── config.js       # Konfigurasi data konten, nama Frans & Amaia, chat Telegram, audio
│   ├── audio.js        # Web Audio API procedural SFX & Background Music Player
│   └── app.js          # Logika transisi, flip polaroid 3D, auto-copy & redirect, tombol back
└── assets/
    ├── audio/          # Tempat file musik latar belakang
    │   └── music.mp3   # File lagu MP3 kamu (rename jadi music.mp3)
    └── photos/         # Foto polaroid kenangan 1 & 2
        ├── photo-1.jpg
        └── photo-2.jpg
```

---

## 🎵 Panduan Menambahkan Musik Latar (Background Music)

Untuk menambahkan musik latar ke website pengakuan:
1. Siapkan file lagu favorit berformat **`.mp3`**.
2. Masukkan file tersebut ke dalam folder:  
   📂 **`assets/audio/`**
3. Ganti nama filenya (*rename*) menjadi:  
   📄 **`music.mp3`**  
   *(Sehingga letak path-nya adalah: `assets/audio/music.mp3`)*
4. Musik akan **otomatis mulai berputar** lembut (*smooth fade-in*) saat penerima menekan tombol pembuka / amplop surat, dan penerima juga dapat memutar/menjeda musik melalui tombol piringan hitam (*vinyl disc*) di pojok kanan atas.
5. Pengaturan volume, putar berulang (*loop*), atau ganti path file dapat diatur kapan saja di [`js/config.js`](file:///d:/LILTZ/SOMETHINGTOTELL/js/config.js) pada bagian `music`.

---

## 🚀 Cara Upload & Hosting ke GitHub Pages

### Opsi A: Menggabungkan Website & Form dalam Satu Repositori
1. Push semua file repositori ini ke GitHub (`main` branch).
2. Buka repository di GitHub -> Masuk ke tab **Settings** -> **Pages**.
3. Pada bagian **Build and deployment**, pilih:
   - **Source**: `Deploy from a branch`
   - **Branch**: `main` / `/ (root)`
4. Klik **Save**.
5. Website kamu akan aktif di:
   - Website Utama: `https://<username>.github.io/<repo-name>/` (atau deploy di Netlify: `https://somethingtotell.netlify.app`)
   - Form Pemesanan: `https://<username>.github.io/<repo-name>/form.html`

### Opsi B: Khusus Halaman Form Saja (seperti `liltzweb.github.io/somethingtotell/`)
1. Jika repositori ini ditujukan **khusus** untuk form pemesanan:
   - Rename `form.html` menjadi `index.html`.
2. Push ke GitHub dan aktifkan GitHub Pages.
3. Form akan langsung terbuka di `https://<username>.github.io/<repo-name>/`.

---

## 📜 Terms & Conditions

1. Seluruh desain, kode, dan konten adalah hak cipta **catamourie** / [@liltz](https://t.me/mirssy).
2. Dilarang mendistribusikan ulang, menjual ulang kode mentah, atau mengklaim kepemilikan desain tanpa izin.
3. Pemesanan resmi hanya melalui Telegram: [@mirssy](https://t.me/mirssy).

---

<div align="center">
  <sub>crafted with care by @liltz ‧ thank you for trusting somethingtotell ♡</sub>
</div>
