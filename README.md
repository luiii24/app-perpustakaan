# App Perpustakaan

Aplikasi manajemen perpustakaan berbasis web yang dibangun menggunakan **Laravel 12** untuk mengelola data buku, peminjaman, serta anggota perpustakaan secara efisien.

## Tujuan Project
Project ini bertujuan untuk menyediakan sistem informasi perpustakaan yang modern, responsif, dan mudah digunakan, sekaligus memanfaatkan fitur-fitur terbaru Laravel 12 seperti performa yang lebih optimal dan struktur aplikasi yang streamlined.

## Cara Menjalankan Project Secara Lokal

### Prasyarat
- XAMPP (PHP >= 8.2 & MySQL/MariaDB)
- Composer

### Langkah Instalasi

1. **Setup project**
   ```bash
   cd c:/xampp/htdocs
   git clone <url-repository-anda> app-perpustakaan
   cd app-perpustakaan
   cp .env.example .env
   ```
2. **Setup DB**
    Buka XAMPP Control Panel, jalankan Apache dan MySQL Akses http://localhost/phpmyadmin di browser dan buat database baru (contoh: db_perpustakaan).
    Buka file .env di text editor, sesuaikan konfigurasi berikut:
   ```DB_CONNECTION=mysql
    DB_HOST=127.0.0.1
    DB_PORT=3306
    DB_DATABASE=db_perpustakaan
    DB_USERNAME=root
    DB_PASSWORD=
   ```
3. **Setup PHP & composer**
   ```bash
   composer install
   php artisan key:generate
   php artisan migrate --seed
   ```
4. **Menjalankan project**
    ```
    php artisan serve
    ```

### Jawaban Refleksi (Perbedaan Model, View, dan Controller):

> **Model** bertugas mengelola struktur data dan komunikasi langsung dengan database MySQL di XAMPP.

> **View** berisi tampilan HTML/Blade yang menyajikan antarmuka visual kepada pengguna, sedangkan.

> **Controller** berfungsi sebagai jembatan yang menerima *request* pengguna, memproses data melalui Model, lalu mengirimkan hasilnya ke View.