# Keputusan Praktikum Pertemuan 06

## 1. Mengapa Java hanya mengizinkan satu superclass?

Java hanya mengizinkan sebuah class mewarisi satu superclass agar struktur pewarisan lebih jelas dan menghindari konflik jika beberapa superclass memiliki atribut atau method yang sama. Namun, sebuah class dapat mengimplementasikan beberapa interface sekaligus.

## 2. Mengapa `isiPenuh($sepeda)` menghasilkan TypeError pada PHP?

Fungsi `isiPenuh()` memiliki parameter bertipe `Fuelable`. Class `Mobil` mengimplementasikan interface `Fuelable`, sehingga objek `Mobil` dapat digunakan sebagai argumen fungsi tersebut.

Sebaliknya, class `Sepeda` hanya mengimplementasikan interface `Movable`, bukan `Fuelable`. Oleh karena itu, ketika objek `Sepeda` diberikan ke fungsi `isiPenuh()`, PHP menghasilkan `TypeError` karena tipe objek tidak sesuai dengan tipe parameter yang diwajibkan.

Hal ini menunjukkan bahwa interface membantu memastikan objek memiliki kemampuan yang sesuai dengan kebutuhan suatu fungsi.