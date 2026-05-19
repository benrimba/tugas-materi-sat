# 📚 MATERI AJAR PPB + BASIS DATA

> Materi Persiapan SAT (Sumatif Akhir Tahun) Kelas XI PPLG 

## 🚀 Kompetensi yang Dipelajari

- Dasar PHP Native
- Variabel dan Tipe Data
- Function PHP
- Array dan Perulangan
- Form Handling (GET & POST)
- Session Login
- CRUD PHP Native + MySQLi
- Dasar Basis Data
- SQL Dasar
- JOIN Database
- Relasi Database
- Normalisasi
- Keamanan Web Dasar
- Proyek Mini Sistem Data Siswa

---

# MATERI AJAR
## Persiapan SAT (Sumatif Akhir Tahun)
### Mata Pelajaran PPB (Pemrograman Berbasis Objek) + Basis Data
### Kelas XI PPLG – Kurikulum Merdeka

---

# DAFTAR ISI
1. Dasar Pemrograman PHP
2. Variabel dan Tipe Data
3. Operator dan Percabangan
4. Array dan Array Multidimensi
5. Function / Fungsi PHP
6. Form Handling (GET & POST)
7. Session dan Login System
8. Debugging dan Error Handling
9. Keamanan Dasar Web
10. Dasar Basis Data
11. ERD dan Relasi Database
12. Normalisasi Database
13. SQL Dasar
14. JOIN pada SQL
15. CRUD PHP Native + MySQLi
16. Studi Kasus dan Latihan
17. Ringkasan Materi Penting SAT

---

# 1. DASAR PEMROGRAMAN PHP

## Pengertian PHP
PHP (Hypertext Preprocessor) adalah bahasa pemrograman server-side yang digunakan untuk membuat website dinamis.

Contoh kode PHP:

```php
<?php
 echo "Halo Dunia";
?>
```

## Ciri-Ciri PHP
- Berjalan di server
- Dapat terhubung dengan database
- Digunakan untuk website dinamis
- Mudah dipelajari

## Penulisan PHP
Kode PHP ditulis di antara:

```php
<?php
// kode
?>
```

## Aturan Dasar PHP
- Setiap perintah diakhiri titik koma (;)
- Variabel diawali tanda $
- PHP bersifat case sensitive

Contoh:

```php
<?php
$nama = "Budi";
$Nama = "Andi";

echo $nama;
?>
```

Variabel `$nama` dan `$Nama` dianggap berbeda.

---

# 2. VARIABEL DAN TIPE DATA

## Variabel
Variabel digunakan untuk menyimpan data.

Contoh:

```php
<?php
$nama = "Rudi";
$umur = 17;
?>
```

## Tipe Data PHP

| Tipe Data | Contoh |
|---|---|
| String | "Halo" |
| Integer | 100 |
| Float | 10.5 |
| Boolean | true / false |
| Array | [1,2,3] |

## Fungsi String Penting

### strlen()
Menghitung jumlah karakter.

```php
<?php
 echo strlen("SMK");
?>
```

Hasil: 3

### trim()
Menghapus spasi di awal dan akhir string.

```php
<?php
 echo trim(" Andi ");
?>
```

### substr()
Mengambil sebagian string.

```php
<?php
 echo substr("Pemrograman",0,4);
?>
```

Hasil: Pemr

---

# 3. OPERATOR DAN PERCABANGAN

## Operator Aritmatika

| Operator | Fungsi |
|---|---|
| + | Tambah |
| - | Kurang |
| * | Kali |
| / | Bagi |
| % | Modulus |

Contoh:

```php
<?php
$a = 10;
$b = 5;

echo $a + $b;
?>
```

## Percabangan IF

```php
<?php
$nilai = 80;

if($nilai >= 75){
   echo "Lulus";
}else{
   echo "Tidak Lulus";
}
?>
```

---

# 4. ARRAY DAN ARRAY MULTIDIMENSI

## Array Numerik

```php
<?php
$buah = ["Apel","Mangga","Jeruk"];

echo $buah[0];
?>
```

## Array Associative

```php
<?php
$siswa = [
   "nama" => "Budi",
   "kelas" => "XI"
];

echo $siswa['nama'];
?>
```

## Array Multidimensi

```php
<?php
$gim = [
   ["judul" => "Gim A"],
   ["judul" => "Gim B"]
];

echo $gim[1]['judul'];
?>
```

Hasil: Gim B

---

# 5. FUNCTION / FUNGSI PHP

## Pengertian Function
Function digunakan agar kode dapat dipakai berulang.

## Membuat Function

