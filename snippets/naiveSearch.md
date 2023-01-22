---
title: naiveSearch
tags: algorithm,array
cover: blog_images/image.jpg
firstSeen: 2023-01-22T18:53:24+00:0
---

Searches an string/string and counts the number of times a pattern occurs in the string/array
using a Naive Search algorithm.

- Takes in `st` and `pattern`. Searching the frequency `pattern` occurs in `array`.
- Declare `count` to 0, which will keep track the frequency of pattern.
- Start looping on `st` and then start nested loop on `pattern`. 
- Break the inner loop if no match found with `pattern` and iterate next for the outerloop.
- Incriment count if `pattern` fouund in the iteratoin.

```js
const naiveSearch = (st,pattern) =>
  {
    let count =0;
    for(let i = 0; i < st.length; i++) {
       for(let j = 0; j < pattern.length; j++) {
            if(st[i + j] !== pattern[j]) break;
            if(j === pattern.length - 1) count++;
        }
    }

    return count;
  }
```

```js
naiveSearch("catdogdogcat", "cat"); // 2
```
