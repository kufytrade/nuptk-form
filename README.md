# 📘 Formulir Pengajuan NUPTK --- Sistem Verval PTK

Aplikasi Web untuk Pengajuan Berkas NUPTK dengan Integrasi Google Drive
& Apps Script

Aplikasi ini dibuat untuk mempermudah guru/ operator sekolah dalam
melakukan pengajuan Calon NUPTK secara online. Semua berkas yang
diunggah akan otomatis tersimpan ke **Google Drive** dan dapat dicatat
ke **Google Sheet** (opsional).

Teknologi yang digunakan:

-   HTML + TailwindCSS\
-   JavaScript modular\
-   Google Apps Script (Web App)\
-   Base64 file transfer\
-   Hosting melalui GitHub Pages

------------------------------------------------------------------------

## 🚀 Fitur Utama

### ✔ Upload Dokumen PDF

-   SK Pengangkatan & SKBM\
-   Ijazah SD, SMP, SMA\
-   Ijazah S1 / D4\
-   Validasi format PDF\
-   Validasi ukuran file

### ✔ Pengiriman Aman

-   Konversi PDF → Base64\
-   Token keamanan\
-   Penyimpanan terstruktur ke Google Drive

### ✔ Tampilan Profesional

-   Loading bar ala SIMPKB\
-   Spinner tombol submit\
-   Modal sukses & error\
-   UI responsif

### ✔ Siap Hosting

-   100% bisa dijalankan di GitHub Pages\
-   Tidak butuh backend server

------------------------------------------------------------------------

## 📂 Struktur Folder

    nuptk-form/
    │
    ├── index.html
    │
    ├── assets/
    │   ├── css/
    │   │   └── style.css
    │   │
    │   ├── js/
    │   │   └── app.js
    │   │
    │   └── img/
    │       └── vervalptk-logo.png
    │
    └── README.md

------------------------------------------------------------------------

## 🔧 Cara Upload ke GitHub

1.  Login ke GitHub\
2.  Buat repository baru → **New Repository**\
3.  Nama repo: `nuptk-form`\
4.  Klik **Create repository**\
5.  Klik **Upload files**\
6.  Drag & drop semua folder/file sesuai struktur di atas\
7.  Klik **Commit changes**

------------------------------------------------------------------------

## 🌐 Cara Hosting di GitHub Pages

1.  Masuk ke repository → **Settings**\
2.  Pilih **Pages**\
3.  Source → **Deploy from a branch**\
4.  Branch → `main`\
5.  Folder → `/ (root)`\
6.  Klik **Save**

GitHub akan membuat URL publik seperti:

    https://username.github.io/nuptk-form/

------------------------------------------------------------------------

## ⚙️ Cara Setup Google Apps Script

1.  Buka https://script.google.com/\
2.  Buat **New Project**\
3.  Buat file `Code.gs`\
4.  Tempel script Apps Script yang sudah dibuat sebelumnya\
5.  Ubah konfigurasi:

``` javascript
const SHARED_TOKEN = "NUPTK-SECURE-2025";
const PARENT_FOLDER_ID = "ID_FOLDER_DRIVE";   // opsional
const LOG_SHEET_ID = "ID_SPREADSHEET";        // opsional
```

6.  Deploy:
    -   Klik **Deploy → New Deployment**
    -   Type: **Web app**
    -   Execute as: **Me**
    -   Access: **Anyone**
    -   Deploy & copy URL Web App
7.  Ganti URL di `app.js`:

``` javascript
const GAS_WEB_APP_URL = "https://script.google.com/macros/s/XXXX/exec";
```

------------------------------------------------------------------------

## 🧪 Cara Menguji Aplikasi

1.  Buka URL GitHub Pages\
2.  Isi semua form\
3.  Upload dokumen PDF\
4.  Klik **Ajukan Data**\
5.  Cek Google Drive:
    -   Folder baru dengan format **"NamaGuru - Pengajuan NUPTK"**\
6.  Cek Google Sheet (jika diaktifkan)

------------------------------------------------------------------------

## 🖼 Mengganti Logo

Ganti file berikut:

    assets/img/vervalptk-logo.png

Dengan file PNG apa pun (logo sekolah / verval PTK versi Anda).

------------------------------------------------------------------------

## 🔒 Catatan Keamanan

-   Tidak ada data disimpan di server selain Google Drive/GSheets Anda.\
-   Hanya browser pengguna → Apps Script → Google Drive.\
-   Token keamanan wajib digunakan untuk mencegah penyalahgunaan.

------------------------------------------------------------------------

## 🤝 Kontribusi

Silakan gunakan atau modifikasi untuk kebutuhan sekolah, yayasan, atau
operator.\
Boleh ditambahkan fitur:

-   Notifikasi WhatsApp\
-   Dashboard admin\
-   Rekap otomatis\
-   Integrasi Firebase\
-   Export PDF

------------------------------------------------------------------------

## 🏁 Lisensi

**Gratis digunakan untuk keperluan pendidikan.**