```php
<?php
function sapa(){
   echo "Halo Siswa";
}

sapa();
?>
```

## Function dengan Parameter

```php
<?php
function luas($p,$l){
   return $p * $l;
}

echo luas(10,5);
?>
```

## Parameter Default

```php
<?php
function sapa($nama = "Siswa"){
   return "Halo " . $nama;
}

echo sapa();
?>
```

Hasil: Halo Siswa

---

# 6. FORM HANDLING (GET & POST)

## Method GET
Data dikirim melalui URL.

Contoh:

```html
<form method="GET">
```

URL akan terlihat seperti:

```text
cari.php?nama=andi
```

### Ciri GET
- Data terlihat di URL
- Cocok untuk pencarian
- Tidak aman untuk password

## Method POST
Data dikirim secara tersembunyi.

```html
<form method="POST">
```

### Ciri POST
- Data tidak terlihat di URL
- Lebih aman
- Cocok untuk login/password

## Mengambil Data Form

### GET

```php
<?php
$nama = $_GET['nama'];
?>
```

### POST

```php
<?php
$nama = $_POST['nama'];
?>
```

## isset()
Digunakan mengecek apakah variabel tersedia.

```php
<?php
if(isset($_POST['simpan'])){
   echo "Data Ada";
}
?>
```

---

# 7. SESSION DAN LOGIN SYSTEM

## Pengertian Session
Session digunakan untuk menyimpan data pengguna selama login.

## session_start()
WAJIB dipanggil sebelum menggunakan session.

```php
<?php
session_start();
?>
```

## Menyimpan Session

```php
<?php
$_SESSION['username'] = "admin";
?>
```

## Mengecek Login

```php
<?php
session_start();

if(!isset($_SESSION['username'])){
   header("Location: login.php");
   exit();
}
?>
```

## Logout

```php
<?php
session_start();
session_unset();
session_destroy();
?>
```

---

# 8. DEBUGGING DAN ERROR HANDLING

## Debugging
Debugging adalah proses mencari dan memperbaiki error.

## Jenis Error

### Syntax Error
Kesalahan penulisan kode.

Contoh:

```php
<?php
 echo "Halo"
?>
```

Kurang tanda titik koma (;)

### Logical Error
Program berjalan tetapi hasil salah.

### Runtime Error
Error saat program dijalankan.

## Pesan Error MySQLi

Contoh:

```text
Access denied for user
```

Artinya username/password database salah.

---

# 9. KEAMANAN DASAR WEB

## Cross Site Scripting (XSS)
Terjadi ketika user memasukkan script berbahaya.

### Pencegahan
Gunakan:

```php
htmlspecialchars()
```

Contoh:

```php
<?php
$nama = htmlspecialchars($_POST['nama']);
?>
```

## SQL Injection
Terjadi ketika user memasukkan query SQL berbahaya.

Contoh:

```text
' OR '1'='1
```

### Pencegahan
Gunakan:

```php
mysqli_real_escape_string()
```

Contoh:

```php
<?php
$nama = mysqli_real_escape_string($conn,$_POST['nama']);
?>
```

## Password Hashing
Password tidak boleh disimpan teks biasa.

Gunakan:

```php
password_hash()
```

Contoh:

```php
<?php
$password = password_hash("admin123", PASSWORD_DEFAULT);
?>
```

---

# 10. DASAR BASIS DATA

## Pengertian Basis Data
Basis data adalah kumpulan data yang tersimpan secara terstruktur.

## RDBMS
Relational Database Management System.

Contoh:
- MySQL
- MariaDB
- PostgreSQL

## Karakteristik RDBMS
- Data berbentuk tabel
- Memiliki relasi
- Menggunakan primary key dan foreign key

---

# 11. ERD DAN RELASI DATABASE

## ERD (Entity Relationship Diagram)
Digunakan untuk merancang database.

## Komponen ERD

| Komponen | Bentuk |
|---|---|
| Entitas | Persegi Panjang |
| Atribut | Oval |
| Relasi | Belah Ketupat |

## Jenis Relasi

### One to One
Satu data berhubungan dengan satu data.

### One to Many
Satu siswa memiliki banyak nilai.

### Many to Many
Satu buku dipinjam banyak anggota.

## Primary Key
Kunci utama untuk identitas unik.

Contoh:
- id_siswa
- id_produk

## Foreign Key
Kunci yang menghubungkan tabel.

Contoh:
- id_siswa pada tabel nilai

---

# 12. NORMALISASI DATABASE

## Tujuan Normalisasi
- Mengurangi duplikasi data
- Mempermudah pengelolaan data
- Menjaga konsistensi

