## Basic Async vs Sync

```javascript
// synchronous: menjalankan code sesuai urutan SATU PER SATU (blocking)
console.log(">>>>>>>>>>>>>> SYNC");
console.log("1");
console.log("2");
console.log("3");

function a() {
    console.log("A");
}

function b() {
    console.log("B");
}

function c() {
    console.log("C");
}

a()
b()
c()

// asynchronous (TIDAK  BLOCKING), ga nunggu perintah lain selesai
console.log(">>>>>>>>>>>>>> ASYNC");
console.log("1");
setTimeout(() => {
    console.log("2");
}, 100); // kita delay selama 100 ms
console.log("3");

async function d() {
    console.log("D");
}

async function e() {
    setTimeout(() => {
        console.log("E");
    }, 200);
}

async function f() {
    console.log("F");
}

d()
e()
f()
```