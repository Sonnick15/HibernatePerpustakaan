# Aplikasi CRUD Data Buku Perpustakaan

Aplikasi ini dibuat untuk mengelola data buku perpustakaan menggunakan bahasa pemrograman *Java* dengan dukungan *Hibernate* sebagai ORM dan *JasperReports* sebagai generator laporan, sebagai bagian dari ujian praktikum.
Pengguna dapat melakukan proses CRUD, cetak laporan, dan export laporan ke PDF.

## Fitur

| Fitur         | Deskripsi                                         |
| ------------- | ------------------------------------------------- |
| Tambah Data   | Menambahkan data buku baru ke database            |
| Update Data   | Mengubah data buku berdasarkan ID                 |
| Hapus Data    | Menghapus data buku dari database                 |
| Refresh       | Memuat ulang tabel agar data terbaru tampil       |
| Clear Form    | Membersihkan input form                           |
| Cetak Laporan | Menampilkan laporan data buku dengan JasperViewer |
| Export PDF    | Menyimpan laporan ke file PDF                     |

## Teknologi

* NetBeans 8.2
* Java JDK 8 (Java SE 8)
* Hibernate ORM 5.x (versi default yang umum digunakan pada NetBeans 8.2)
* JasperReports 6.x (mengikuti library bawaan praktikum)
* Database MySQL

## Database

Menggunakan *MySQL* (XAMPP) dengan tabel *buku* berisi kolom:

* id (INT, Primary Key, Auto Increment)
* judul VARCHAR
* penulis VARCHAR
* kategori VARCHAR
* tahun INT

## Setup

### 1. Membuat Database di MySQL (XAMPP)

1. Buka *phpMyAdmin*.
2. Buat database baru bernama db_perpustakaan.
3. Jalankan query berikut:

sql
CREATE TABLE buku (
  id INT AUTO_INCREMENT PRIMARY KEY,
  judul VARCHAR(100),
  penulis VARCHAR(100),
  kategori VARCHAR(50),
  tahun INT
);

INSERT INTO buku (judul, penulis, kategori, tahun) VALUES
('Laskar Pelangi', 'Andrea Hirata', 'Fiksi', 2005),
('Bumi Manusia', 'Pramoedya Ananta Toer', 'Sejarah', 1980),
('Atomic Habits', 'James Clear', 'Non-Fiksi', 2018);


### 2. Import Project ke NetBeans 8.2

1. Buka NetBeans.
2. Pilih *File > Open Project*.
3. Arahkan ke folder project praktikum.
4. Klik *Open Project*.

### 3. Konfigurasi Library Hibernate & JasperReports

1. Klik kanan project → *Properties*.
2. Masuk ke *Libraries*.
3. Tambahkan file .jar Hibernate dan JasperReports yang disediakan oleh dosen/praktikum.
4. Pastikan Hibernate Configuration (hibernate.cfg.xml) berisi koneksi:

xml
<property name="hibernate.connection.url">jdbc:mysql://localhost:3306/db_perpustakaan</property>
<property name="hibernate.connection.username">root</property>
<property name="hibernate.connection.password"></property>


### 4. Menjalankan Aplikasi

1. Jalankan aplikasi melalui: FormCRUDPerpustakaan.java
2. Klik kanan project → *Run*.
3. Aplikasi siap digunakan untuk CRUD dan generate laporan.

## Author

Nickson Winil_51422241_UJIAN
