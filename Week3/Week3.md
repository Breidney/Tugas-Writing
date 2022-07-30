# Rekursif

Apa itu rekursif?

Mudahnya, rekursif adalah suatu teknik pemrograman yang menggunakan function atau fungsi. Sederhananya adalah fungsi yang memanggil fungsi tersebut atau dirinya sendiri, seolah-olah terjadi suatu perulangan. Proses pemanggilan inilah yang disebut sebagai recursion (rekursi) dan akan terus dilakukan sampai pada kondisi yang sudah ditentukan. Contoh sederhananya adalah sebagai berikut:

``function rekursif() {
  // kode lainnya
  rekursif();
}``

Pada kode di atas dapat dilihat bahwa terdapat fungsi bernama rekursif() yang di dalamnya memanggil fungsi rekursif() itu sendiri. Sehingga jika dianalogikan dengan gambar, terlihat seperti gambar di bawah ini:

<img src="https://skilvul-assets-01.s3-ap-southeast-1.amazonaws.com/lesson/js-intermediate/recursive.png">

"Seperti cermin yang saling berhadapan, sehingga menyebabkan pantulan cermin terus menerus (cermin di dalam cermin)."

Membuat Rekursif
Seperti yang kita ketahui, rekursif adalah pemanggilan fungsi yang berulang. Function yang menerapkan cara rekursif disebut juga dengan recursive function. Jika recursive function tersebut memanggil dirinya sendiri, akan terjadi infinity recursion (rekursi tak hingga). Maka dari itu ada beberapa hal yang harus diperhatikan dalam membuat recursive function.

Algoritma rekursif mempunyai 2 komponen utama, yaitu:

Base Case
Kasus dasar untuk menyelesaikan permasalahan. Base case akan dikunjungi jika rekursi berakhir (kondisi untuk berhenti terpenuhi), serta mengembalikan nilai tanpa melakukan rekursi kembali.

Recursion Call
Permasalahan yang ada tentunya akan diperkecil dengan melakukan pemanggilan function itu sendiri (recursion call). Permasalahan dapat diperkecil dengan mengurangi atau memecahkan data input pada setiap pemanggilannya hingga mencapai base case.

# Regex

Apa itu Regex?
Regular Expression atau disebut juga Regex / Regexp adalah deretan karakter spesial yang menggambarkan pattern atau pola untuk pencarian teks pada sebuah string atau document.

Regex = Text matching.

Kapan sih kita harus menggunakan regex?

1. Validasi input dari sebuah form
2. Mencari keyword tertentu pada email atau halaman website
3. Mencari IP address dalam kisaran tertentu
4. Dan masih banyak lagi
Cara membuat pola regex
Ada dua cara untuk membuat regex, kita bisa menggunakan regex literal dengan menuliskan pola yang ingin dicari di antara dua slash / seperti ini:

 ``const namaVariable = /pola/;
atau bisa juga menggunakan fungsi RegExp seperti ini:

const namaVariable = new RegExp("pola");``

# OOP

Secara umum tipe data terbagi menjadi 2, yaitu tipe data primitive dan non primitive.

- Tipe data primitive adalah tipe data yang hanya dipakai untuk menyimpan data seperti: byte, short, int, long, float, double, boolean dan char.
- Tipe data non primitive adalah tipe data yang selain dipakai untuk menyimpan data, tetapi juga mempunyai metode bawaan (built-in method) untuk dilakukan modifikasi dan operasi oleh programmer, seperti: String, Array, Class dan Object.

Apa itu OOP?
OOP adalah suatu paradigma atau konsep di dunia pemrograman yang berorientasikan pada objek. Biasanya objek memiliki 2 komponen, yaitu ciri-ciri dari objek tersebut (properti) dan kemampuan yang dapat dilakukan oleh objek tersebut (method).

Contohnya pada dunia nyata terdapat objek makhluk hidup seperti manusia yang memiliki nama, umur, dan** jenis kelamin**. Manusia juga dapat melakukan aktifitas seperti tidur, belajar, bermain dan sebagainya.

<img src="https://skilvul-assets-01.s3-ap-southeast-1.amazonaws.com/lesson/js-intermediate/oop.png">

Kenapa harus menggunakan OOP?
Aplikasi yang dibuat semakin lama akan semakin besar dan baris kodenya pun semakin lama akan semakin banyak. Maka dari itu, kamu membutuhkan teknik baru untuk dapat mengatur manajemen kode yang kamu punya sehingga akan lebih mudah dikembangkan dan dilakukan update.

OOP juga banyak digunakan pada bahasa pemrograman lain seperti Java, C++, C#, Kotlin, dan masih banyak lagi. Di topik selanjutnya kamu akan mempelajari pemahaman dasar dari OOP dan cara penerapannya pada bahasa pemrograman JavaScript.

"📝  Catatan:

JavaScript tidak sepenuhnya mendukung konsep OOP, tapi kamu akan mempelajari pemahaman dasar dari paradigma OOP."

# Asynchronous