## 1NF
- Data harus atomic
- Tidak ada data ganda dalam satu kolom

## 2NF
- Sudah 1NF
- Tidak ada partial dependency

---

# 13. SQL DASAR

## CREATE DATABASE

```sql
CREATE DATABASE db_toko;
```

## CREATE TABLE

```sql
CREATE TABLE siswa(
   id INT,
   nama VARCHAR(100)
);
```

## INSERT

```sql
INSERT INTO produk(nama_produk,harga)
VALUES('Mouse',50000);
```

## SELECT

```sql
SELECT * FROM siswa;
```

## WHERE

```sql
SELECT * FROM siswa
WHERE nilai > 80;
```

## UPDATE

```sql
UPDATE produk
SET harga = 10000
WHERE id_produk = 1;
```

## DELETE

```sql
DELETE FROM siswa
WHERE id_siswa = 12;
```

## LIKE

```sql
SELECT * FROM produk
WHERE nama_produk LIKE '%Gim%';
```

## Fungsi Agregasi

| Fungsi | Kegunaan |
|---|---|
| COUNT | Menghitung jumlah |
| SUM | Menjumlahkan |
| AVG | Rata-rata |
| MAX | Nilai terbesar |
| MIN | Nilai terkecil |

Contoh:

```sql
SELECT AVG(nilai)
FROM siswa;
```

---

# 14. JOIN PADA SQL

## INNER JOIN
Menampilkan data yang cocok di kedua tabel.

```sql
SELECT siswa.nama, nilai.angka
FROM siswa
INNER JOIN nilai
ON siswa.id_siswa = nilai.id_siswa;
```

## LEFT JOIN
Semua data tabel kiri tetap tampil.

```sql
SELECT produk.nama_produk, transaksi.id_transaksi
FROM produk
LEFT JOIN transaksi
ON produk.id_produk = transaksi.id_produk;
```

Jika data transaksi tidak ada maka hasil NULL.

---

# 15. CRUD PHP NATIVE + MYSQLI

## Koneksi Database

```php
<?php
$conn = new mysqli("localhost","root","","db_sekolah");
?>
```

## CREATE

```php
<?php
$sql = "INSERT INTO siswa(nama)
VALUES('Andi')";
mysqli_query($conn,$sql);
?>
```

## READ

```php
<?php
$result = mysqli_query($conn,"SELECT * FROM siswa");

while($row = mysqli_fetch_assoc($result)){
   echo $row['nama'];
}
?>
```

## UPDATE

```php
<?php
mysqli_query($conn,
"UPDATE siswa SET nama='Budi' WHERE id=1");
?>
```

## DELETE

```php
<?php
mysqli_query($conn,
"DELETE FROM siswa WHERE id=1");
?>
```

## Menutup Koneksi

```php
<?php
mysqli_close($conn);
?>
```

---

# 16. STUDI KASUS DAN LATIHAN

## Studi Kasus 1
Buat login sederhana menggunakan:
- form POST
- session
- mysqli

## Studi Kasus 2
Buat CRUD siswa dengan:
- tambah data
- edit data
- hapus data
- tampil data

## Studi Kasus 3
Buat pencarian produk menggunakan LIKE.

---

# 17. RINGKASAN MATERI PENTING SAT

## PHP
- PHP bersifat case sensitive
- Variabel diawali $
- Setiap perintah diakhiri ;

## Fungsi Penting
- strlen() → menghitung karakter
- trim() → hapus spasi
- isset() → cek variabel
- htmlspecialchars() → anti XSS
- password_hash() → hash password

## Form
- GET → data terlihat di URL
- POST → data tersembunyi

## Session
- session_start() wajib dipanggil
- session_destroy() untuk logout

## Database
- Primary Key = identitas unik
- Foreign Key = penghubung tabel
- One to Many = satu ke banyak
- Many to Many = perlu tabel relasi

## SQL Penting
- CREATE DATABASE
- INSERT
- SELECT
- UPDATE
- DELETE
- JOIN

## JOIN
- INNER JOIN = data cocok saja
- LEFT JOIN = semua data kiri tampil

## Keamanan
- Gunakan htmlspecialchars()
- Gunakan mysqli_real_escape_string()
- Password gunakan password_hash()

---

# 18. TUGAS DAN LATIHAN SISWA

## TUGAS 1 – Variabel dan Output PHP

### Instruksi:
Buatlah program PHP sederhana untuk:
1. Menampilkan nama siswa
2. Menampilkan kelas
3. Menampilkan jurusan

