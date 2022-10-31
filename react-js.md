# **REACT JS**

## Apa itu React JS ?
React JS adalah library JavaScript yang biasa digunakan saat membangun UI suatu website atau aplikasi web. 

Jadi, React JS bisa dianggap seperti perpustakaan yang berisi berbagai kode JavaScript yang sudah tertulis (pre-written).
Ada 2 fiture unggulan React JS, yitu JSX dan virtual DOM.

**JSX ADALAH** xtension syntax JavaScript yang memungkinkan Anda untuk memodifikasi Document Object Model (DOM) dengan kode bergaya HTML. 
Sedangkan,**Virtual DOM** adalah  salinan dari DOM asli yang ingin diupdate yang berguna untuk melihat bagian dari DOM asli yang berubah. 

## Cara install React js
1. Install Node.js (dapat diunduh di https://nodejs.org)
2. Ada 3 library untuk create-react-app, yaitu npx, npm yarn. (syntak dapat dilihat di docs https://create-react-app.dev).
3. Setelah diinstal untuk menjalankan program menggunakan

```
npm start
```
## Aturan dalam jsx
1. Setiap JSX hanya bisa memiliki 1 parent element.
2. Pada jsx, terdapat beberapa perubahan pada attribut seperti attribut class berubah menjadi **className**
3. Javascript dapat disisipkan menggunakan curly braces.
4. Untuk mengakses variabel pada JSX, gunakan curly brances.
5. Deklarasi event dengan curly braces pada JSX, contoh :
```
onClick={onClickFunction}
```

## Komponen dan Props
**Komponen adalah** salah satu core dari React JS. Komponen akan membagi UI dalam satuan-satuan kecil.
Artinya dalam 1 page ada beberapa komponen yang bisa kita buat. Sehingga dengan begitu, kita dapat menggunakan komponen berulang-ulang dan menghemat code.

Catatan : Bagaimana kita memnentukan sebuah komponen?
Perhatikan, jika code yang akan kita tulis akan digunakan di page lain, maka itu sudah digolongkan oleh komponen.

**Ada 2 cara membuat componen, yaitu :**
1. Menggunakan Function
2. Menggunakan class

Langkah-langkah membuat componen menggunakan function:

**step 1**. Buat sebuah project

**step 2**. Buka project yang telah dibuat pada code editor.

**step 3.** Jalankan React js

**step 4.** Pada folder src, buat folder baru bernama componentes.

**step 5.** Dalam folder componenets, buat file componen yang akan kita buat(WAJIB DIAWALI DENGAN HURUP KAPITAL). Contoh kita ini membuat componen card
```
Card.jsx
```

**step 6.** Dalam file card.jsx Jangan lupa untuk menyisipkan eksport default, agar dapat diakses di App.js

```
export default Card;
```

**step 7.** Komponen sudah siap dibuat dan siap untuk digunakan. Cara menampilkannya yaitu dengan import difile  App.js. 

```
import Card from "./components/Card.jsx"
```

cara menyisipkannya :
```
<card />
```
## Conditional dalam React
React memperkenalkan sebuah conditional bernama Conditional Rendering (docs: https://reactjs.org/docs/conditional-rendering.html)
Penggunaan Conditional rendering hampir sama dengan conditional if dalam vanilla javascript.
Contoh :
1. Kita buat 2 fungsi dengan parameter, seperi dibawah ini
```
function UserGreeting(props) {
  return <h1>Welcome back!</h1>;
}

function GuestGreeting(props) {
  return <h1>Please sign up.</h1>;
}
```

2. Setelah itu kita akan buat fungsi dengan nama greeting yang akan menampilkan komponen UserGreeting atau GuestGreeting (sesuai dengan nilai parameter yang dimasukkan).

```
function Greeting(props) {
  const isLoggedIn = props.isLoggedIn;
  if (isLoggedIn) {    return <UserGreeting />;  }  return <GuestGreeting />;}
const root = ReactDOM.createRoot(document.getElementById('root')); 
// Try changing to isLoggedIn={true}:
root.render(<Greeting isLoggedIn={false} />);
```

## Hook dan LifeCycle
Pembuatan komponen terbagi dua, yaitu menggunakan function dan class. Kebnayakan orang, lebih sering menggunakan function, karna lebih mudah dan praktis. Untuk membuat komponen dengan function, react memperkenalkan alat bantu yang dinamakan **hook**. 
Hooks yang sering digunakan, yaitu:
1. useState 
2. useEffect

**Penggunaan useState**
cara menggunakan useState :
1. import useState dengan cara:
```
import { useState } from "react";
```
2. deklarasi useState dengan cara 
```
const [nama, setNama] = useState("luthfi");
```

3. Pemanggilan data
```
<p> Hallo nama saya { nama } </p>
```

4. cara merubah data
```
<button onClick={ setNama(":david)}> Ubah </button>
```

**Catatan**: untuk menampilan data gunakan nama, jika ingin merubah data gunakan setData.
