## Insertion Sort

```javascript
/* Versi while */
// function insertionSort(data) {
//     for (let i = 0; i < data.length; i++) {
//         let temp_data = data[i]
//         let j = i - 1
//         while (j >= 0 && data[j] > temp_data) {
//             // swap data
//             data[j + 1] = data[j]
//             j--
//         }
//         data[j + 1] = temp_data
//     }
//     return data
// }

/* Versi for */
function insertionSort(data) {
    for (let i = 1; i < data.length; i++) {
        const temp_data = data[i]
        let j
        for (j = i - 1; j >= 0 && data[j] > temp_data; j--) {
            data[j + 1] = data[j]
        }
        data[j + 1] = temp_data
    }
    return data
}
console.log(insertionSort([4, 5, 2, 1, 0, 3])) // Expected Output: [0, 1, 2, 3, 4, 5]
console.log(insertionSort([104, 94, 201, 43]));
console.log(insertionSort([27, 38, 4, 43, 9, 82, 10]));
```