## Regex
```javascript
/* CARA MENDAPATKAN ANGKA */
// const keterangan_parkir = "1 Jam 20 Menit 30 Detik"
// const pattern = /\d+/g
// console.log(pattern.exec(keterangan_parkir)) // 1
// console.log(pattern.exec(keterangan_parkir)) // 20
// console.log(pattern.exec(keterangan_parkir)) // 30

/* Cara mendapatkan yang BUKAN ANGKA */
const keterangan_parkir = "1 Jam 20 Menit 30 Detik"
const pattern = /\D+/g
console.log(pattern.exec(keterangan_parkir)[0]) // Jam
console.log(pattern.exec(keterangan_parkir)[0]) // Menit
console.log(pattern.exec(keterangan_parkir)[0]) // Detik
console.log(pattern.exec(keterangan_parkir)) // Null
```

```javascript
const pattern = /[abc]../

console.log(pattern.test("a")); // true
console.log(pattern.test("b")); // true
console.log(pattern.test("z")); // false
console.log(pattern.test("aa")); // true
console.log(pattern.test("ab")); // true
console.log(pattern.test("abc")); // true
console.log(pattern.test("bca")); // true
console.log(pattern.test("ax")); // false
console.log(pattern.test("bz")); // false
```

```javascript
// const kalimat = "Nama Saya Adalah Bambang"
// const regex_literal = /Nama/
// console.log(regex_literal.test(kalimat))


// const kalimat = "Nama Saya Adalah Bambang"
// const regex_literal = /Adalah /
// console.log(regex_literal.test(kalimat))

// const email = "joko@gmail.com"
// const pattern_gmail_valid = /@gmail.com/
// console.log(pattern_gmail_valid.test(email))

// contoh validasi nama harus tidak ada angka menggunakan regex
const name = "Sinus Saut Parulian"
const pattern_character_only = /\d+/
const is_name_invalid = pattern_character_only.test(name)
if (is_name_invalid) {
    console.log("Nama tidak valid")
} else {
    console.log("Nama valid");
}
```