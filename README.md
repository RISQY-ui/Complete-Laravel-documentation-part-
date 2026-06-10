# Complete-Laravel-documentation-part-
Dokumentasi langkah awal setup dan proyek pertama Laravel 13: Persiapan lingkungan, instalasi, konfigurasi database SQLite, hingga membuat Model &amp; Controller API.
Documentation of the initial setup steps and first project of Laravel 13: Environment preparation, installation, SQLite database configuration, to creating Model & Controller API.
--------------------------------------

# Dokumentasi Lengkap: Persiapan & Proyek Laravel 13

## 📋 Daftar Isi

- [I. Persiapan Awal (Setup Lingkungan)](#i-persiapan-awal-setup-lingkungan)
- [II. Inisialisasi Proyek Laravel](#ii-inisialisasi-proyek-laravel)
- [III. Konfigurasi Database & Server](#iii-konfigurasi-database--server)
- [IV. Panduan "Daging" (Langkah Lanjutan)](#iv-panduan-daging-langkah-lanjutan)

---

## I. Persiapan Awal (Setup Lingkungan)

| Langkah | Perintah | Keterangan |
|---------|----------|-------------|
| Instalasi PHP 8.3 | `sudo apt install php8.3` | Memastikan sistem Linux memiliki PHP 8.3 untuk performa terbaru |
| Instalasi Composer | `sudo apt install composer` | Mengelola library proyek |
| Verifikasi PHP | `php -v` | Cek versi PHP sebelum mulai |
| Verifikasi Composer | `composer --version` | Cek versi Composer sebelum mulai |

---

## II. Inisialisasi Proyek Laravel

### 1. Buat Proyek Baru

Masuk ke folder `Desktop` (atau folder kerja pilihan), lalu jalankan:

```bash
composer create-project laravel/laravel proyek-pertama-laravel
```

2. Instalasi Extension Wajib

Jika muncul error, pastikan modul berikut terpasang agar Laravel bisa "bernafas":

```bash
# Untuk database SQLite
sudo apt install php8.3-sqlite3

# Modul standar PHP
sudo apt install php8.3-xml php8.3-dom
```

---

III. Konfigurasi Database & Server

1. Migrasi Tabel

Setelah instalasi selesai, jalankan perintah berikut untuk membuat tabel sistem (seperti users, sessions, jobs) di database SQLite:

```bash
php artisan migrate
```

2. Jalankan Server

```bash
php artisan serve
```

3. Akses Hasil

Buka browser dan arahkan ke alamat:

```
http://127.0.0.1:8000
```

---

IV. Panduan "Daging" (Langkah Lanjutan)

1. Membuat Model & File Migrasi

```bash
php artisan make:model NamaModel -m
```

⚠️ Peringatan: Jangan ketik make:modal (itu typo, harus make:model)

2. Membuat Controller API

```bash
php artisan make:controller NamaController --api
```

Perintah ini membuat Controller yang bersih dan khusus untuk API.

---

📝 Catatan Penting

Komponen Fungsi
php artisan migrate Membuat tabel di database
php artisan serve Menjalankan development server
make:model Membuat file Model (plus migrasi dengan -m)
make:controller --api Membuat Controller khusus API

---

🐛 Troubleshooting

Masalah Solusi
php: command not found Install PHP dulu: sudo apt install php8.3
composer: command not found Install Composer: sudo apt install composer
Error terkait xml atau dom Jalankan: sudo apt install php8.3-xml php8.3-dom
Error terkait sqlite Jalankan: sudo apt install php8.3-sqlite3
Port 8000 sudah digunakan Gunakan port lain: php artisan serve --port=8080

---

Dokumentasi untuk keperluan pembelajaran Laravel 13 oleh Faris.

