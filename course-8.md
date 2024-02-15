## Boolean

```javascript
const name = "Onesinus"
const salary = 9999999999999
const is_married = false // boolean

const name = "Ayu"
const salary = 10000
const is_married = true // boolean
```

```javascript
/* Syntax 
if (<kondisi>) {
    // lakukan sesuatu jika kondisi terpenuhi (bernilai true)
}
*/
if (1 > 2) { // 1 > 2 mengembalikan false
    console.log("Ini tidak akan dieksekusi")
}

if (true) {
    console.log("ini pasti di eksekusi karena kondisinya bernilai true")
}

if (false) {
    console.log("ini tidak akan di eksekusi karena kondisinya bernilai false")
}

if (1 < 2) {
    console.log("Okeee")
}
```

```javascript
// operator (>, <, ==) -> mengembalikan nilai true / false (boolean)
console.log(10 > 7) // true
console.log(7 > 10) // false
console.log(7 == 7) // true
console.log(7 == 10) // false

console.log(5 == "5") // true
console.log(5 === "5") // false (karena dibandingkan sampai ke tipe datanya)
console.log(5 === 5) // true
console.log("5" === 5) // true
```