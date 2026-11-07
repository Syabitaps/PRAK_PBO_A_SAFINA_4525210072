# LAPORAN PRAKTIKUM PEMROGRAMAN BERORIENTASI OBJEK

## Praktikum Pertemuan 10 — Exception Handling dan Pemrograman Defensif

**Nama:** Syabita Putri Safina  
**NPM:** 4525210072    
**Mata Kuliah:** Pemrograman Berorientasi Objek  
**Dosen Pengampu:** Adi Wahyu Pribadi, S.Si., M.Kom.

---

## 1. Tujuan Praktikum

Praktikum ini bertujuan untuk memahami penggunaan Exception Handling dalam pemrograman Java dan PHP. Selain itu, praktikum ini melatih penerapan pemrograman defensif agar program dapat menangani kesalahan dengan baik, memberikan informasi penyebab kesalahan, serta tetap berjalan sesuai alur yang diharapkan.

## 2. Dasar Teori

### A. Exception Handling

Exception Handling merupakan mekanisme untuk menangani kesalahan yang terjadi saat program dijalankan. Dengan mekanisme ini, program dapat memberikan pesan kesalahan tanpa harus langsung berhenti secara tiba-tiba.

### B. Try, Catch, dan Finally

- **Try:** Digunakan untuk menampung kode yang berpotensi menghasilkan kesalahan.
- **Catch:** Digunakan untuk menangkap dan menangani kesalahan yang terjadi.
- **Finally:** Digunakan untuk menjalankan kode yang tetap harus dilakukan, baik terjadi kesalahan maupun tidak.

### C. Throw dan Custom Exception

`throw` digunakan untuk melempar exception ketika suatu kondisi tidak terpenuhi. Custom Exception merupakan exception yang dibuat sendiri sesuai kebutuhan program agar penyebab kesalahan dapat dijelaskan secara lebih spesifik.

### D. Guard Clause

Guard Clause merupakan teknik penulisan kode dengan memeriksa kondisi yang tidak memenuhi syarat di bagian awal method. Teknik ini membantu mengurangi penggunaan percabangan bersarang sehingga kode lebih mudah dibaca dan dipahami.

### E. Try-with-resources

Try-with-resources merupakan fitur Java yang digunakan untuk mengelola resource secara otomatis. Resource seperti file akan ditutup secara otomatis setelah proses selesai, termasuk ketika terjadi kesalahan.

## 3. Alat dan Bahan

1. Laptop atau komputer.
2. Visual Studio Code.
3. Java Development Kit (JDK).
4. Apache Maven.
5. PHP.
6. Composer.
7. Terminal untuk menjalankan program.

## 4. Struktur Proyek

```text
Prak 10/
│
├── java/
│   ├── pom.xml
│   └── src/
│       └── main/
│           └── java/
│               └── id/ac/univpancasila/perpustakaan/
│                   ├── Main.java
│                   ├── exception/
│                   │   ├── PerpustakaanException.java
│                   │   ├── AnggotaTidakDitemukanException.java
│                   │   ├── BatasPinjamTerlampauiException.java
│                   │   ├── BukuSedangDipinjamException.java
│                   │   └── BukuTidakDitemukanException.java
│                   └── service/
│                       ├── LibraryServiceKotor.java
│                       ├── LibraryService.java
│                       └── PerpustakaanService.java
│
├── php/
│   ├── Main.php
│   ├── composer.json
│   └── src/
│       ├── Exception/
│       └── Service/
│
└── README.md
```

## 5. Pembahasan dan Hasil Praktikum

### A. Penerapan Exception Handling pada Java

Pada bagian Java, program menggunakan Exception Handling untuk menangani berbagai kesalahan dalam proses peminjaman buku. Beberapa kondisi yang ditangani antara lain anggota tidak ditemukan, buku tidak ditemukan, stok buku habis, dan anggota telah mencapai batas maksimal peminjaman.

**File yang digunakan:**

- `PerpustakaanException.java`: Menjadi kelas induk untuk seluruh exception khusus perpustakaan.
- `AnggotaTidakDitemukanException.java`: Menangani kondisi anggota yang belum terdaftar.
- `BukuTidakDitemukanException.java`: Menangani kondisi ISBN buku yang tidak tersedia dalam katalog.
- `BukuSedangDipinjamException.java`: Menangani kondisi stok buku yang sudah habis.
- `BatasPinjamTerlampauiException.java`: Menangani kondisi anggota yang telah mencapai batas maksimal peminjaman.

### B. Perbaikan Struktur Kode dengan Guard Clause

**Sebelum Perbaikan**

Pada file `LibraryServiceKotor.java`, proses peminjaman buku masih menggunakan percabangan `if` bersarang hingga beberapa tingkat. Setiap kondisi yang tidak terpenuhi hanya mengembalikan nilai `false`, sehingga pemanggil tidak mengetahui alasan kegagalan peminjaman.

**Setelah Perbaikan**

Pada file `LibraryService.java`, struktur kode diperbaiki menggunakan Guard Clause. Setiap kondisi diperiksa pada bagian awal method dan akan melempar Custom Exception apabila persyaratan tidak terpenuhi. Dengan demikian, kode menjadi lebih sederhana dan penyebab kesalahan dapat diketahui dengan jelas.

### C. Pengelolaan Proses Peminjaman

File `PerpustakaanService.java` berfungsi mengelola proses input data anggota, penambahan buku, dan peminjaman buku. Program menggunakan `try-catch` untuk menangani exception yang muncul sehingga pengguna dapat mengetahui pesan kesalahan yang terjadi.

### D. Pengelolaan File dengan Try-with-resources

Pada file `Main.java`, program menggunakan Try-with-resources untuk membuat laporan daftar buku ke dalam file `laporan_buku.txt`. Data yang disimpan meliputi ISBN, judul buku, jumlah stok, dan status ketersediaan buku.

Penggunaan Try-with-resources membantu memastikan file ditutup secara otomatis setelah proses penulisan selesai. Program juga menggunakan `catch` untuk menangani kesalahan ketika proses penulisan file mengalami masalah.

### E. Implementasi Exception Handling pada PHP

Pada bagian PHP, konsep Exception Handling diterapkan menggunakan namespace dan autoloading PSR-4 melalui Composer.

File `LibraryServiceKotor.php` merupakan contoh kode sebelum perbaikan, sedangkan `LibraryService.php` merupakan hasil refactoring menggunakan Guard Clause dan Custom Exception.

File `Main.php` digunakan untuk menjalankan beberapa percobaan peminjaman buku. Program juga menggunakan `try-catch-finally` dalam proses pembuatan laporan agar file dapat ditutup dengan aman setelah digunakan.

## 6. Kesimpulan

Berdasarkan praktikum yang telah dilakukan, Exception Handling dapat digunakan untuk menangani kesalahan dalam program dengan lebih terstruktur. Penerapan Custom Exception membantu memberikan informasi penyebab kesalahan secara spesifik, sedangkan Guard Clause membuat struktur kode lebih sederhana dan mudah dipahami. Selain itu, penggunaan Try-with-resources pada Java dan Try-Catch-Finally pada PHP membantu mengelola file dengan lebih aman. Dengan demikian, program menjadi lebih terstruktur, mudah dipelihara, dan mampu menangani berbagai kondisi kesalahan dengan baik.