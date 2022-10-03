# **Rangkuman Week2 JavaScript Dasar**

## A. JavaScript Scope
Scope secara sederhana dapat diartikan sebagai area/wilayah/tempat untuk mencari dan melakukan sesuatu.
Dianalogikan penggunaan scope seperti ember yang didalamnya berisi kelereng. Kita bisa memasukkan kelereng ditiap ember yang berbeda, setiap kita membutuhkan kelereng tersebut, kita harus tau dimana ember yang berisi kelereng tersebut.

Scope dalam JavaScript terbagi dua, yaitu
- Global Scope
- Lokal Scope

**Global Scope** => Setiap variabel yang dideklarasikan diluar blok disebut variabel global. Variabel tersebut dapat diekesekusi secara global

**Local Scope** => Setiap variabel yang dideklarasikan didalam blok atau didalam sebuah  curly brackets {} disebut variabel local. Variabel lokal hanya bisa dieksekusi didalam blok tersebut. 

contoh yang membedakan variabel dengan global scope atau locak scope :
 ```// Initialize a global variable
var digimon = "Agumon";

function evolution() {
  // Initialize a local, function-scoped variable
  var digimon = "Greymon";
  console.log(digimon);
}

// Show the result
console.log(digimon);
evolution();
console.log(digimon);; 
```

dapat dilihat dari code diatas, hasil output dari variabel digimon berbeda, karena penggunaan scope.

**catatan penting:** Var tidak tidak akan menanggap sebuah variabel didalam if, for, while loops sebuah blok. Jika kita mendeklarasikan sebuah variabel menggunakan var didalam if, for, while loops, maka varibel akan terbaca oleh komputer sebagai global scope. contoh :

```var trigger = true;

// Initialize a global variable
var digimon = "Agumon";

if (trigger) {
  // Attempt to create a new variable in a block
  var digimon = "Greymon";
  console.log(`Evolution triggered, you are become ${digimon}.`);
}

console.log(`Evolution failed, you are still ${digimon}.`);;
```


## B. JavaScript Function

JavaScript Function adalah sebuah blok kode yang dibuat untuk melakukan sebuah pekerjaan tertentu.
Bayangkan jika kita memiliki tugas untuk menampilkan output seperti berikut
[gambar]

berapa banyak kita harus mengetik jika diminta menampilkan 1000 
```
console.log("hallo, dina")
console.log("hallo, raudha")
console.log("hallo, zizah")
```
Untuk mempermudahnya kita menggunakan sebuah function.
```
function hello(nama) {
    console.log(`hallo ${nama}`)
}
```
kita dapat menjalankan function sebanyak yang kita mau
```
hallo(dina);
hallo(raudha);
hallo(zizah);
```
bukankan dengan function code kita menjadi singkat dan mudah digunakan ?

Dalam memanggil function / mengeksekusi sebuah fuction terdapat 2 cara, yaitu menggunakan console.log dan return.
Apa **perbedaan** antara **console.log** dengan **return** ?
Jika kita menggunakan **console.log**, value yang akan dipanggil akan ditampilkan saja tetapi tidak bisa diproses kembali, tetapi jika kita menggunakan **return** valeu yang akan dieksekusi dapat digunakan kembali dan diproses untuk tugas-tugas selanjutnya.

## C. Data Type in Prototype

## D. DOM
DOM merupakan singkatan dari **Document Object Model.**
