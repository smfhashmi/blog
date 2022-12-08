---
author: "Hashmi Mohammed"
title: "Recursion"
date: 2022-12-08
description: "this recurisive function for jsalgo"
tags: ["recursion", "algorithms", "recursive fibonacci", "recursive factorial"]
---
Recurrsion 
----------

![biochart: bigocomplexity](/blog/img/bigocomplexity_chart.png)

few points to note

*   every recursion should have a base case and condition to terminate the recursion
*   it will solve a problem but it does not always translate to a faster solution
*   it is not straight forward to understand, do not give up

Recursive fibonacci sequence
----------------------------

the first two numbers in the sequence are 0 and 1. (0,1,1,2,3,5,8,13.....)

recurisveFibonacci(0) => 1
recurisveFibonacci(2) => 1
recurisveFibonacci(4) => 3

Tips for recursive solution
---------------------------

* Figure out to break down the problem into smaller versions of the same problem

<kbd>f(n) = f(n-1) + f(n-2)</kbd>

```javascript
  function recursiveFibonacci(n){
    if(n < 2){
        return n
    }
    return recursiveFibonacci(n-1) + recursiveFibonacci(n-2)
  }
```

```javascript
var fs = [0,1]
function recursiveFibonacci(n) {
    if(fs.length <= n) {
        fs.push(fs[fs.length - 1] + fs[fs.length - 2])
        recursiveFibonacci(n)
    }else{
        console.log(fs[n])
    }
}

console.log(recursiveFibonacci(5))
```
*For Fibonacci recursive is not a feasible solution because it is O(2^n) iterative BigO is good O(n)*



Recursive Factorial
-------------------
<kbd>n! = n * (n-1)</kbd>

```javascript

function recursiveFactorial(n){
    if(n == 0){
        return 1
    }
    return n * recursiveFactorial(n-1)
}

console.log(recursiveFactorial(6))
```

*BigO = O(n) liner time complexity*