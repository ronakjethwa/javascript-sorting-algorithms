# JavaScript | Sorting Algorithms

### Bubble Sort

```javascript
function bubbleSort(array) {
  // run time --> O(n^2) 
  let length = array.length;

  for (let i = 0; i < length - 1; i++) {
    for (let j = 0; j < length - 1; j++) {
      if (array[j] > array[j + 1]) {
        let tmp = array[j + 1];
        array[j + 1] = array[j];
        array[j] = tmp;
      }
    }
  }
  return array;
}
```

### Insertion Sort
```javascript

```

### Selection Sort
```javascript

```

### Quick Sort
```javascript

```

### Heap Sort
```javascript

```

### Merge Sort
```javascript

```
