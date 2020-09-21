# Course 4

## Learning Objective
Peserta training dapat memahami apa itu DOM dan dapat memanipulasi html dengan javascript.

## Course :mortar_board:
### Apa itu DOM?

Sederhananya DOM itu singkatan dari Document Object Model :smile: yaitu sebagai "perantara" (API) untuk kita dapat berinteraksi dengan dokument HTML atau XML.
DOM adalah model dokumen yang ditampilkan pada browser dan direpresentasikan sebagai node tree ( seperti pohon ) dimana setiap node adalah bagian dari dokumen
Seperti Element, text string, dan komentar.

DOM merupakan salah satu API yang paling banyak digunakan di web karena DOM membuat kode yang kita buat yang berjalan pada browser dapat berinteraksi dengan semua
dokumen node yang ada pada dokumen.

### Bagaimana cara memanipulasi HTML menggunakan javascript?

Oke, pertama kita dapat melihat struktur HTML yang akan kita ubah menggunakan inspect element yang ada pada browser caranya bisa dengan klik kanan pada browser -> Inspect
Di windows kita juga bisa menggunakan kombinasi **ctrl + shift + i** atau **f12** pada keyboard

Sekarang mari kita coba buat sebuah folder bernama **belajar_dom** dan buat didalamnya sebuah file **index.html** dan juga **main.js**

isi **index.html** dengan kode berikut

```html
<div id="hello">Hello</div>
<div class="bunga">Mawar</div>
<div class="bunga">Melati</div>
<span>Semuanya</span>
<span>Indah</span>
<script src="main.js"></script>
```

isi **main.js** dengan kode berikut

```javascript
window.addEventListener('load', (event) => {
    const hello = document.getElementById("hello");
    const current_value = hello.innerText;
    hello.innerHTML = current_value + " World!";

    const spans = document.getElementsByTagName("span");
    console.log(spans[0].innerHTML)
    console.log(spans[1].innerHTML)

    var bunga = document.getElementsByClassName('bunga');
    for (let i = 0; i < bunga.length; i++) {
        bunga[i].style.backgroundColor = "red";
    }
});
```

### Selector

Kita dapat memanipulasi dengan beberapa cara, bisa menggunakan beberapa selector seperti id, class maupun nama dari tag/element html itu sendiri.
Untuk javascript kita dapat gunakan **document.getelementById**, **getElementsByClassName**, **getElementsByTagName**, **querySelector**, dan lain-lain.

## Event

DOM sendiri memiliki beberapa event, event ini adalah kapan waktu kita ingin memanipulasi DOM. misalnya ketika kita ingin memunculkan alert ketika halaman sudah berhasil diload
atau menampilkan popup error ketika gagal load, atau misalnya ketika kita ingin memanipulasi DOM ketika suatu tombol diklik, ketika element difokuskan atau diblurkan, dan lain-lain

Dan event ini juga bisa mendeteksi loh apakah browser dapat akses ke internet (online) atau tidak (offline).

Contoh

```javascript
window.addEventListener('load', (event) => {
  console.log('page is fully loaded');
});
```

```javascript
window.addEventListener('load', (event) => {
  console.log('page is fully loaded');
});
```

```javascript
const button = document.querySelector('button');

button.addEventListener('click', event => {
  button.innerHTML = `Click count: ${event.detail}`;
});
```

```javascript
// onoffline version
window.onoffline = (event) => {
  console.log("The network connection has been lost.");
};
```

Selamat anda sudah belajar tentang DOM.... :round_pushpin:

## Exercise :muscle:
Buatlah sebuah kotak dan 3 buah tombol (merah, kuning, hijau) dan buatlah ketika tombol tersebut diklik warna pada kotak menyesuaikan dengan tombol yang diklik!

## Next course preparation :100:
### Pelajari dan cari tau tentang library & Framework yang ada pada javascript

## Reference
https://developer.mozilla.org/en-US/docs/Glossary/DOM
https://developer.mozilla.org/en-US/docs/Web/Events
