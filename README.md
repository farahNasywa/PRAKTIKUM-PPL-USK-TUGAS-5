# Tugas 5 PPL – Sistem API Sederhana

Repositori ini berisi hasil pengerjaan Tugas 5 untuk mata kuliah Praktikum PPL di Universitas Syiah Kuala. Tugas ini berfokus pada pembuatan sistem API sederhana menggunakan **AdonisJS**, yang dapat melakukan operasi dasar seperti melihat dan menambahkan data ke database menggunakan ORM **Lucid** dan database **MySQL**.

## 📌 Deskripsi Singkat

API yang dibuat dalam tugas ini memungkinkan pengguna untuk:

* Melihat daftar semua item (GET)
* Melihat detail satu item berdasarkan ID (GET)
* Menambahkan item baru ke dalam sistem (POST)

Data yang digunakan memiliki tema tertentu dan disimpan dalam database menggunakan **Lucid ORM** milik AdonisJS.

## ✅ Fitur Wajib

Berikut fitur yang telah diimplementasikan sesuai instruksi:

* [x] Route `GET /[resource]` – Menampilkan semua item
* [x] Route `GET /[resource]/:id` – Menampilkan satu item berdasarkan ID
* [x] Route `POST /[resource]` – Menambahkan data baru melalui Postman
* [x] Data disimpan di **MySQL**
* [x] Menggunakan **Lucid ORM**
* [x] Tema data: (misalnya: Komik, Karakter, Buku, dll)
* [x] Setiap item memiliki minimal **3 atribut**

> Catatan: Tidak ada tampilan UI yang disediakan. Interaksi hanya dilakukan melalui Postman atau browser (untuk GET request).

## ✨ Nilai Tambahan (Jika Ada)

* [ ] Fitur `UPDATE` (PUT/PATCH)
* [ ] Fitur `DELETE`
* [ ] UI sederhana
* [ ] Fitur tambahan lainnya

## ⚙️ Teknologi yang Digunakan

* [AdonisJS](https://adonisjs.com/)
* MySQL
* Lucid ORM
* Node.js
* Postman (untuk pengujian API)

## 🚀 Cara Menjalankan Proyek

1. **Clone repositori**

   ```bash
   git clone https://github.com/farahNasywa/PRAKTIKUM-PPL-USK-TUGAS-5.git
   cd PRAKTIKUM-PPL-USK-TUGAS-5
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

3. **Konfigurasi database**

   * Buat database MySQL
   * Salin file `.env.example` menjadi `.env` lalu sesuaikan konfigurasi database:

     ```
     DB_CONNECTION=mysql
     MYSQL_USER=root
     MYSQL_PASSWORD=
     MYSQL_DB_NAME=nama_database
     ```

4. **Generate key dan migrasi database**

   ```bash
   node ace generate:key
   node ace migration:run
   ```

5. **Jalankan server**

   ```bash
   node ace serve --watch
   ```

6. **Uji endpoint melalui Postman**

## 🛠 Contoh Endpoint

* GET semua item: `http://localhost:3333/items`
* GET satu item: `http://localhost:3333/items/1`
* POST data baru: `http://localhost:3333/items`


```

## 📁 Struktur Folder (Singkat)

```
├── app/
│   ├── Controllers/
│   ├── Models/
├── database/
│   ├── migrations/
├── start/
├── .env
├── package.json
└── README.md
```
