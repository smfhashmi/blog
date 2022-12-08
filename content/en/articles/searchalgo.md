---
author: "Hashmi Mohammed"
title: "Search Algorithms"
date: 2022-12-08
description: "this is search algorithms post"
tags: ["linear search", "Binary search"]
---
![biochart: bigocomplexity](/blog/img/bigocomplexity_chart.png)

Problem
-------

problem: arr = [-5, 2,10,4,6], t = 10 => should return 2
problem: arr = [-5, 2,10,4,6], t = 6 => should return 4
problem: arr = [-5, 2,10,4,6], t = 20 => should return -1

Linear Search
-------------

```javascript
function lsearch(n) {
    let arr = [-5, 2,10,4,6]
    let idx = -1;
    arr.map(function(value, index){
        if(value === n){
            idx = index
        }
    })
    return idx
}
console.log(lsearch(10))
```
*BigO = O(n) liner time complexity*


Binary Search
-------------
Binary search only works on sorted array, if not sorted array linear search will get applied

### psuedocode
- if the array has no elements return -1
- if the array has elements find the middle element and if target is equal to middle element return middle element index
- if the target is less than middle element binary search left half of the array
- if the target is greater than middle element binary search right half of the array

*if there are two items the first item is the middle item same applies to the even number of elements*

```javascript
function binarySearch(array, target) {
    let leftIndex = 0
    let rightIndex = array.length - 1

}

binarySearch([-5, 2,10,4,6], 10)
binarySearch([-5, 2,10,4,6], 4)
binarySearch([-5, 2,10,4,6], 20)

```