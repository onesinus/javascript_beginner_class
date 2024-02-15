## Callback
```javascript
/* Contoh 1: basic callback, cara melempar fungsi melalui parameter dan execute kemudian */
function penjumlahan(angka1, angka2, callBackPenjumlahan) {
    callBackPenjumlahan()
    return angka1 + angka2
}

function callBackPenjumlahan() {
    console.log("Penjumlahan akan segera dilakukan");
}

console.log(penjumlahan(2, 3, callBackPenjumlahan))

/* contoh 2: eksekusi callback function dengan parameter */
// function penjumlahan(angka1, angka2, cb) {
//     angka1 = cb(angka1)
//     return angka1 + angka2
// }

// function callBackPenjumlahan(angka1) {
//     return angka1 + 100
// }

// console.log(penjumlahan(2, 3, callBackPenjumlahan))

/* Contoh 3: fungsi yang mengembalikan (return) sebuah fungsi */
// function penjumlahan(angka1, angka2, callBackPenjumlahan) {
//     return callBackPenjumlahan(angka1, angka2)
// }

// function callBackPenjumlahan(angka1, angka2) {
//     console.log("Penjumlahan akan segera dilakukan");
//     return angka1 + angka2
// }

// console.log(penjumlahan(2, 3, callBackPenjumlahan))
```

```javascript
// buat fungsi yang bisa menjumlahkan (+), mengurangi (-), membagi(/) dan mengkali (*)
function calculate(angka1, angka2, cb) {
    return cb(angka1, angka2)
}

function penjumlahan(angka1, angka2) { return angka1 + angka2 }
const pengurangan = (angka1, angka2) => { return angka1 - angka2 }
const pembagian = (angka1, angka2) => { return angka1 / angka2 }
const perkalian = (angka1, angka2) => { return angka1 * angka2 }

console.log(calculate(2, 3, penjumlahan))
console.log(calculate(5, 3, pengurangan))
console.log(calculate(6, 2, pembagian))
console.log(calculate(4, 4, perkalian))
```

```javascript
/*
    Buatlah sebuah fungsi yang menerima 3 parameter
    parameter pertama dan kedua adalah jumlah uang
    parameter ketiga adalah Currency ("Rp", "$", "SGD")
    buatlah fungsi callback yang dapat menjumlahkan kedua angka tersebut 
    dan kembalikanlah dalam format sebagai berikut "{Currency} {hasil operasi}"

    Kirim callback function tersebut sebagai parameter terakhir pada fungsi yang anda sudah buat
*/

function currency(uang1, uang2, currency, cb) {
    return cb(uang1, uang2, currency);
}

const addTwoNumbers = (uang1, uang2, currency) => {
    return `${currency} ${uang1 + uang2}`;
};

console.log(currency(2000, 3000, "Rp. ", addTwoNumbers));
console.log(currency(5000, 3000, "$. ", addTwoNumbers));
console.log(currency(3000, 3000, "SGD. ", addTwoNumbers));
```