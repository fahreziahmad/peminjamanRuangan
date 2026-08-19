# SIPERU UMY - Sistem Peminjaman Ruangan Kampus UMY

**SIPERU UMY** adalah Single Page Application (SPA) berbasis web untuk mengelola dan memfasilitasi peminjaman ruangan di lingkungan Universitas Muhammadiyah Yogyakarta. Aplikasi ini dirancang menggunakan standar desain modern dengan nuansa khas hijau-emas UMY, glassmorphism, dan transisi halus.

Aplikasi ini menggunakan **HTML5**, **Vanilla CSS3**, **Vanilla JavaScript (ES6+)**, dan **LocalStorage** untuk penyimpanan state/database lokal tanpa memerlukan setup database eksternal yang rumit.

---

## 🚀 Fitur Utama
1. **SPA Routing**: Navigasi halaman instan tanpa perlu reload halaman.
2. **Katalog & Discovery Ruangan**: Pencarian ruangan berdasarkan nama, tipe, gedung, dan filter fasilitas.
3. **Validasi Bentrok & Kapasitas**: Mencegah *double-booking* pada hari/sesi yang sama dan memvalidasi batas kapasitas peserta.
4. **Dashboard Admin**: Visualisasi analitik menggunakan **Chart.js** untuk kepadatan booking per gedung dan status persetujuan.
5. **Manajemen Ruangan (CRUD)**: Admin Sarpras dapat menambah, memperbarui status (Tersedia/Maintenance), mengedit, dan menghapus ruangan.
6. **Slip Izin Resmi**: Pemohon yang disetujui dapat mengunduh dan mencetak slip izin resmi (dilengkapi dengan QR Code verifikasi) dengan desain *print-ready* CSS.
7. **Analisis UML**: Dilengkapi file diagram UML lengkap (`uml_diagrams.md`).

---

## 🛠️ Cara Menjalankan Project Secara Lokal

Aplikasi ini adalah static site, namun untuk memastikan fitur **LocalStorage**, dynamic routing, dan pemuatan CDN eksternal (Chart.js & Lucide Icons) berjalan dengan aman tanpa kendala kebijakan keamanan CORS browser (`file://`), **sangat direkomendasikan** untuk dijalankan menggunakan local server:

### Opsi 1: Menggunakan Python (Direkomendasikan & Paling Mudah)
Jika Anda memiliki Python terinstal di komputer Anda, jalankan perintah ini di dalam direktori project:

```bash
python -m http.server 8000
```
Setelah itu, buka browser Anda dan akses:
👉 **[http://localhost:8000](http://localhost:8000)**

### Opsi 2: Menggunakan Node.js (`http-server`)
Jika Anda menggunakan Node.js, Anda bisa menjalankan server statik dengan perintah:

```bash
npx http-server -p 8000
```
Setelah itu, buka browser Anda dan akses:
👉 **[http://localhost:8000](http://localhost:8000)**

### Opsi 3: Membuka Langsung `index.html` (Tanpa Server)
Anda bisa langsung melakukan klik ganda (double-click) pada file `index.html` untuk membukanya di browser. Namun, pastikan browser Anda mengizinkan fitur `localStorage` untuk berjalan pada protokol `file://`.

---

## 🔑 Akun Uji Coba (Quick Fill)
Untuk mempermudah pengujian, terdapat tombol **Quick Fill** di menu Login untuk mengisi kredensial secara otomatis:

| Role | Username | Password | Deskripsi / Organisasi |
| :--- | :--- | :--- | :--- |
| **Mahasiswa** | `mhs` | `mhs` | BEM Fakultas Teknik UMY |
| **Dosen** | `dosen` | `dosen` | Prodi Teknologi Informasi UMY |
| **Admin Sarpras** | `admin` | `admin` | Biro Aset & Sarpras UMY |

---

## 📂 Struktur Direktori Project
```
umy-room-booking/
├── assets/                     # Gambar dan aset photorealistic ruangan (PNG)
│   ├── umy_campus_hero.png
│   ├── amphitheater.png
│   ├── ruang_sidang.png
│   ├── sportorium.png
│   ├── ruang_seminar.png
│   ├── lab_komputer.png
│   └── meeting_room.png
├── index.html                  # Struktur utama aplikasi (SPA Shell & Modals)
├── style.css                   # Desain antarmuka premium (Responsif & Cetak)
├── app.js                      # Router, controller, dan logika validasi booking
├── mockData.js                 # Seeding awal dan wrapper database LocalStorage
├── uml_diagrams.md             # Kode Mermaid.js untuk diagram UML lengkap
└── README.md                   # Panduan instalasi dan penggunaan
```

---

## 📊 Dokumentasi Diagram UML
Seluruh file diagram UML (Use Case, Activity, Class, Sequence, dan Communication Diagram) ditulis menggunakan format diagram modern **Mermaid.js**. Kode diagram tersebut dapat dilihat dan dibaca pada file:
👉 **`uml_diagrams.md`**
