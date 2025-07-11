# Simple Portfolio Template

Selamat datang di **Simple Portfolio Template**, sebuah template portofolio single-page yang interaktif, modern, dan sepenuhnya dapat dikustomisasi. Dibuat dengan HTML, CSS, dan JavaScript murni, template ini dirancang untuk menampilkan profil profesional, proyek, keahlian, dan perjalanan karirmu dengan cara yang menarik dan dinamis.

Cek contoh live 👉 [https://dgxoportfolio.netlify.app/](https://dgxoportfolio.netlify.app/)

## ✨ Fitur Utama

  - **Desain Modern**: Tampilan kartu kaca (*glassmorphism*) dengan latar belakang partikel ASCII yang interaktif.
  - **Sepenuhnya Responsif**: Tampilan optimal di berbagai perangkat, dari desktop hingga *mobile*.
  - **Kustomisasi Mudah**: Semua data (teks, keahlian, proyek, dll.) terpusat dalam satu objek JavaScript untuk kemudahan modifikasi.
  - **Tema Ganda**: Beralih antara mode terang (*light mode*) dan gelap (*dark mode*) dengan sekali klik.
  - **Multi-Bahasa**: Dukungan bawaan untuk Bahasa Inggris (EN) dan Indonesia (ID).
  - **Interaktif & Dinamis**:
      - Animasi halus pada transisi antar bagian.
      - Bagian "Universe" untuk menampilkan pratinjau situs lain (misal: web utama, toko, API).
      - Kuis interaktif untuk menentukan "Profil Teknologi" pengunjung.
      - Sistem penyaringan sertifikasi berdasarkan lembaga penerbit.
      - Tampilan *timeline* visual untuk perjalanan karir atau pembelajaran.
  - **Fitur Tersembunyi**:
      - **Command Palette (`Ctrl+K`)**: Navigasi cepat ke semua bagian, ganti tema, atau ganti bahasa.
      - **Terminal Easter Egg**: Aktifkan dengan Konami Code (`↑↑↓↓←→←→BA`) untuk menampilkan terminal rahasia.
      - **Secure Broadcast**: Fitur untuk mengirim pesan "terenkripsi" (simulasi) melalui modal khusus.

-----

## 🚀 Cara Menggunakan

Menggunakan *template* ini sangat mudah. Anda hanya perlu mengedit file `index.html`.

### 1. Struktur File

Pastikan Anda memiliki file dan folder berikut:

```
/
├── index.html       # File utama yang akan Anda edit
└── logo.png         # Foto profil atau logo Anda
```

### 2. Ganti Logo

Ganti file `logo.png` yang ada dengan foto profil atau logo Anda. Pastikan nama filenya tetap `logo.png` dan berada di direktori yang sama dengan `index.html`. Ukuran ideal adalah gambar persegi (misalnya 500x500 piksel).

### 3. Edit Data Pribadi

Buka file `index.html` dan cari bagian `<script>`. Di dalamnya, Anda akan menemukan area yang ditandai dengan komentar `✨ EDIT DATA DI SINI ✨`. Inilah pusat data untuk seluruh portofolio Anda.

#### Nama dan Kontak

  - **Nama**: Ubah `"Your Name"` di dalam `<h1>` HTML.
    ```html
    <h1 class="card-fullname">Dika-Kun</h1>
    ```
  - **Kontak**: Ubah informasi kontak di dalam `div` dengan `id="contact"`.
    ```html
    <div class="card-contact"><i class="fas fa-map-marker-alt"></i> Bekasi, Indonesia</div>
    <div class="card-contact"><i class="fas fa-phone"></i> +62 123 4567 890</div>
    <div class="card-contact"><i class="fas fa-envelope"></i> dika.kun@email.com</div>
    ```

#### Teks & Terjemahan (`translations`)

Edit objek `translations` untuk mengubah semua teks yang ditampilkan di portofolio, baik untuk versi Bahasa Inggris (`en`) maupun Indonesia (`id`).

#### Keahlian (`allSkills`)

Daftar keahlian Anda dalam *array* `allSkills`.

```javascript
const allSkills = [
    { name: 'Penetration Testing', level: 'Expert', width: '95%' },
    { name: 'Network Security', level: 'Advanced', width: '90%' },
    { name: 'Python (for scripting)', level: 'Intermediate', width: '75%' },
];
```

#### Sertifikasi (`allCertifications`)

```javascript
const allCertifications = [
    { issuer: 'EC-Council', name: 'Certified Ethical Hacker (CEH)' },
    { issuer: 'CompTIA', name: 'Security+' },
    { issuer: 'EC-Council', name: 'Licensed Penetration Tester (LPT)' },
];
```

#### Dunia Digital (`universeData`)

```javascript
const universeData = {
    portfolio: { /* ... biarkan default ... */ },
    main: { link: 'https://dikasite.com', target: '_blank' },
    store: { link: 'https://store.dikasite.com', target: '_blank' },
    api: { link: 'https://api.dikasite.com', target: '_blank' }
};
```

#### Perjalanan (`journeyData`)

```javascript
const journeyData = [
    { date: '2021', title_en: 'Started in Cybersecurity', title_id: 'Memulai Karir di Keamanan Siber', desc_en: 'Began my professional journey.', desc_id: 'Memulai perjalanan profesional saya.', icon: 'fa-solid fa-flag' },
    { date: '2023', title_en: 'Earned CEH Certification', title_id: 'Mendapatkan Sertifikasi CEH', desc_en: 'Achieved my first major certification.', desc_id: 'Meraih sertifikasi besar pertama saya.', icon: 'fa-solid fa-award' },
];
```

#### Proyek

```javascript
const projectCards = [
    { title: "WebApp Pentest Report", tech: "Burp Suite, OWASP ZAP", lang_key_title: "project1_title", lang_key_desc: "project1_desc"},
];
```

```javascript
en: {
    project1_title: 'WebApp Pentest Report',
    project1_desc: 'Performed a comprehensive penetration test on a live web application, identified 15+ vulnerabilities including SQLi and XSS, and provided a detailed remediation report.',
},
id: {
    project1_title: 'Laporan Uji Penetrasi WebApp',
    project1_desc: 'Melakukan uji penetrasi komprehensif pada aplikasi web, mengidentifikasi 15+ kerentanan termasuk SQLi dan XSS, serta memberikan laporan perbaikan yang mendetail.',
}
```

-----

## 🛠️ Kustomisasi Lanjutan

### Mengubah Kuis

Edit `quizData` dan `translations`.

### Mengubah Skema Warna

```css
:root {
    --bg-card: rgba(20, 20, 20, 0.7);
    --bg-body: #0a0a0a;
    --accent-color: #ff4757;
}

body.light-mode {
    --bg-card: rgba(255, 255, 255, 0.85);
    --bg-body: #f0f0f0;
    --accent-color: #d63031;
}
```

-----

## 📜 Lisensi & Kredit

  - *Template* ini bebas untuk digunakan, dimodifikasi, dan didistribusikan.
  - Ikon oleh [Font Awesome](https://fontawesome.com/).
  - *Font*: [Jost](https://fonts.google.com/specimen/Jost), [DM Sans](https://fonts.google.com/specimen/DM+Sans)
  - API: [JsonLink](https://jsonlink.io/).

-----

## ❤️ Dibuat Oleh

**Dika | DGameXO**  
_AI Engineer | Fullstack Developer | Cybersecurity Specialist_

**Masha | Masha AI**  
_Digital AI Partner & Intelligence Analysis Specialist_

Contoh: https://dgxoportfolio.netlify.app/
