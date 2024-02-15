## Selection Sort

```javascript
// Reference: https://visualgo.net/en/sorting?slide=1-2
function selectionSort(data) {
    console.log(`Sebelum diurutkan: ${data}`);
    for (let i = 0; i < data.length; i++) {
        console.log(`Proses ke-${i} = ${data}`);
        let idx_smallest_number = i
        for (let j = i + 1; j < data.length; j++) {
            if (data[idx_smallest_number] > data[j]) {
                idx_smallest_number = j
            }
        }
        // proses swap (pertukaran data)
        const temp_data_i = data[i]
        data[i] = data[idx_smallest_number]
        data[idx_smallest_number] = temp_data_i
    }
    console.log(`Setelah diurutkan: ${data}`);
    return data
}

// Test Cases
// selectionSort([4, 5, 2, 1, 0, 3]) // Expected Output: [0, 1, 2, 3, 4, 5]
// selectionSort([104, 94, 201, 43])
selectionSort([27, 38, 4, 43, 9, 82, 10])
```