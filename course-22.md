## Merge Sort

```javascript
function joinAndSort(leftArr, rightArr) {
    const sortedArray = []
    while (leftArr.length && rightArr.length) {
        if (leftArr[0] <= rightArr[0]) {
            sortedArray.push(leftArr[0])
            leftArr = leftArr.slice(1)
        } else {
            sortedArray.push(rightArr[0])
            rightArr = rightArr.slice(1)
        }
    }

    while (leftArr.length) {
        sortedArray.push(leftArr.shift())
    }

    while (rightArr.length) {
        sortedArray.push(rightArr.shift())
    }


    return sortedArray
}

function mergeSort(data) {
    if (data.length < 2) {
        return data
    } else {
        const total_data = data.length
        const idx_middle = parseInt(total_data / 2)
        const left_arr = data.slice(0, idx_middle)
        const right_arr = data.slice(idx_middle, total_data)
        return joinAndSort(mergeSort(left_arr), mergeSort(right_arr))
    }
}

console.log(mergeSort([])) // []
console.log(mergeSort([4])) // [4]
console.log(mergeSort([4, 5, 2, 1, 0, 3]))
console.log(mergeSort([104, 94, 201, 43]));
console.log(mergeSort([27, 38, 4, 43, 9, 82, 10]));
```