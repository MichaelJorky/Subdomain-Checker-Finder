# **Subdomain Checker & Finder**

A lightweight, fast, and multi-threaded tool for discovering and validating subdomains.

## **📌 Overview**

**Subdomain Checker & Finder** adalah aplikasi Windows yang dirancang untuk membantu administrator sistem, peneliti keamanan, maupun developer dalam mendeteksi dan memvalidasi subdomain pada suatu domain. Dengan antarmuka yang sederhana, aplikasi ini mampu melakukan pengecekan secara paralel (multi-threaded) untuk mempercepat proses scanning.

Aplikasi ini masih dalam tahap **Beta Version**, namun telah stabil digunakan untuk tugas-tugas dasar enumerasi dan pengecekan respons subdomain menggunakan HTTP/HTTPS.

---

## **✨ Fitur Utama**

### **🔍 1. Subdomain Loader**

* Memuat daftar subdomain dari file eksternal.
* Menampilkan jumlah total subdomain yang berhasil dimuat.
* Mendukung list dalam format text file (.txt).

### **⚡ 2. Multi-threaded Checker**

* Penggunaan thread paralel untuk mempercepat proses scanning.
* Pengaturan jumlah thread dapat disesuaikan (misalnya default 10 threads).

### **🌐 3. SNI Host Support**

* Input khusus untuk *SNI Host* (misalnya `example.com`) guna memastikan koneksi TLS yang kompatibel saat melakukan pengecekan subdomain HTTPS.

### **🧪 4. Real-time Scan Result**

Aplikasi menampilkan informasi dalam tabel, termasuk:

* **Subdomain** yang sedang dicek
* **HTTP status code**
* **Full URL**
* **Protocol support** (HTTP/HTTPS)
* **Response time**

### **▶️ 5. Start / Stop Scan Control**

* Tombol *Start* untuk memulai proses scanning.
* Tombol *Stop* untuk menghentikan proses kapan saja.

### **📊 6. UI Ringan dan User-Friendly**

* Antarmuka Windows yang sederhana dan mudah digunakan.
* Informasi status tampil pada *status bar* bagian bawah (misalnya total subdomain yang dimuat).

---

## **🔧 Cara Menggunakan**

1. **Persiapan Daftar Subdomain**

   * Aplikasi secara otomatis memuat file default bernama **`_sublist.txt`** pada folder aplikasi.
   * File ini dapat **diedit oleh user** untuk menambah, mengurangi, atau memodifikasi daftar subdomain.
   * Jika file tersebut tidak ada, aplikasi tetap dapat dijalankan dan Anda dapat memuat daftar secara manual.

2. **Memuat Subdomain Secara Manual (Opsional)**

   * Jika ingin menggunakan daftar lain, klik tombol **Load**.
   * Pilih file `.txt` berisi list subdomain yang ingin Anda gunakan.
   * Aplikasi akan menampilkan jumlah total subdomain yang berhasil dimuat pada status bar.

3. **Pengaturan Scan**

   * Atur jumlah **Max Threads** sesuai kebutuhan (misalnya 10 sebagai default). Semakin besar nilai ini, semakin cepat proses scanning, tetapi lebih berat bagi sistem.
   * Masukkan **SNI Host** sesuai domain target (contoh: `example.com`). Ini memastikan koneksi TLS/HTTPS bekerja dengan benar.

4. **Memulai Proses Scan**

   * Klik tombol **Start** untuk menjalankan pemeriksaan.
   * Setiap subdomain akan dicek satu per satu menggunakan pengaturan multi-thread.
   * Hasil akan muncul secara real-time pada tabel (Subdomain, Status Code, URL, Support, Time).

5. **Menghentikan Proses (Opsional)**

   * Anda dapat menghentikan proses kapan saja dengan tombol **Stop**, terutama jika ingin mengganti list subdomain atau ingin melakukan pengecekan ulang.

6. **Review Hasil Scan**

   * Tabel utama menampilkan hasil pengecekan lengkap yang dapat digunakan untuk analisis lebih lanjut.
   * Ekspor file otomatis ke CSV/TXT.

---

## **🚧 Status Pengembangan**

Versi ini adalah **Beta v1.0.0.1**, sehingga beberapa fitur lanjutan masih dalam tahap pengembangan, seperti:

* Export hasil scan (HTML/JSON)
* Pengecekan wildcard
* Auto-discover using DNS brute-force
* Integrasi API TLS/HTTP advanced

Kontribusi, laporan bug, atau saran fitur sangat diterima.

---
