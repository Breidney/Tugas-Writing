# __Java Script Dasar__

<img src="https://nextgen.co.id/wp-content/uploads/2020/12/javascript.jpg">

Java Script :
adalah bahasa pemrograman yang digunakan dalam pengembangan website agar lebih dinamis dan interaktif.

### __Ada dua cara, yaitu:__

* Internal JavaScript, yaitu menyisipkan kode JavaScript langsung di dalam file HTML.

```
<!DOCTYPE html>
<html>
  <head>
    <title>Website Pertamaku</title>
  </head>
  <body>
    <h2>JavaScript di dalam body</h2>

    <script>
      console.log("Halo Semua!"); // output : Halo Semua!
    </script>
  </body>
</html>
```

* External JavaScript, yaitu membuat file JavaScript sendiri dan menyambungkannya dengan file HTML.

```
<!-- File index.html -->

<!DOCTYPE html>
<html>
  <head>
    <title>Website Pertamaku</title>
    <script src="script.js"></script>
  </head>
  <body>
    <h2>Hello, World!</h2>
  </body>
</html>
// File script.js

console.log("Halo Semua!"); // output : Halo Semua!
```
### 3 Cara Mendeklarasikan Variabel
- Var 
- Let
- Const 

# __Tipe Data JS__
* string - deretan karakter yang diapit oleh sepasang tanda kutip;
number - bilangan bulat, pecahan, dan lain-lain;

Contoh :

let nama = "Budi";

console.log(nama); // Output: Budi

* boolean - nilai benar dari sebuah pernyataan yang dituliskan sebagai true atau false;

Contoh :

let apakahSudahMakan = false;

console.log(apakahSudahMakan); // Output: false

* null - sebuah nilai yang berarti kosong atau menunjuk pada nilai yang tidak ada;

* undefined - berbeda dari null, undefined menandakan kondisi variabel yang belum diberi sebuah nilai. Jadi pernyataan "nilai variabel itu adalah undefined" sebenarnya kurang tepat, sebab variabelnya memang tidak mempunyai sebuah nilai;

Contoh :

let jumlahAnak;

console.log(jumlahAnak); // Output: undefined

* symbol - sebuah nilai unik yang dihasilkan tiap kali kita memanggil fungsi Symbol(). Nilai unik ini memiliki beberapa kegunaan seperti memberi nomor identifikasi unik dan berperan sebagai nama properti unik sebuah objek;

* object - sebuah kumpulan pasangan properti dan nilai. Seperti objek dalam kehidupan sehari-hari saja. Misalnya objek Apel memiliki properti warna dengan nilai merah.

# __Operator JS :__

## 1. Operator Aritmatika
* Penjumlahan  :

let bilangan1 = 10;

let bilangan2 = 3;

console.log(bilangan1 + bilangan2); // Output: 13

* Pengurangan :

let bilangan1 = 10;

let bilangan2 = 3;

console.log(bilangan1 - bilangan2); // Output: 7

* Perkalian :

let bilangan1 = 10;

let bilangan2 = 3;

console.log(bilangan1 * bilangan2); // Output: 30

* Pembagian :

let bilangan1 = 10;

let bilangan2 = 2;

console.log(bilangan1 / bilangan2); // Output: 5

* Berpangkat  :

let bilangan1 = 10;

let bilangan2 = 3;

console.log(bilangan1 ** bilangan2); // Output: 1000

* Modulus :

let bilangan1 = 10;

let bilangan2 = 3;

console.log(bilangan1 % bilangan2); // Output: 1

* Increment (Tambah 1)

let bilangan = 10;

bilangan++;

console.log(bilangan); // Output: 11

* Decrement (Kurang 1)

let bilangan = 10;

bilangan--;

console.log(bilangan); // output: 9

## 2. Assignment Operator

* (==)	sama dengan (cek nilai)

* (===)	sama dengan (cek nilai dan tipe data)

* (!=)	tidak sama dengan (cek nilai)