### Ketentuan:
- Gunakan variabel
- Gunakan echo
- Simpan dengan nama file `profil.php`

### Contoh Output:

```text
Nama : Andi
Kelas : XI PPLG
Jurusan : PPLG
```

---

## TUGAS 2 – Menggunakan Function PHP

### Instruksi:
Buat function bernama `hitungLuas()` untuk menghitung luas persegi panjang.

### Ketentuan:
- Gunakan parameter panjang dan lebar
- Gunakan return
- Tampilkan hasilnya

### Contoh:

```php
<?php
function hitungLuas($p, $l){
   return $p * $l;
}

echo hitungLuas(10,5);
?>
```

---

## TUGAS 3 – Membuat Form POST

### Instruksi:
Buat form input data siswa menggunakan method POST.

### Data yang Diinput:
- Nama
- Kelas
- Jurusan

### Ketentuan:
- Gunakan `$_POST`
- Gunakan `isset()`
- Tampilkan hasil input

---

## TUGAS 4 – Array dan Perulangan

### Instruksi:
Buat array berisi 5 nama siswa kemudian tampilkan menggunakan perulangan.

### Ketentuan:
- Gunakan array numerik
- Gunakan foreach atau for

### Contoh Output:

```text
1. Andi
2. Budi
3. Caca
```

---

## TUGAS 5 – Membuat Login Session Sederhana

### Instruksi:
Buat halaman login sederhana menggunakan session.

### Ketentuan:
- Gunakan `session_start()`
- Simpan username ke session
- Jika belum login redirect ke login.php
- Buat tombol logout

---

## TUGAS 6 – Membuat Database Sekolah

### Instruksi:
Buat database bernama `db_sekolah`.

### Buat tabel:

#### Tabel siswa
- id_siswa
- nama
- kelas

#### Tabel nilai
- id_nilai
- id_siswa
- mapel
- nilai

### Ketentuan:
- Gunakan Primary Key
- Gunakan Foreign Key

---

## TUGAS 7 – SQL Dasar

### Instruksi:
Tuliskan query SQL berikut:
1. Membuat database
2. Membuat tabel siswa
3. Menambah data siswa
4. Menampilkan seluruh data siswa
5. Mengubah nama siswa
6. Menghapus data siswa

---

## TUGAS 8 – Membuat CRUD Siswa

### Instruksi:
Buat aplikasi CRUD data siswa menggunakan:
- PHP Native
- MySQLi
- Bootstrap/Tailwind (opsional)

### Fitur:
- Tambah Data
- Tampil Data
- Edit Data
- Hapus Data

### Struktur Database:

| Kolom | Tipe |
|---|---|
| id | INT |
| nama | VARCHAR |
| kelas | VARCHAR |
| jurusan | VARCHAR |

---

## TUGAS 9 – JOIN Database

### Instruksi:
Buat query JOIN untuk menampilkan:
- nama siswa
- mata pelajaran
- nilai

### Ketentuan:
- Gunakan INNER JOIN
- Gunakan tabel siswa dan nilai

---

## TUGAS 10 – Keamanan Web

### Instruksi:
Jelaskan:
1. Apa itu SQL Injection
2. Apa itu XSS
3. Fungsi `htmlspecialchars()`
4. Fungsi `mysqli_real_escape_string()`
5. Fungsi `password_hash()`

### Ketentuan:
- Jawaban minimal 5 kalimat setiap nomor

---

# PROYEK AKHIR MINI

## Tema:
Sistem Data Siswa Berbasis Web

### Fitur Minimal:
- Login sederhana
- CRUD siswa
- Pencarian data
- Logout session
- Database MySQL

### Ketentuan:
- PHP Native
- Koneksi menggunakan:

```php
$conn = new mysqli("localhost","root","","db_sekolah");
```

- Gunakan folder terstruktur
- Tampilan rapi

### Penilaian:

| Aspek | Bobot |
|---|---|
| Logika Program | 30 |
| Tampilan | 20 |
| Database | 20 |
| CRUD Berjalan | 20 |
| Kerapihan Kode | 10 |

---

# PENUTUP

Pelajari seluruh materi ini secara bertahap dan lakukan praktik langsung menggunakan:
- VS Code
- XAMPP/AppServ
- PHP Native
- MySQL/phpMyAdmin

Kunci utama memahami PPB dan Basis Data adalah:
1. Banyak latihan coding
2. Memahami alur logika
3. Sering melakukan debugging
4. Membiasakan praktik CRUD
5. Memahami relasi database

Semangat belajar dan semoga sukses menghadapi SAT!

