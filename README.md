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
function insertionSort(array) {
  // run time --> O(n^2)
  let length = array.length;
  for (let i = 1; i < length; i++) {
    let tmp = array[i];
    let currentIndex = i;
    while (currentIndex > 0 && array[currentIndex - 1] > tmp) {
      array[currentIndex] = array[currentIndex - 1];
      currentIndex--;
    }
    array[currentIndex] = tmp;
  }
  return array;
}
```

### Selection Sort

```javascript
function selectionSort(array) {
  // runtime -->  O(n^2)
  let startIdx = 0;
  let length = array.length;
  while (startIdx < length - 1) {
    let smallestIdx = startIdx;
    for (let i = startIdx + 1; i < length; i++) {
      if (array[smallestIdx] > array[i]) smallestIdx = i;
    }
    swap(startIdx, smallestIdx, array);
    startIdx++;
  }
  return array;
}

function swap(i, j, array) {
  let tmp = array[j];
  array[j] = array[i];
  array[i] = tmp;
}
```

### Quick Sort

```javascript
function quickSort(array) {
  let start = 0;
  let end = array.length - 1;
  helper(array, start, end);
  return array;
}

function helper(array, start, end) {
  if (start >= end) return;
  let pivot = start;
  let left = start + 1;
  let right = end;

  while (right >= left) {
    if (array[left] > array[pivot] && array[right] < array[pivot]) {
      swap(left, right, array);
    }
    if (array[left] <= array[pivot]) left++;
    if (array[right] >= array[pivot]) right--;
  }
  swap(pivot, right, array);
  let tmp = right - start - 1 < end - (right + 1);
  if (tmp) {
    helper(array, start, right - 1);
    helper(array, right + 1, end);
  } else {
    helper(array, right + 1, end);
    helper(array, start, right - 1);
  }
}

function swap(i, j, array) {
  let tmp = array[i];
  array[i] = array[j];
  array[j] = tmp;
}
```

### Heap Sort

```javascript
```

### Merge Sort

```javascript
```
