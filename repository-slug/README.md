# TLX Repository Gate Problem Slug Style Guide

## Daftar Isi

- [Latar Belakang] (#latar-belakang)
- [Batasan] (#batasan)
- [Soal Kontes] (#soal-kontes)
- [Soal Training] (#soal-training)
- [Soal Lainnya] (#soal-lainnya)
- [Lain-lain] (#lain-lain)

## Latar Belakang

[TLX Repository Gate] (https://repository.ia-toki.org/) adalah tempat untuk meletakan soal-soal yang digunakan di TLX, baik [TLX Training Gate] (https://training.ia-toki.org/) maupun [TLX Competition Gate] (https://competition.ia-toki.org/). Sampai dengan 19 Juni 2017 terdapat 200 kontes berbeda yang terdapat di TLX Competition Gate yang mencakup Pelatnas TOKI, Open OSN, TOKI Open, TOKI Open Contest, Bukalapak Programming Contest (BLPC), dan lain lain. Kontes-kontes ini memiliki panitia yang berbeda-beda, dan setiap panitia kontes harus meletakan soal-soalnya di TLX Repository Gate. 

Karena hal itu, terdapat banyak sekali soal yang ada di TLX Repository Gate, tepatnya 1.402 soal sampai dengan 19 Juni 2017. Setiap soal di TLX Repository Gate memiliki sebuah *slug* yang merupakan sebuah string. Karena digunakan sebagai *identifier* (pengenal), slug dari soal yang berbeda tidak boleh sama. 

Terdapat beberapa pasang soal independen (dari kontes yang berbeda) dari 1.402 soal ini yang memiliki judul soal yang mungkin saja sama. Sebagai contoh : `Tebak Angka` adalah judul soal yang lumayan umum walaupun dua soal dengan judul `Tebak Angka` mungkin saja berbeda soalnya. Menggunakan `tebak-angka` sebagai slug bukanlah ide yang baik. Karenanya, dokumen ini dibentuk agar dua soal yang berbeda (walaupun dengan judul soal yang sama) tidak memiliki slug yang sama.

## Batasan

Slug dari sebuah soal harus mengikuti format yang terdapat pada [dokumentasi Judgels pada bagian Problem Components - Slug] (http://judgels.readthedocs.io/en/latest/operator/sandalphon/problem.html#problems-components), yaitu beberapa kata yang dipisahkan oleh `-` yang mana setiap kata tersusun atas beberapa karakter huruf kecil, angka, atau keduanya.

## Soal Kontes

### Soal Kontes akan Datang atau sudah Lewat

Jika Anda ingin meletakan soal pada kontes yang sudah lewat (sebagai contoh : untuk digunakan pada Pelatnas TOKI) atau meletakan soal baru untuk digunakan pada kontes yang akan datang (sebagai contoh : soal untuk TOKI Open Contest yang akan datang), slug soal Anda harus mengikuti format dibawah ini

`<nama kontes>-<nama soal>`

Sebagai contoh, `toki-oc-mei-17-teman-terbaik`, `osn-informatika-2012-sungai-biner`, `gemastik-2016-final-e-irigasi` adalah slug yang baik.

#### Bagian <nama kontes>

Bagian nama kontes harus mengidentifikasikan kontes secara **unik** di mana soal ini digunakan. Sebagai contoh, jika soal ini digunakan untuk TOKI Open Contest Februari 2017, maka `toki-open-contest` adalah contoh yang salah, karena terdapat beberapa TOKI Open Contest. Contoh yang benar adalah `toki-open-contest-feb-2017`, `toki-oc-feb-2017`, atau sebagainya. Walaupun demikian, kontes yang serupa sebaiknya memiliki format yang serupa. Sebagai contoh, bagian slug nama kontes untuk soal TOKI Open Contest selalu menggunakan format `toki-oc-<bulan>-<tahun>`.

#### Bagian <nama soal>

Bagian nama soal harus mengidentifikasikan soal secara **unik** pada kontes di mana soal ini digunakan. Sebagai contoh, jika soal berjudul `Hello World` digunakan untuk sebuah kontes dan pada kontes ini juga terdapat soal berjudul `Hello Lagi`, maka `hello` adalah contoh yang salah, karena terdapat beberapa soal berjudul `hello`. Contoh yang benar adalah `hello-world`, `world`, atau sebagainya.

### Modifikasi dari Soal Kontes yang sudah Lewat

Dalam beberapa kasus, beberapa soal dari kontes yang sudah lewat mungkin saja perlu dimodifikasi, seperti :

- Batasan dari soal asli dapat diubah menjadi soal modifikasi yang menjadi lebih sulit (atau lebih mudah)
- Soal asli menggunakan penilaian ICPC-style (tidak terdapat subtask) dan dimodifikasi menjadi soal yang menggunakan penilaian IOI-style (terdapat subtask)
- Dan lain lain

Dalam kasus ini, slug soal modifikasi ini harus mengikuti format dibawah ini

`<nama kontes di mana soal asli digunakan>-<nama soal asli>-modified`

Soal yang menggunakan format slug `<nama kontes>-<nama soal>` tanpa diikuti dengan kata kunci `modified` harus sama persis dengan soal asli yang bersangkutan agar tidak menimbulkan kebingungan.

## Soal Training

Soal-soal yang digunakan pada Kelas Pembelajaran Pemrograman TLX Training Gate memiliki pengecualian. Soal-soal tersebut diletakan oleh hanya beberapa (sedikit) anggota IA-TOKI yang sudah memiliki konvensi tersendiri.

## Soal Lainnya

Jika soal bukan merupakan soal kontes dan juga tidak digunakan untuk TLX Training Gate, maka slug soal harus diawali dengan `<username TLX Anda>`. Jika username TLX Anda memiliki karakter yang bukan merupakan karakter huruf kecil atau angka, maka Anda harus mengabaikan karakter-karakter tersebut.

### Soal Testing

Jika Anda membuat soal yang digunakan untuk menguji atau mencoba-coba sistem TLX Repository Gate, maka slug soal harus diawali dengan `<username TLX Anda>-TESTING`. Diharap untuk meminimalisasi banyaknya soal testing yang Anda buat. Jika Anda sudah pernah membuat soal testing sebelumnya dan ingin melakukan coba-coba kembali, gunakan ulang soal testing yang sudah Anda buat sebelumnya.

### Soal Tidak Dipakai

Jika soal yang Anda buat sudah tidak dipakai lagi (sebagai contoh : Anda membuat kesalahan commit dan tidak bisa di revert), maka slug soal harus diawali dengan `<username TLX Anda>-UNUSED`. Soal dengan slug yang mengandung substring `UNUSED` dapat dihapus kapan saja dari TLX jika dibutuhkan (sebagai contoh : jika TLX kehabisan storage).

## Lain-lain

Dokumen ini ditulis dan diurus oleh Ashar Fuadi dan Jonathan Irvin Gunawan. Jika Anda merasa ada beberapa bagian dari dokumen ini yang perlu dihapus, diubah, atau ditambahkan, maka Anda dapat menghubungi kami. Jika Anda merasa terdapat kasus khusus yang tidak dicakup oleh dokumen ini, atau kasus khusus yang mana dokumen ini tidak berlaku, Anda juga dapat menghubungi kami.
