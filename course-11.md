## Sorting

```javascript
// Sort secara default mengurutkan ascending (dari kecil ke besar)
const umur = [10, 5, 17, 22, 3]
umur.sort(function (a, b) { // urutkan dari angka terkecil ke terbesar (ascending)
    return a - b
})

console.log(umur)
// urutkan dari angka terbesar ke terkecil (descending)
umur.sort(function (a, b) { return b - a })
umur.sort(function (a, b) {
    return b - a
})

const indomie = ["Ayam bawang", "Kari Ayam", "Soto"]
indomie.sort()
console.log(indomie)

const angka = [7, 3, 1, 4, 73, 21]
angka.sort((a, b) => a - b)
console.log(angka)
```