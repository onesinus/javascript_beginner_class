## Basic Promise
```javascript
/* Promise States */
// 1. Pending (ketika belum diresolve / direject)
// 2. Resolved (ketika janji ditepati / berhasil)
// 3. Rejected (ketika janji tidak ditepati / error)

/* Basic Sintax */
// const janjian = new Promise((resolve, reject) => {
//     // resolve()
//     // reject()
// })

// console.log(janjian) // pending

/* Contoh resolve promise */
// const janjian = new Promise((resolve, reject) => {
//     resolve("Udah dateng nih ke tempat janjian")
// })

// console.log(janjian) // "Udah dateng nih ke tempat janjian"

/* Contoh reject promise */
const janjian = new Promise((resolve, reject) => {
    reject("Gabisa gue bro, lagi mules")
})

console.log(janjian) // Error, kita perlu handle error ini (atau aplikasi akan crash)
/* Cara handle error promise */
janjian
    .then(data => console.log(data))
    .catch(err => console.log(err))
```

```javascript
/*
    1. deklarasikan sebuah promise (nama bebas)
    2. Resolve promise tersebut
    3. Reject promise tersebut
*/

//soal1
const janjian = new Promise((resolve, reject) => {
    //resolve()
    //reject()
})

//soal 2
const janji_terpenuhi = new Promise((resolve, reject) => {
    resolve("udah aku penuhin janjiku yha!")
})
console.log(janji_terpenuhi)

//soal 3
const tidak_terpenuhi = new Promise((resolve, reject) => {
    reject("maaf, yha!")
})

tidak_terpenuhi
    .then(data => console.log(data))
    .catch(err => console.log(err))

console.log(tidak_terpenuhi)
```

## Async Paralel
```javascript
const firstPromise = () => {
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            resolve("First Promise")
        }, 1000);
    })
}

const secondPromise = () => {
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            resolve("Second Promise")
        }, 2000);
    })
}

const thirdPromise = () => {
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            resolve("Third Promise")
        }, 1000);
    })
}

async function asyncParalel() {
    firstPromise().then(response => console.log(response))
    secondPromise().then(response => console.log(response))
    thirdPromise().then(response => console.log(response))
}

asyncParalel()
```

## Async Serial
```javascript
const firstPromise = () => {
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            resolve("First Promise")
        }, 1000);
    })
}

const secondPromise = () => {
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            resolve("Second Promise")
        }, 5000);
    })
}

const thirdPromise = () => {
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            resolve("Third Promise")
        }, 1000);
    })
}

async function asyncParalel() {
    await firstPromise().then(response => console.log(response))
    await secondPromise().then(response => console.log(response))
    await thirdPromise().then(response => console.log(response))
}

asyncParalel()
```
