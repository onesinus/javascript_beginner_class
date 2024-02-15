## Linear Search

```javascript
function linearSearch(data, dataToFind) {
    for (let i = 0; i < data.length; i++) {
        if (data[i] === dataToFind) {
            return i
        }
    }
    return -1
}

// Test Cases
console.log(linearSearch([1, 2, 3, 4, 5], 3)) // 2
console.log(linearSearch([2, 3, 5, 7, 1], 7)) // 3
console.log(linearSearch([1, 2, 3], 10)) // -1
```