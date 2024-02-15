## Build in functions
```javascript
// 1. Terdapat sebuah array dengan data nama2 siswa yaitu "Udin" "Bambang", "Tejo"
// 2. masukan data baru ke array tersebut dengan data "Jacky" pada urutan terakhir
// 3. Hapus data pertama pada array itu (Udin)
// 4. hapus data terakhir pada array itu (Jacky)
// expected output = Bambang, Tejo
// 5. Masukan data pada urutan pertama pada array tersebut dengan data "Kucrut"
// expected output = Kucrut, Bambang, Tejo
const siswa = ["Udin", "Bambang", "Tejo"]
siswa.push("Jacky")
siswa.shift()
siswa.pop()
siswa.unshift("kucrut")
console.log(siswa)

// terdapat data sebagai berikut[7, 3, 1, 4, 73, 21]
// Urutkanlah data tersebut sehingga menjadi seperti ini[1, 3, 4, 7, 21, 73]
const arr = [7, 3, 1, 4, 73, 21]
arr.sort(function (a, b) {
    return a - b
})
console.log(arr)

// coba
const temp = [12, 5, "Ayam", 2, "Kutek", 9, "Kura", 4, "Jagung"];
temp.sort((a, b) => a - b);
console.log(temp);
```

## Splice and Split
```javascript
/*
    terdapat data seperti ini ["Somay", "oddo", "ipong"]
    ubahlah agar menjadi seperti ini ["Somay", "oddo", "Pipo", "ipong"]
*/
const handphones = ["Somay", "oddo", "ipong"]
handphones.splice(2, 0, "Pipo")
console.log(handphones)


/*
    terdapat data seperti ini ["Somay", "oddo", "Pipo", "ipong"]
    ubahlah agar menjadi seperti ini ["Somay", "Semsang", "Ashus", "Pipo", "ipong"]
*/
const hp = ["somay", "oddo", "pipo", "ipong"]
hp.splice(1, 1, "semsang", "ashus")
console.log(hp)

/*
    terdapat data seperti ini "Aku Suka Dia"
    ubahlah agar menjadi seperti ini ["Aku", "Suka", "Dia"]
*/
console.log("Aku Suka Dia".split(" "))

/*
    terdapat data seperti ini "Ini,isi,dari,file,csv"
    ubahlah agar menjadi seperti ini ["Ini", "isi", "dari", "file", "csv"]
*/
console.log("Ini,isi,dari,file,csv".split(","))

/*
    terdapat data seperti ini "Bembeng:1000, Coki-coki: 2000"
    ubahlah agar menjadi seperti ini ["Bembeng: 1000", "Coki-coki: 2000"]
*/
console.log("Bembeng:1000, Coki-coki: 2000".split(", "))
```

```javascript
const alat_musik = ["Gitar", "Ukulele", "Kalimba"]
// syntax .splice(1. INDEX BERAPA, 2. APUS BERAPA DATA, 3. DATA YANG DITAMBAHIN)

// ["Gitar", "Ukulele", "Kalimba"] => ["Ukulele", "Kalimba"]
// alat_musik.splice(0, 1)
// console.log(alat_musik)


// ["Gitar", "Ukulele", "Kalimba"] => [ 'Gitar', 'Ukulele', 'PIANO', 'DRUM', 'Kalimba' ]
// alat_musik.splice(2, 0, 'PIANO', 'DRUM')
// console.log(alat_musik)

// ["Gitar", "Ukulele", "Kalimba"] => ["Gitar"]
// alat_musik.splice(1, 2)
// console.log(alat_musik)

// ["Gitar", "Ukulele", "Kalimba"] => ["BASS", "BASS BETOT" "Kalimba"]
// alat_musik.splice(0, 2, "BASS", "BASS BETOT")
// console.log(alat_musik)
```

```javascript
const nama = "Onesinus Saut Parulian Tamba"
console.log(nama)
console.log(typeof nama)

const arr_nama = nama.split(" ")
console.log(arr_nama)
console.log(typeof arr_nama)

const usia = "17,12,13,15".split(",")
console.log(usia)

const mobil = "BMW, Avanza, Calya".split(", ")
console.log(mobil)
```

## Push, pop, shift and unshift
```javascript
/* constant tidak dapat diubah jika tipe datanya primitif
 (yang datanya hanya menyimpan 1 value / nilai)
*/
/* ini error
    const nama = "Bambang"
    nama = "udin"
*/
/* ini kagak
    let nama = "Bambang"
    nama = "udin"
*/

const siswa = []
siswa.push("Bambang", "Udin", "Jacky") // 1, return new length of array
siswa.push("udin") // 2
siswa.push(["wkwkwk", "wew"])
siswa.push({ ah: "Mantap" })
console.log(siswa)

siswa.pop()
siswa.pop() // untuk menghapus element terakhir dalam sebuah array
console.log(siswa)

siswa.unshift("Maliki") // untuk menambahkan element ke paling pertama (index 0)
console.log(siswa)

siswa.shift() // untuk menghapus element di paling depan (index 0)
siswa.shift()
console.log(siswa)
```