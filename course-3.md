# Course 3

## Learning Objective
### Peserta training memahami tentang fungsi di javascript
### Peserta mengetahui beragam cara membuat kode fungsi dan bisa membuatnya

## Course :mortar_board:
### Fungsi di javascript?

Fungsi berisi sebagian kode yang dibuat untuk tujuan tertentu. fungsi dapat dijalankan dengan cara dipanggil dengan nama fungsi nya atau bisa juga membuat fungsi tersebut
jalan secara otomatis. fungsi juga dapat diletakkan kesebuah variable yang nantinya variable tersebut akan mengarah ke fungsi tersebut.

Dan ingat... dalam javascript fungsi adalah sebenarnya object juga... 

### Apa saja yang harus diketahui dari fungsi?
Dalam mempelajari fungsi ada setidaknya 2 hal yang harus kita ketahui yaitu arguments atau bisa juga disebut parameters  adalah nilai yang kita harus isi ketika memanggil fungsi
kemudian yang kedua adalah return value atau nilai yang akan dikembalikan ketika fungsi tersebut dipanggil / dijalankan.

### Fungsi sebagai expression vs fungsi sebagai declaration?

Sebelum kita lebih jauh mengetahui tentang fungsi, kita harus mengetahui kedua hal ini dahulu yaitu ada disebut expression function dan declaration function.
Sederhana nya declaration function adalah mendeklarasi fungsi yang **nantinya akan digunakan atau dipanggil**. Istilah pemanggilan fungsi biasa disebut invoked.

contoh:
```javascript
function hello() {
  console.log("Hello World");
}
```

Sedangkan expression function adalah fungsi diletakkan ke sebuah variable, dan tidak memerlukan nama fungsi, yang akan menjadi nama dari fungsi tersebut adalah
nama variable yang digunakan dalam meletakkan fungsi.
contoh:
```javascript
var hello = function() {
  console.log("Hello World");
}
```

Untuk memanggil fungsi / invoked:
```javascript
hello();
```

Perbedaan mendasar dari expression function dengan declaration function adalah declaration function dijalankan sebelum kode lain dijalankan.
Sedangkan expression function akan dijalankan sesuai urutan pembacaan kode.

Jadi ini akan berjalan pada declaration function

```javascript
hello();
function hello() {
  console.log("Hello World");
}
```

Tetapi tidak akan berjalan pada expression function
```javascript
hello();
var hello = function() {
  console.log("Hello World");
}
```

Jadi jika fungsi ingin dapat bisa digunakan meskipun kode fungsi berada di tengah ataupun paling bawah maka gunakanlah declaration function, tetapi jika ingin pembacaan
sesuai urutan gunakanlah expression function, dan juga jika ingin menggunakan fungsi sebagai argument/parameter pada fungsi lain gunakan expression function.

### Beberapa tipe fungsi di javascript

Ada beberapa cara dalam mendeklarasikan fungsi pada javascript, yaitu:
* Anonymous Function: 
* Named Function
* Inner Function
* Recursive Function
* Immediately Invoked Function Expressions (IIFE)

### Anonymous Function

Anonymous function tidak memiliki nama, dan hanya expression function yang dapat menjadi anonymous, declaration function harus memiliki nama fungsi.

```javascript
(function () {});
```
Atau jika kita menggunakan ES6 / ECMAScript 2015 notasi arrow
```javascript
() => {};
```

### Named Function

Named function kebalikan dari anonymous function yaitu named function merupakan fungsi yang diberi nama.

Contoh named function sebagai declaration function

```javascript
function hello() {}
```

contoh named function sebagai expression function
```javascript
(function hello() {})
```

contoh named function pada ES6 / ECMAScript 2015

```javascript
const hello = () => {};
```

### Inner Function

Inner fungsi merupakan sebutan untuk fungsi yang ada pada fungsi lain ( Yo Dawg... gue denger lu belajar fungsi? jadi gua fungsi didalem fungsi supaya lu bisa liat fungsi dalem fungsi ) :smile:

Contoh inner function
```javascript
function showNames() {
  function name(p_name) {
    return p_name;
  }
  return name("Onesinus") + name("Saut");
}

showNames(); //"OnesinusSaut"
```

### Recursive Function

Fungsi rekursif adalah fungsi yang memanggil dirinya sendiri.

```javascript
function berulang(urutan) {
  console.log('Fungsi dipanggil dengan urutan ' , urutan);
  
  if (urutan >= 10) return;
  if (!urutan) return; // ini untuk jagaan agar tidak infinite call / fungsi dipanggil terus menerus
  
  berulang(urutan+1);
}
```

Yap tepat sekali fungsi itu akan terus berjalan dari angka yang diberikan diparameter (dikenal sebagai variable urutan didalam fungsi), sampai urutan mencapai 10.

### Immediately Invoked Function Expressions (IIFE)

Nah kalau IIFE ini ketika kode fungsi berhasil diload browser langsung otomatis dijalankan / di invoked fungsi nya
Note: Function declaration tidak dapat menggunakan IIFE ini, selain declaration bisa

caranya hanya tinggal menambahkan () pada akhir fungsi, contoh
```javascript
(function hello() {
  console.log("hello");
}());

(function hello() {
  console.log("hello");
})();

(() => console.log('hello'))();
```

Selamat! anda telah belajar tentang fungsi pada javascript... :round_pushpin:

## Exercise :muscle:
Buatlah sebuah file bernama fungsi.js yang berisi kode penerapan beberapa jenis fungsi yang ada pada javascript dengan membuat fungsi untuk menampilkan data diri 
sepeti showNama(), showUmur(), showHobby(), dll!

## Next course preparation :100:
### Pelajari tentang apa itu DOM

## Reference
https://developer.mozilla.org/en-US/docs/Glossary/Function
