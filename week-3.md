# **Rangkuman Minggu Ke-3 JavaScript Dasar : Js Array and Multidimensional, Object, Recursive, Asyncronus, Git & Github Lanjutan, BootStrap 5**

## A. JavaScript Array and Multidimensional
Struktur data merupakan cara-cara atau metode yang digunakan untuk menyimpan data di dalam memori komputer.
Salah satu struktur data yang sering digunakan dalam pemrograman adalah Array.
Array merupakan struktur data yang digunakan untuk menyimpan sekumpulan data dalam satu tempat.
Setiap data dalam Array memiliki indeks, sehingga kita akan mudah memprosesnya.
Indeks array selelau dimulai dari ('0').

``` Let namaArray = []; ```

contoh :

``` Let buah = [anggur, jeruk, apel]; ```

lalu, bagaimana cara mengambil data di array :

``` namaArray[index] ```

contoh : jika ingin mengambil jeruk dari array buah, dengan cara :

``` buah[1]; ```

lalu, bagaimana jika array memiliki index sampai 1000 dan kita ingin mengambil datanya? masalah ini dapat diselesaikan menggunakan perulangan.
contoh :

``` for(let i = 0; i <buah.length; i++>) {
    document.write(`<li>${buah[i]} <li>`);
}
```

**Cara Menambahkan Data ke Array**
Kita dapat memabhakan isi array menggunakan method **push()**.
 contohnya: kita ini menambahkan isi Array buah ke index 3 dengan value semangka. Maka :

 ``` buah[3] = "semangka"; ```

 **Cara Menghapus Data Array**
 Ada dua cara untuk menghapus data dalam array. Pertama, kita dapat menggunakan **delete**, dan yang kedua kita dapat menggunakan method seperti **pop(), shift(), dan splice()**.

 contoh penggunaan delete

 ``` delete buah[2]; //menghapus indeks ke-2 ```

 contoh penggunaan pop() (pop digunakan untuk menghapus index terakhir dalam array)

``` buah.pop()l //menghapus data yang terakhir dari array ```

 contoh penggunaan shift() (shift digunakan untuk menghapus index pertama dalam array)

 ``` buah.shift() //menghapus data pertama dalam array buah ```

 dan yang terakhir menggunakan splice(), (splice digunakan untuk menghapus pada index tertentu)

 syntak :

 ```array.splice(<index>, <total>); ```

 contohnya :

````buah.splice(2,1) //menghapus index 2```

## B. JavaScript Object
Objek sebenarnya adalah sebuah variabel yang menyimpan nilai (properti) dan fungsi (method).
cara membuat object, yaitu 

``` let namaObject = {property: 'value'}; ```

**Cara mengakses properti dan Method Dalam Object**

Adapun cara untuk mengakses properti dan method, seperti dibawah ini :

``` console.log(namaObject.properti) ```


## C. JavaScript Recursive
## D. JavaScript Asyncronus
 Asynchronous hasil eksekusi atau output tidak selalu berdasarkan urutan kode, tetapi berdasarkan waktu proses. Eksekusi dengan asynchronous tidak akan membloking atau menunggu suatu perintah sampai selesai. Daripada menunggu, asynchronous akan mengeksekusi perintah selanjutnya.
Promise adalah object yang mempersentasikan keberhasilan / kegagalan sebuah event yang async di masa yang akan datang. 


 Pada promise, untuk mengeksekusinya dapat menggunakan 2 cara, yaitu :
 - Async await
 - Fetch()

 Penggunaan Async Await, yaitu :

 ```
async function name(param0) {
  statements
}
async function name(param0, param1) {
  statements
}
async function name(param0, param1, /* … ,*/ paramN) {
  statements
}

 ```

 Sedangkan penggunaan fetch, yaitu :

 ```
fetch('http://example.com/movies.json')
  .then((response) => response.json())
  .then((data) => console.log(data));

 ```
## E. Git & Github Lanjutan

Dalam mempermudah project tim, Github memberikan fiture Git Organization. Git Organization memberikan kita repository yang dapat digunakan bersama untuk project tim. 
Adapun langkah-langkah untuk menggunakan git organization, yaitu :

1. Ketua project membuat git organizationa, dan mengundang anggota tim masuk ke dalam git organization
2. Dalam git organization terdapat 2 branch utama, yaitu main dan development.
3. Setiap anggota hanya boleh menge-push project yang dikerjakan kedalam brach development. Branch main hanya beloh digunakan jiga project sudah benar-benar siap dan tidak ada lagi yang do ubah untuk di push ke publick.
4. Cara push ke git project diawali dengan tiap anggota melakaukan "clone" file repositori kedalam perangkat masing-masing dengan syntak :
``` clone namaRepository ```

5. Mmebuat branch baru sesuai project yang dikerjakan, dengan syntak 
``` git branch namaBranch ```
6. Masuk kedalam branch nya menggunakan syntak :
``` git switch namaBranch ```
7. lakukan 
``` git add .```
8. Masukkan nama perubahan
``` git commit -m "judul perubahan" ```
9. Terakhir, push project dengan syntak
``` git push -u origin namaBranch ```

## F. Bootstrap Responsive
Ada 6 cara untuk membuat website kita responsive, yaitu :
- Meta Viewport
- max-width
- relative unit
- media query
- flex
- grid

1. Meta Viewport
Viewport disediakan oleh HTML 5, dengan cara menyisipkan 

``` 
<meta name="viewport" content="width=device-width initial-scale=1.0">
 ```
 
2. Media Query

Media Query digunakan untuk mengatur css dengan ketentuan panjang width.
Contoh penggunaan nya :

```
@media only screen and (max-width: 600px) {
  body {
    background-color: lightblue;
  }
}
```
Maksud dari kode diatas, yaitu : dengan ketentuan lebar minimal 600px pada perangkat yang digunakan, maka background-color akan berubah menjadi lightblue
