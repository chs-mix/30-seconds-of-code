---
title: countingSort
tags: algorithm,array
cover: blog_images/image.jpg
firstSeen: 2023-01-22T05:44:50+00:00
---

Sorts an array of numbers using the countingSort algorithm.

- Takes in `arr` an array of integers to be sorted and `x` the length of `arr`
- Declare variables `k` which is set as the max num from `arr` and declares `t` 
- `temp` is a variable that holds  zero value as the same length of max elemet + 1
- count the amount of times each number in `arr` occurs and stores in `temp`
- Updating counts based on previous index and add elements of `arr` to newley created array 
`outputArr`
-  `outputArr` will be returned with the sorted order of elements
- cite : https://learnersbucket.com/tutorials/algorithms/counting-sort-algorithm-in-javascript/

```js
const countingSort = (arr, x = arr.length) =>
{let k = Math.max(...inputArr),t;
  const temp = new Array(k + 1).fill(0);
  for(let i = 0; i < n; i++){
    t = arr[i];
    temp[t]++;
  }
  for(let i = 1; i <= k; i++){
    temp[i] = temp[i] + temp[i - 1];  
  }
  const outputArr = new Array(n).fill(0);
  for(let i = n - 1; i >= 0; i--) {
    t = arr[i];
    outputArr[temp[t] - 1] = t;  
    temp[t] = temp[t] - 1;		
   }
  
  return outputArr;}
```

```js
countingSort([9,4,5,1]); // [1,4,5,9]
```
