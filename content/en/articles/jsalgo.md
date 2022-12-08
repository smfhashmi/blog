---
author: "Hashmi Mohammed"
title: "JS Algorithms"
date: 2022-12-06
description: "I am learning js alogrithms"
tags: ["algorithms", "js"]
# thumbnail: img/dunes.jpg
# thumbnail: https://picsum.photos/400
---
Javascript Algorithms Notes
===========================

algorithm anlysis
-----------------

it can be done via time complexity and space complexity

algo represent complexity
-------------------------

mathematical represent tools to represent time and space complexity

there are three asymptotic notations

1.  there are three asymptotic notations
2.  Big-O Notation -> worst case complexity
3.  Omega Notation -> Best case complexity
4.  Theta Notation -> Average case complexity

BigO Notation Time Complexity
-----------------------------

there is no faster approach in algorithm as the time for the execution of the algo depends of various factors like input size, os speed, etc
```javascript
for(i=1; i<= n; i++){
    for(j=1; j<=i, j++){

    }
}
```

Quadratic O(n2)

Input size reduces by half every iteration then it is logarithmic O(logn)

BigO Notation Space Complexity
------------------------------

if the algorithm doesnot need extra memory and the memory needed doesn't depend on input size then space complexity is constant

*   O(1) constant space complexity
*   O(2) Linear space complexity
*   O(3) logarithmic space complexity

![](/bigocomplexity_chart.png)

Few points to note

*   Multiple solutions exists for the same problem and there is no one right solution, different algorithms work well under different constraints
*   same algo in same programming languagge can be implemented in different ways
*   Rather than writing clever code write a simple code to read and maintain

1.  **O(1)** is constant space complexity
2.  **O(2)** is linear space complexity
3.  **O(3)** is Logarthmic space complexity

Objects BigO
------------

it is collection of keys and values, no matter how many attributes in the object it takes same amount of time to insert or remove the properites in the object

*   insert -> O(1)
*   Remove -> O(1)
*   Access -> O(1)
*   search -> o(n) linear time complexity

Arrays BigO
-----------

*   search is linear time complexity
*   Access is constant time complexity
*   insert/remove is constant time complexity
*   push/pop is O(1) constant
*   shift/unshift/concat/slice/splice are linear O(n)
*   foreach map filter reduce are linear O(n)

BigO Guide
----------

*   calculation not depend on input size O(1)
*   loop O(n) is linear
*   nested loops O(n^2)
*   input size reduce by half O(logn)

Math Algorithms
---------------

*   Fibonacci sequence
*   Factorial of Number
*   Prime Number
*   Power of two
*   Recurrsion
*   Fibonacci sequence with recurrsion
*   Fibonacci Number with recurrsion

Fibonacci sequence
------------------
```javascript
function fibonacci (number) {
    const fib = [0,1]
    for(i=2; i < number; i++) {
        fib[i] = fib[i-1] + fib[i-2]
    }
    return fib
}
console.log(fibonacci(4))
```

Factorial
---------
```javascript
function factorial (n) {
    const result = 1;
    for(i=2; i <= n ; i++){
        result = result * i
    }
    return result
}
console.log(factorial(5))
```

prime number
------------
```javascript
// this is a short way to know the prime number
function primenumber (n) {
    if (n < 2) {
        return false
    }

    for(i = 2; i < Math.sqrt(n) ; i++){
        if(n%i === 0){
            return false
        }
    }
    return true
}

function primenumber (n) {
    if (n < 2) {
        return false
    }

    for(i = 2; i < n ; i++){
        if(n%i === 0){
            return false
        }
    }
    return true
}
console.log(primenumber(13))
```

Power of two
------------
```javascript
// this is a short way to know the power of two
function poweofTwoBitwise (n) {
    if(n < 1){
        return false
    }
    return (n & (n-1)) === 0
}
```
<kbd>Big0 = O(1)</kbd>

```javascript
function powerofTwo(n) {
    if(n < 1) {
      return false
    }
    while (n > 1) {
        if(n % 2 !== 0){
            return false
        }
        n = n/2
    }
    return true
}

console.log(powerofTwo(12));
console.log(powerofTwo(64));
```
<kbd>Big0 = O(logn)</kbd>
                        
                        
                    
