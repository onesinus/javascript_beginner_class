# Course 6

## Learning Objective
Peserta training dapat membuat tampilan sederhana yang berisi text box untuk melakukan pencarian dan sebuah tombol untuk mencari

## Course :mortar_board:
### Membuat tampilan sederhana dengan HTML & CSS

Untuk membuat tampilan pada aplikasi web kita, kita hanya memerlukan html dan css. maka kita akan membuat sebuah folder dengan nama **search_engine**
Kemudian buat 2 file didalam folder tersebut yaitu file **index.html** dan file **main.css**

Isi file **index.html** dengan kode berikut ini

```html
<!DOCTYPE html>
<html>
<head>
	<title>Search Engine</title>
	<link rel="stylesheet" type="text/css" href="main.css">
</head>
<body>
	<div class="container">
		<div class="title">Search Engine Apps</div>
		<div>
			<input type="text" name="keyword">
		</div>
		<div>
			<button class="btn" id="btnSearch">Search Data</button>			
			<button class="btn" id="btnClear">Clear Input</button>			
		</div>
		<br/>
		<div class="data">
			<a href="#">Lorem ipsum dolor sit amet jokoy</a>
			<a href="#">Lorem is simply dummy text of the printing and types</a>
			<a href="#">Neque porro quisquam est qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit...</a>
		</div>
	</div>
</body>
</html>
```

Isi file **main.css** dengan kode berikut ini

```css
body {
	font-family: arial,sans-serif;
	color: #475c6c;
	overflow: hidden;
}

.container {
	display: flex;
	flex-direction: column;
	align-items: center;
}

.title {
	font-size: 36pt;
	margin: 3vh;
}

input {
	width: 50vw;
	height: 5vh;
	border: 1px solid grey;
	border-radius: 25px;
	outline: none;
	margin: 1vh;
	font-size: 16pt;
	text-align: center;
}

.btn {
	height: 5vh;
	margin: 0.5vw;
	cursor: pointer;
}

.data {
	font-size: 18pt;
	max-width: 	50vw;
	text-align: center;
	overflow-y: auto;
	max-height: 60vh;
}

.data a {
	text-decoration: none;
	display: block;
	padding: 3vh;
}
```

Buka file **index.html** menggunakan browser dan akan tampil hasil dari kode html dan css yang kita sudah buat.

Kita sudah siap dengan tampilan sederhana kita, berikutnya kita akan membuat kode javascript untuk menampilkan data yang dicari.... :round_pushpin:

## Exercise :muscle:
Improve / ubah tampilan sesuai selera dan kreatifitas masing-masing

## Next course preparation :100:
### Persiapkan tentang bagaimana looping di javascript seperti for dan lain-lain.
### Persiapkan tentang kondisi dalam javascript seperti if else, switch case, dan lain-lain.

## Reference
https://css-tricks.com/snippets/css/a-guide-to-flexbox/
