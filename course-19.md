## Binary Search

```javascript
// 1. data harus dalam keadaan berurutan
// 2. Ketika data yang di cari sama dengan data tengah, maka kembalikan index data tengah
// Jika data yang dicari tidak sama:
// 3. Jika lebih kecil dari data tengah,maka akan mencari ke kiri 
//    (sekumpulan data yang posisinya SEBELUM data tengah)
// 4. Jika lebih besar dari data tengah, maka akan mencari ke kanan
//    (sekumpulan data yang posisinya SESUDAH data tengah)


function binarySearch(sortedData, dataToFind) {
    let lowest_index = 0
    let highest_index = sortedData.length - 1
    while (lowest_index <= highest_index) {
        const mid_index = Math.floor((lowest_index + highest_index) / 2)
        if (sortedData[mid_index] === dataToFind) {
            return mid_index
        } else if (sortedData[mid_index] < dataToFind) {
            lowest_index = mid_index + 1
        } else {
            highest_index = mid_index - 1
        }
    }
    return -1
}

// test cases
console.log(binarySearch([1, 3, 5, 7], 3)) // 1
console.log(binarySearch([1, 3, 5, 7], 5)) // 2
console.log(binarySearch([1, 3, 5, 7], 7)) // 3
console.log(binarySearch([1, 3, 5, 7], 17)) // -1
```