* (!==)	tidak sama dengan (cek nilai dan tipe data)

* ```>```	lebih dari

* ```<```	kurang 

* ```>=```	lebih dari atau sama dengan

* (<=)	kurang dari atau sama dengan

* ? :	ternary operator

contoh :

let makanan = "daging";

let jenisHewan = makanan === "daging"  ? "karnivora" : "herbivora";

console.log(jenisHewan); // Output: "karnivora"

# __Operator Logika__

<!DOCTYPE html>
<html lang="en">
<head>
</head>
<body>
    <table border="1">
        <tr>
            <td>Operator</td>
            <td>Kondisi1</td>
            <td>Kondisi2</td>
            <td>Hasil</td>
        </tr>
        <tr>
            <td>&&</td>
            <td>True</td>
            <td>True</td>
            <td>True</td>
        </tr>
        <tr>
            <td>&&</td>
            <td>True</td>
            <td>False</td>
            <td>False</td>
        </tr>
        <tr>
            <td>&&</td>
            <td>False</td>
            <td>True</td>
            <td>False</td>
        </tr>
        <tr>
            <td>&&</td>
            <td>False</td>
            <td>False</td>
            <td>False</td>
        </tr>
        <tr>
            <td>||</td>
            <td>True</td>
            <td>True</td>
            <td>True</td>
        </tr>
        <tr>
            <td>||</td>
            <td>True</td>
            <td>False</td>
            <td>True</td>
        </tr>
        <tr>
            <td>||</td>
            <td>False</td>
            <td>True</td>
            <td>True</td>
        </tr>
        <tr>
            <td>||</td>
            <td>False</td>
            <td>False</td>
            <td>False</td>
        </tr>
        <tr>
            <td>!</td>
            <td>True</td>
            <td>-</td>
            <td>False</td>
        </tr>
        <tr>
            <td>!</td>
            <td>False</td>
            <td>-</td>
            <td>True</td>
        </tr>
    </table>
</body>
</html>

# __Function JS__

Fungsi pada JavaScript adalah sekumpulan kode yang dirancang untuk melakukan tugas tertentu. Sebuah fungsi JavaScript dijalankan ketika ada yang memanggilnya.

* Mendeklarasikan Function

function namaSaya (){
  console.log("brey")
}
namaSaya();//output : "brey"

* Parameter dan Argument

function operasiPerkalian(angka1, angka2){
  return angka1 * angka2;
}

console.log(operasiPerkalian(2, 6)) // Output: 12

Penjelasan :

"angka1 & angka2 adalah parameter. Pada contoh di atas, parameter harus bertipe number, agar bisa diolah oleh fungsi, yaitu perkalian kedua parameter."

"2 & 6 adalah argument"

# Java Script DOM

DOM adalah singkatan dari Document Object Model.

<img src="https://skilvul-assets-01.s3-ap-southeast-1.amazonaws.com/lesson/intro-to-javascript/the-html-dom-tree-of-objects.png">

Dengan adanya DOM ini, JavaScript diberi akses untuk membuat HTML menjadi dinamis, seperti:

Mengubah element HTML pada halaman website.
Mengubah attribute HTML pada halaman website.
Mengubah CSS style pada halaman website.
Menambah dan/atau menghapus element maupun attribute HTML.
Menambah HTML event (contoh: efek klik pada mouse, hover pada mouse, dan lain-lain) pada halaman website.
Berinteraksi dengan semua HTML event di website.
Di HTML DOM, semua element HTML dari sebuah website dianggap sebagai objek. Dan sama seperti objek JavaScript pada umumnya, objek element HTML di HTML DOM juga mempunyai properti dan method atau yang lebih dikenal dengan istilah DOM Property dan DOM Method.

Jadi untuk mengubah nilai properti dari element HTML, kita bisa menggunakan DOM Property dan untuk memanggil fungsi dari suatu element HTML, kita bisa menggunakan DOM Method.