Asynchronous yang biasa dikenal juga dengan sebutan non-blocking mengizinkan komputer kita untuk memproses perintah lain sambil menunggu suatu proses lain yang sedang berlangsung. Ini artinya kita bisa melakukan lebih dari 1 proses sekaligus (multi-thread). Eksekusi perintah dengan asynchronous tidak akan melakukan blocking atau menunggu perintah sebelumnya selesai. Jadi sambil menunggu kita bisa mengeksekusi perintah lain.

Analoginya seperti saat kita mencuci baju di mesin cuci. Agar lebih produktif, sambil menunggu cucian selesai kita bisa melakukan pekerjaan lain misalnya menyapu dan mengepel. Artinya disini kita melakukan 3 proses sekaligus.

Untuk lebih jelasnya, mari kita lihat perbedaan jika menggunakan asynchronous dengan synchronous dengan memperhatikan waktu eksekusi perintah:

<!DOCTYPE html>
<html lang="en">
<head>
</head>
<body>
    <table border="1">
        <tr>
            <td>perintah</td>
            <td>waktu proses detik</td>
        </tr>
        <tr>
            <td>a</td>
            <td>2</td>
        </tr>
        <tr>
            <td>b</td>
            <td>3</td>
        </tr>
        <tr>
            <td>c</td>
            <td>2</td>
        </tr>
    </table>
</body>
</html>

Jika perintah di atas dieksekusi dengan perintah synchronous, maka eksekusi perintahnya akan terlihat seperti ini:

<img src="https://skilvul-assets-01.s3-ap-southeast-1.amazonaws.com/lesson/js-intermediate/async-intro-1.png">

Dari gambar di atas, kita dapat lihat bahwa **setiap perintah dijalankan sampai selesai terlebih dahulu, baru mengeksekusi perintah selanjutnya**, sehingga **membutuhkan waktu 7 detik** untuk menyelesaikan semua perintah.
Namun, jika perintah di atas dijalankan secara asynchronous, maka eksekusi perintahnya akan terlihat seperti ini:

<img src="https://skilvul-assets-01.s3-ap-southeast-1.amazonaws.com/lesson/js-intermediate/async-intro-2.png">

Dari gambar di atas, kita dapat lihat bahwa setiap perintah dijalankan saat perintah yang lain juga sedang dijalankan, sehingga membutuhkan waktu 4 detik untuk menyelesaikan semua perintah.

## Menjalankan Asynchronous pada JavaScript

Jika JavaScript secara default bersifat synchronous, maka bagaimana jika ingin menerapkan proses asynchronous ? Ada beberapa cara untuk membuat proses asynchronous. Kami membatasi hanya memberikan 2 cara ini:

1. setTimeout(function, milliseconds) digunakan untuk simulasi pemanggilan kembali proses asynchronous yang sedang/sudah selesai dijalankan. Pemanggilan hanya dilakukan 1 kali.
2. setInterval(function, milliseconds) digunakan untuk simulasi pemanggilan proses asynchronous yang sedang/sudah dijalankan dalam interval waktu tertentu. Pemanggilan dilakukan berkali-kali sesuai interval waktu yang ditentukan.

Contoh asynchronous menggunakan setTimeout():

setTimeout(() => {

  console.log("Cuci baju"); // proses 
  asynchronous

}, 1000);

console.log("Menyapu");

console.log("Mengepel");

console.log("Memasak");

// 1000 ms = 1 second

// Output:
// Menyapu
// Mengepel
// Memasak
// Cuci baju


Contoh asynchronous menggunakan setInterval():

setInterval(() => {

  console.log("Cuci baju"); // proses asynchronous

}, 3000);

console.log("Menyapu");

console.log("Mengepel");

console.log("Memasak");

// 3000 ms = 3 second

// Output:

// Menyapu

// Mengepel

// Memasak

// Cuci baju (x time)

// Cuci baju akan dijalankan setiap 3 detik sekali

Kita bisa lihat bahwa hasilnya urutan pertama adalah Menyapu, Mengepel, Memasak, dan Cuci Baju. Ini terjadi karena cara kerja asynchronous tidak akan menunggu suatu perintah sampai selesai, namun langsung mengeksekusi perintah lainnya.

Dari contoh simulasi di atas model eksekusi asynchronous lebih effisien dibandingkan synchronous. Namun, permasalahan terjadi saat menggunakan asynchronous, ada satu perintah yang bergantung pada output eksekusi asynchronous sebelumnya. Dengan kata lain fungsi berjalan kejar-kejaran (race condition), sehingga data yang kita inginkan menjadi kosong. Sebagai contoh:

const user = getUser(); // fungsi async untuk mengambil data user dari API
console.log(user) // Output: null

Dari kode di atas, ada kemungkinan user masih bernilai null. Hal ini terjadi karena fungsi getUser() adalah fungsi asynchronous yang belum selesai dijalankan, namun perintah console.log() sudah menuntut untuk dijalankan.

Untuk mengatasi masalah tersebut, kita dapat menggunakan:

1. Callback.
2. Promises.
3. Async / Await.

Lalu dalam kondisi apa saja kita perlu menggunakan asynchronous? Teknik asynchronous paling banyak digunakan dalam mengelola komunikasi ke server seperti proses request API (mengambil data dari server), operasi file, koneksi ke database, real time communication (messenger/chat), dan sebagainya.