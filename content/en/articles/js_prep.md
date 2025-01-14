
---
author: "Hashmi Mohammed"
title: "JS preparation functions 2025"
date: 2025-01-14
description: "practicing function expressions callbacks IIFE, hoisting, scope"
tags: ["js_prep_2025", "functions"]
---

# javascript functions 2025 

Functions in javascript
what is function declaration

```javascript
function square(num) {
  return num*num;
}
```

what is function expression
when you store function under variable then it is function expression

```javascript
const square1 = function(num) {
  return num*num;
}
```

what are first class functions
functions can be passed to another functions as arguments

```javascript
function displaySquare(fn) {
  return fn(5)
}
console.log(displaySquare(square));
```

what is IIFE
immediately invoked function expressions

```javascript
(function square(num) {
  console.log(num*num);
})(5)
```


### function scope

```javascript
var n1 = 3;
var n2 = 4;
var name = 'hashmi'

function multiple(){
  return n1 * n2;
}

function funcScope () {
  var n1 = 2;
  var n2 = 5;

  return `${name} the sum of numbers is ${n1 + n2}`
}

```

* function scope output based question

```javascript
for (let i = 0; i < 5; i++) {
  setTimeout(() => {
    console.log(i)
  }, i * 1000);
}
```

since let will create a blocked scope the output will be 0,1,2,3,4,5


function hositing output based question

```javascript
var x = 5;
func();

function func() {
  console.log(x);
  var x = 7;
}
```

* so what is happening here is that the func and x are hoisted globally
* when x is hoisted it is undefined
* when func is hoisted it will check x and logs as undefined
* when executes completely it will go into the block scope based and returns 7


### question: params vs arguments - o/p based question

``` javascript
const fn = (a,b,c, ...numbers) {
  console.log(a, b, c, numbers)
}

fn(1,2,3,4,5,6)

//output = 1, 2, 3, [4, 5, 6]
```

### what is a callback function

a callback function is a function which gets passed as the argument to 
another function and then gets executed inside the other function
