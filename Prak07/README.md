# Praktikum 07 — Pemodelan Relasi Objek dan UML

**Nama: Syabita Putri Safina**
**NPM: 4525210072**
**Mata Kuliah: Pemrograman Berorientasi Objek**
**Dosen Pengampu: Adi Wahyu Pribadi, S.Si., M.Kom**

## 1. Buku.java

### Pengertian
`Buku.java` merupakan kelas yang merepresentasikan sebuah buku dalam program. Kelas ini digunakan untuk menyimpan informasi buku dan mengelola bab-bab yang menjadi bagian dari buku tersebut.

### Penjelasan Kode
Kelas `Buku` menerapkan konsep **komposisi (composition)**, yaitu hubungan ketika suatu objek memiliki objek lain sebagai bagian yang dikelolanya. Dalam contoh ini, objek `Buku` mengelola objek `Bab`, sehingga bab menjadi bagian dari buku.

## 2. Jurusan.java

### Pengertian
`Jurusan.java` merupakan kelas yang merepresentasikan jurusan dalam lingkungan akademik. Kelas ini digunakan untuk mengelola data mahasiswa yang terdaftar pada jurusan tersebut.

### Penjelasan Kode
Kelas `Jurusan` menerapkan konsep **agregasi (aggregation)**, yaitu hubungan ketika sebuah objek memiliki hubungan dengan objek lain yang tetap dapat berdiri sendiri. Dalam contoh ini, objek `Mahasiswa` dapat dibuat secara terpisah dan tetap ada meskipun tidak lagi terdaftar pada suatu jurusan.


## 3. PerpustakaanService.java

### Pengertian
`PerpustakaanService.java` merupakan kelas layanan yang berfungsi mengatur proses pengelolaan data buku dalam sistem perpustakaan.

### Penjelasan Kode
Kelas ini menjadi perantara untuk menjalankan fungsi-fungsi yang berkaitan dengan buku, seperti mengelola koleksi, mencari buku berdasarkan nomor induk, serta menangani proses peminjaman dan pengembalian apabila fungsi tersebut tersedia dalam implementasi program.

## 4. Main.java

### Pengertian
`Main.java` merupakan kelas utama yang digunakan sebagai titik awal untuk menjalankan program Java.

### Penjelasan Kode
Kelas ini digunakan untuk membuat objek dan menguji penerapan komposisi serta agregasi. Melalui program utama, hubungan antara objek buku dan bab serta jurusan dan mahasiswa dapat diamati berdasarkan hasil eksekusi program.

## 5. relasi.php

### Pengertian
`relasi.php` merupakan file PHP yang digunakan untuk mendefinisikan kelas-kelas dan hubungan antarobjek dalam program.

### Penjelasan Kode
File ini menerapkan konsep pemrograman berorientasi objek menggunakan PHP. Hubungan komposisi dan agregasi ditunjukkan melalui interaksi antarobjek yang dibuat berdasarkan kelas masing-masing.

## 6. main.php

### Pengertian
`main.php` merupakan file utama yang digunakan untuk menjalankan program PHP dan menampilkan hasil penerapan relasi antarobjek.

### Penjelasan Kode
File ini membuat objek dari kelas yang telah didefinisikan, kemudian menjalankan proses untuk memperlihatkan hubungan komposisi dan agregasi. Hasilnya digunakan untuk mengamati perilaku objek saat program dijalankan.


## 7. UML Class Diagram

### Pengertian
UML (*Unified Modeling Language*) merupakan bahasa pemodelan yang digunakan untuk menggambarkan struktur dan hubungan antarbagian dalam suatu sistem perangkat lunak.

### Penjelasan
Class diagram menunjukkan kelas-kelas yang digunakan dalam sistem, atribut dan method yang dimiliki, serta hubungan antarobjek. Pada praktikum ini, diagram digunakan untuk menggambarkan relasi komposisi dan agregasi sebelum atau selama penerapannya dalam kode program.

## 8. Screenshot Hasil Keseluruhan

### Hasil Program Java
Masukkan screenshot hasil eksekusi program Java di sini.

### Hasil Program PHP
Masukkan screenshot hasil eksekusi program PHP di sini.

## Kesimpulan

Praktikum ini membahas penerapan konsep komposisi dan agregasi dalam pemrograman berorientasi objek menggunakan Java dan PHP. Komposisi menunjukkan hubungan ketika suatu objek mengelola objek lain sebagai bagian dari dirinya, sedangkan agregasi menunjukkan hubungan ketika objek yang terlibat tetap dapat berdiri sendiri. UML class diagram membantu menggambarkan struktur kelas dan hubungan tersebut agar implementasi program lebih mudah dipahami.