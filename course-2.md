# Course 2

## Learning Objective
### Peserta training memahami tentang tipe data yang ada pada javascript
### Peserta training dapat mendefisinikan variable dengan tipe data yang ada

## Course :mortar_board:
### Tipe data dijavascript?

Untuk tipe data javascript merupakan bahasa pemrograman yang cukup "tidak ketat" dalam artian kita tidak perlu mendefinisikan tipe data setiap kali kita mendeklarasikan variable.
Wait... Apa itu variable? ketika berbicara tentang variable sederhananya bayangkan saja variable sebagai sebuah "ember" :smile:
Tidak mungkin kan teman-teman tidak pernah melihat atau tidak mengetahui fungsi ember? Variable adalah seperti sebuah ember yang dapat menampung air, minyak, ataupun isi yang 
lainnya (jenisnya bisa bermacam-macam). So? Yap, variable adalah sebuah wadah untuk menampung data yang jenisnya berbeda beda. Jenis yang berbeda-beda itu bisa disebut sebagai
Tipe Data.

### Cara mendefinisikan variable pada javascript?
Jika kita lihat kode-kode javascript sebelum ES6 pendefinisian variable menggunakan kata kunci var, maka tidak heran jika kita menggunakan library seperti jQuery dan banyak
menemukan pendefinisian menggunakan var

Tetapi cara yang terbaru dalam mendefinisikan variable adalah dengan menggunakan let dan const yang mana let digunakan untuk data yang dapat diubah nilainya sedangkan const
untuk data yang tidak boleh diubah nilainya seperti phi dalam matematika.

### Tipe data yang ada pada javascript apa aja sih?

Ada 6 tipe data yang disebut sebagai tipe data primitif (hanya menyimpan 1 jenis data) yaitu:
* Undefined / Null ( tipe data spesial )
* Boolean
* Number
* String
* Int
* Symbol

Ada 3 tipe data yang disebut sebagai tipe data composite (tipe data gabungan), yaitu:
* Object
* Array
* Fungsi

Dan uniknya adalah ketiga tipe data tersebut sebenarnya object loh :smile:

### Cara cek tipe data?
Gunakan kode 

```javascript
typeof
```

Yuk langsung aja kita coba mendeklarasikan variable dengan tipe data yang ada pada javascript!

```javascript
let nama = "Onesinus Saut Parulian";
let usia = 23;
const is_male = true;

console.log(nama); // Onesinus Saut Parulian
console.log(usia); // 23

typeof nama; // "string";
typeof(usia); // "number"
typeof(is_male); // "boolean"
```

```javascript
const info = { nama: "Onesinus Saut Parulian", usia: 23 }
typeof(info); // "object"
console.log(info); // {nama: "Onesinus Saut Parulian", usia: 23}
console.log(info.nama); // Onesinus Saut Parulian


const skills = ["PHP", "Javascript", "Database"];
typeof(skills); // "object"
console.log(skills); // ["PHP", "Javascript", "Database"]
console.log(skills[0]); // "PHP"
console.log(skills[1]); // "Javascript"
```

Note: Kita berhitung dimulai dari 1 tetapi javascript ( dan bahasa pemrograman lainnya ) berhitung dimulai dari 0 ya... :smile:

Selamat! anda telah belajar tentang tipe data yang ada pada javascript... :round_pushpin:

## Exercise :muscle:
Buatlah sebuah file bernama tipe_data.js yang berisi kode penerapan tipe-tipe data yang ada pada javascript dengan isi data diri termasuk nama, umur, hoby, dll!

## Next course preparation :100:
### Pelajari tentang apa itu fungsi

## Reference
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures
