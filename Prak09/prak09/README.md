# **Praktikum Pertemuan — Package, Namespace, dan Build Tool**

**Nama:** Syabita Putri Safina  
**NPM:** 4525210072  
**Mata Kuliah:** Pemrograman Berorientasi Objek  
**Dosen Pengampu:** Adi Wahyu Pribadi, S.Si., M.Kom

## **1. Penjelasan Materi**

### **Package**

Package merupakan fitur Java yang digunakan untuk mengelompokkan class berdasarkan fungsi tertentu. Package membuat struktur program menjadi lebih terorganisasi dan memudahkan pengelolaan class.

Pada program perpustakaan ini, package dibagi menjadi beberapa bagian, yaitu `model`, `service`, dan `util`.

### **Namespace**

Namespace merupakan ruang lingkup penamaan yang digunakan untuk membedakan identifier agar tidak terjadi konflik nama.

Dalam Java, konsep namespace diterapkan melalui package. Package membantu membedakan class berdasarkan lokasi dan kelompoknya.

### **Build Tool**

Build tool merupakan alat yang membantu proses pembangunan aplikasi, seperti kompilasi program dan pengelolaan dependency.

Pada praktikum ini digunakan Maven sebagai build tool. Maven mengatur konfigurasi project melalui file `pom.xml` dan membantu mengelola library yang digunakan oleh program.

## **2. Penjelasan File Program**

### **File `Anggota.java`**

#### **Sebelum Perbaikan**

Class `Anggota` digunakan untuk menyimpan data anggota perpustakaan, seperti nomor anggota, nama, dan jenis keanggotaan. Data anggota perlu dijaga agar tidak memiliki nilai kosong.

#### **Setelah Perbaikan**

Class `Anggota` menggunakan atribut `final` agar data utama anggota tidak dapat diubah setelah objek dibuat. Validasi juga ditambahkan untuk memastikan nomor anggota dan nama tidak kosong. Method getter digunakan untuk mengambil data anggota.

**Screenshot hasil running:**

<!-- Masukkan screenshot di sini -->

### **File `Buku.java`**

#### **Sebelum Perbaikan**

Class `Buku` digunakan untuk menyimpan informasi buku perpustakaan, seperti nomor induk, judul, penulis, dan jumlah eksemplar. Data buku juga perlu dikelola agar stok tidak bernilai negatif.

#### **Setelah Perbaikan**

Class `Buku` dilengkapi dengan validasi jumlah stok, method untuk menambah dan mengurangi stok, serta pengecekan ketersediaan buku. Class ini juga memiliki fitur untuk menambahkan bab buku dan menampilkan daftar bab secara aman.

**Screenshot hasil running:**

<!-- Masukkan screenshot di sini -->

### **File `Peminjaman.java`**

#### **Sebelum Perbaikan**

Class `Peminjaman` digunakan untuk menyimpan informasi transaksi peminjaman buku, termasuk anggota yang meminjam, buku yang dipinjam, tanggal peminjaman, dan tanggal jatuh tempo.

#### **Setelah Perbaikan**

Class `Peminjaman` dilengkapi dengan validasi data peminjaman dan perhitungan tanggal jatuh tempo berdasarkan lama peminjaman. Class ini juga memiliki atribut tanggal kembali untuk mengetahui apakah buku sudah dikembalikan.

**Screenshot hasil running:**

<!-- Masukkan screenshot di sini -->

### **File `PerpustakaanService.java`**

#### **Sebelum Perbaikan**

Class `PerpustakaanService` digunakan untuk mengelola proses utama dalam sistem perpustakaan, seperti pengelolaan koleksi buku, pendaftaran anggota, serta transaksi peminjaman dan pengembalian.

#### **Setelah Perbaikan**

Class ini dilengkapi dengan fitur pencarian buku dan anggota, validasi peminjaman, pembatasan maksimal tiga peminjaman aktif, serta pengelolaan stok buku. Sistem juga menghitung denda keterlambatan berdasarkan jenis keanggotaan.

**Screenshot hasil running:**

<!-- Masukkan screenshot di sini -->

### **File `Format.java`**

#### **Sebelum Perbaikan**

Class `Format` digunakan untuk membantu proses pemformatan data agar tampilan informasi lebih mudah dibaca.

#### **Setelah Perbaikan**

Class `Format` menyediakan method untuk mengubah angka menjadi format mata uang Rupiah dan mengubah tanggal menjadi format tanggal Indonesia. Class ini dibuat sebagai utility class dengan method static sehingga dapat digunakan tanpa membuat objek.

**Screenshot hasil running:**

<!-- Masukkan screenshot di sini -->

### **File `App.java`**

#### **Sebelum Perbaikan**

Class `App` merupakan bagian utama program yang digunakan untuk menjalankan sistem perpustakaan. Class ini menghubungkan data buku, anggota, peminjaman, dan layanan perpustakaan.

#### **Setelah Perbaikan**

Class `App` digunakan untuk menjalankan simulasi sistem perpustakaan. Program menambahkan data buku dan anggota, melakukan transaksi peminjaman dan pengembalian, serta menampilkan data dalam bentuk tabel menggunakan library `AsciiTable`.

**Screenshot hasil running:**

<!-- Masukkan screenshot hasil running program di sini -->

## **3. Hasil Pengujian Program**

### **Hasil Java**

<!-- Masukkan screenshot hasil running Java di sini -->

## **4. Kesimpulan**

Berdasarkan praktikum yang telah dilakukan, package dapat digunakan untuk mengelompokkan class agar program lebih terorganisasi. Konsep namespace membantu membedakan penamaan class, sedangkan Maven sebagai build tool mempermudah pengelolaan project dan dependency. Penerapan konsep tersebut membantu membangun sistem perpustakaan yang lebih terstruktur dan mudah dikembangkan.