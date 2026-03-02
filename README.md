Dokumentasi ini dikhususkan untuk Branch Fitur Pengeluaran yang dikembangkan oleh Kelompok B10 sebagai bagian dari proyek besar Sistem Manajemen Masjid. Modul ini fokus pada pencatatan arus kas keluar, manajemen kategori, visualisasi data, dan pelaporan.

👥 Anggota Kelompok B10
Raka Aprianto (15-2019-113)
Luthfi Ardyansyah (15-2019-110)
Maulana Seno Aji Yudhantara (15-2022-065)
🚀 Fitur Unggulan (In-Scope)
Berikut adalah fitur-fitur yang telah berhasil diimplementasikan sesuai proposal:

1. Manajemen Transaksi Pengeluaran
CRUD Lengkap: Tambah, Lihat, Edit, dan Hapus data pengeluaran.
Upload Bukti: Mendukung upload foto struk/nota transaksi.
Pencatat Otomatis: Sistem otomatis mencatat siapa user yang menginput data.
2. Manajemen Kategori
Pengelolaan dinamis untuk kategori pengeluaran (misal: Operasional, Kajian, Sosial).
Kategori yang dibuat langsung muncul di form input pengeluaran.
3. Dashboard & Visualisasi Data
Ringkasan Real-time: Menampilkan total pengeluaran bulan ini dan total keseluruhan.
Grafik Interaktif: Pie Chart (Donat) menggunakan Chart.js untuk melihat komposisi pengeluaran per kategori.
4. Laporan & Ekspor
Cetak PDF: Fitur generate laporan resmi siap cetak menggunakan DomPDF.
Filter Laporan: Bisa memilih bulan dan tahun pelaporan sesuai kebutuhan.
🛠️ Teknologi Tambahan
Selain stack utama (Laravel 10, PHP 8.1, MySQL), modul ini menambahkan dependensi berikut:

barryvdh/laravel-dompdf: Untuk generate laporan PDF.
Chart.js (CDN): Untuk visualisasi grafik di dashboard.
Alpine.js: Untuk interaktivitas modal dan form tanpa reload.
⚙️ Cara Instalasi & Menjalankan (Lokal)
Karena modul ini memiliki dependensi tambahan, harap ikuti langkah berikut saat pull atau clone:

1. Clone Repository (Branch B10)
git clone -b fitur-pengeluaran-b10 https://github.com/Zulfan15/manajemen_masjid.git
cd manajemen_masjid
2. Install Dependencies (PENTING)
Wajib dijalankan karena ada library PDF baru.

composer install
3. Setup Environment
cp .env.example .env
php artisan key:generate
Atur koneksi database di file .env sesuai settingan MySQL lokal.

4. Setup Database & Storage
php artisan migrate:fresh --seed
php artisan storage:link
Note: Perintah storage:link wajib dijalankan agar gambar bukti transaksi bisa muncul di browser.

5. Jalankan Server
php artisan serve
🔑 Akun Pengujian
Gunakan akun berikut untuk mengakses fitur Pengeluaran secara penuh:

Role: Admin Keuangan
Username: admin_keuangan
Password: password
