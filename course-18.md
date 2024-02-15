## Basic Recursive

```javascript
/* Example 1 */
function recursive(counter = 0) {
    if (counter >= 5) { // stopper (yang membuat fungsi recursive berhenti)
        return "Finish" // jika tidak ada ini recursive akan berjalan tanpa henti
    }
    console.log("Pemanggilan fungsi recursive() ke-", counter)
    return recursive(counter + 1) // memanggil fungsi (dirinya sendiri)
}

console.log(recursive())

/* Example 2: factorial */
let result = 5;
function factorial(num) {
    if (num != 1) {
        num--
        console.log(`${result} x ${num}`);
        result = result * num
        return factorial(num)
    }
    else {
        return result;
    }
}
console.log(factorial(5))
```