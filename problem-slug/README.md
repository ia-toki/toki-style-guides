# TLX Problem Slug Style Guide

> Available in: :indonesia: Bahasa Indonesia

Setiap soal pada TLX memiliki sebuah *identifier* (pengenal) berupa sebuah string yang disebut *slug*, yang harus berbeda-beda. Biasanya, slug dibentuk dari judul soal, misalnya `tebak-angka`.

Saat ini terdapat banyak kontes pada TLX. Mungkin saja ada dua soal dari dua kontes berbeda yang memiliki judul yang sama. Sebagai contoh, `Tebak Angka` adalah judul soal yang lumayan umum. Menggunakan `tebak-angka` sebagai slug tentu bukanlah ide yang baik.

Dokumen ini ditulis agar dua soal yang berbeda (walaupun dengan judul soal yang sama) tidak memiliki slug yang sama, dan gayanya konsisten.

## Daftar Isi

- [1. Aturan Umum](#1-aturan-umum)
- [2. Soal Kontes](#2-soal-kontes)
  - [2.1. Soal Kontes yang Sudah Lewat atau Akan Datang](#21-soal-kontes-yang-sudah-lewat-atau-akan-datang)
  - [2.2. Modifikasi dari Soal Kontes yang Sudah Lewat](#22-modifikasi-dari-soal-kontes-yang-sudah-lewat)
- [3. Soal Lainnya](#3-soal-lainnya)
  - [3.1. Soal Belum Terpakai](#31-soal-belum-terpakai)
  - [3.2. Soal Coba-Coba](#32-soal-coba-coba)
  - [3.3. Soal Tidak Dipakai](#33-soal-tidak-dipakai)

## 1. Aturan Umum

Slug harus terdiri atas beberapa kata yang dipisahkan oleh `-`. Setiap kata harus tersusun atas satu atau lebih karakter huruf kecil, angka, atau keduanya.

- Contoh :+1:: `a-plus-b`, `tree-reconstruction`, `2sat-construction`.
- Contoh :x:: `a+b`, `tree--reconstruction`, `2SAT-construction`.

## 2. Soal Kontes

### 2.1. Soal Kontes yang Sudah Lewat atau Akan Datang

Jika Anda ingin meletakkan:

- soal pada kontes yang sudah lewat, misalnya untuk arsip soal ICPC,
- soal baru untuk digunakan pada kontes yang akan datang, misalnya TROC bulan depan,

maka slug soal harus mengikuti format berikut:

`<nama kontes>-<nama soal>`

Contoh :+1:: `ksn-2020-mencari-bola`, `icpc-jakarta-2020-police`, `troc-22-near`.

- **2.1.2. Bagian** `<nama kontes>`

  Bagian ini harus mengidentifikasikan kontes secara **unik** pada TLX. Selain itu, kontes yang serupa sebaiknya memiliki format yang serupa. Sebagai contoh, format untuk kontes TOKI Open Contest selalu berupa `toc-<tahun>-<bulan>`.

  - Contoh :+1:: `ksn-2020`, `icpc-jakarta-2020`, `troc-22`, `toc-2018-feb`.
  - Contoh :x:: `ksn`, `icpc-jakarta`, `troc`, `toc-2018`.

- **2.1.3. Bagian** `<nama soal>`

  Bagian ini harus mengidentifikasikan soal secara **unik** pada kontes di mana soal ini digunakan. Sebaiknya terdiri atas satu atau dua kata kunci yang diambil dari judul soal.

  - Contoh :+1:: `mencari-bola`, `police`, `near`
  - Contoh :x:: `a`, `b`, `pohon-merah-hitam`,  `daratan-dan-es`

### 2.2. Modifikasi dari Soal Kontes yang Sudah Lewat

Jika Anda memodifikasi soal kontes yang sudah lewat, misalnya:

- batasan dari soal asli diubah menjadi soal modifikasi yang menjadi lebih sulit (atau lebih mudah),
- soal asli menggunakan penilaian ICPC (tidak terdapat subsoal) dan dimodifikasi menjadi soal yang menggunakan penilaian IOI (terdapat subsoal),

maka slug soal modifikasi ini harus mengikuti format berikut:

- `<slug-soal-asli>-modified`
- `<slug-soal-asli>-modified-<indeks>` (jika terdapat lebih dari satu modifikasi)

Sebagai contoh, soal modifikasi pada soal `troc-22-near` memiliki slug:

- `troc-22-near-modified`
- `troc-22-near-modified-2` (modifikasi kedua)

## 3. Soal Lainnya

### 3.1. Soal Belum Terpakai

Jika soal bukan/belum merupakan kontes pada TLX, maka slug harus diawali dengan `<username TLX Anda>-`. Jika username TLX Anda memiliki karakter yang bukan merupakan karakter huruf kecil atau angka, maka Anda harus mengabaikan karakter-karakter tersebut.

Sebagai contoh, jika username TLX Anda adalah `dengklek`, lalu Anda membuat soal pribadi yang belum dipakai untuk kontes apapun berjudul `Halo Dunia`, maka Anda dapat menggunakan slug `dengklek-halo-dunia`. Jika nantinya soal ini digunakan untuk suatu kontes (misalnya TROC), Anda dapat mengganti slugnya.

Contoh :+1:: `dengklek-halo-dunia`.

### 3.2. Soal Coba-Coba

Jika Anda membuat soal yang digunakan untuk mencoba-coba saja, maka slug soal harus diawali dengan `<username TLX Anda>-TESTING`.

Diharapkan untuk meminimalkan banyaknya soal coba-coba yang Anda buat. Jika Anda sudah pernah membuat soal coba-coba sebelumnya dan ingin melakukan coba-coba kembali, gunakan ulang soal coba-coba yang sudah Anda buat sebelumnya.

Contoh :+1:: `dengklek-TESTING-grader`.

### 3.3. Soal Tidak Dipakai

Jika soal yang Anda buat sudah tidak dipakai lagi (misalnya Anda membuat kesalahan commit dan tidak bisa di-revert), maka slug soal harus diawali dengan `<username TLX Anda>-UNUSED`.

Soal dengan slug yang mengandung substring `UNUSED` dapat dihapus kapan saja dari TLX jika dibutuhkan (misalnya jika TLX kehabisan *storage*).

Contoh :+1:: `dengklek-UNUSED-commit-error`.

---

Dokumen ini ditulis oleh:

- Ashar Fuadi
- Jonathan Irvin Gunawan
