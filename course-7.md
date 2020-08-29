# Course 7

## Learning Objective
Peserta training dapat menampilkan data yang "mirip" dengan kata kunci yang diisi pada kotak pencarian
Peserta dapat membuat event onclick pada tombol cari
Peserta dapat membuat event onpress pada tombol cari

## Course :mortar_board:
### Membuat kode javascript untuk menampilkan data sesuai dengan pencarian

Untuk menampilkan data pada aplikasi web kita, kita memerlukan javascript. maka kita akan membuat sebuah file dengan nama **main.js**
Kemudian jangan lupa untuk memanggil file main.js difile **index.html** dengan menambahkan script ini sebelum penutup tag </body> pada index.html

```html
<script src="main.js"></script>
```

Isi file **main.js** dengan kode berikut ini

```javascript
// Kita buat data dummy untuk pencarian data
// Nantinya data ini akan diambil dari database
const data = [
	'How to become JS expert',
	'JS is Javascript',
	'Coding is Fun',
	'Programmer do coding everyday',
	'Everyday is fun'
];

// Kita akan mendefinisikan selector-selector yang kita perlukan
const btnSearch 	= document.getElementById('btnSearch');
const btnClear 		= document.getElementById('btnClear');
const search 		= document.getElementsByName('keyword')[0];
const data_section 	= document.getElementsByClassName('data')[0];

// Membuat event untuk handle tombol search ketika diklik
btnSearch.addEventListener('click', event => {
	searchData();
});

// Membuat event untuk handle tombol clear input diklik
btnClear.addEventListener('click', event => {
	search.value = "";
});

// Membuat event ketika menekan enter pada inputan search
search.addEventListener('keyup', event => {
	if (event.keyCode === 13) {
		searchData();
	}
});

// fungsi untuk melakukan pencarian data
function searchData() {
	const search_value 	= search.value.toLowerCase();

	// Copy array data ke variable data_filtered
	const data_filtered = data.slice(0);

	// Lakukan perulangan pada semua data untuk cek apakah ada yang mengandung "keyword" atau tidak
	data_section.innerHTML = "";
	for (var i = 0; i < data_filtered.length; i++) {
		if ( data_filtered[i].toLowerCase().includes(search_value) ) {			
			// Jika ada, Masukkan data ke list data pencarian yang didapat
			data_section.innerHTML += "<a href='#'>"+data_filtered[i]+"</a>";
		}
	}	
}
```

Sekarang mari coba ketik kata kunci dan lakukan pencarian data.... :round_pushpin:

## Exercise :muscle:
Hapus code javascript yang ada, lalu buat lagi dengan versi kalian masing-masing, jika lupa bisa check lagi dan ikuti lagi, sampai bisa!
Kalian juga boleh improve kode javascript nya jika kalian merasa ada cara yang lebih baik ya :smile:

## Now Time for Final Project :100:
### Untuk kelas beginner sampai disini pembelajarannya, tugas kalian adalah mengembangkannya dan mencoba kode javascript seperti kondisi (if else, switch case, dll)
### Cobalah jika looping (for, while, do while, foreach)
### Cari tau sintax-sintax ES6
### And be ready for final project! :smile:

## Reference
