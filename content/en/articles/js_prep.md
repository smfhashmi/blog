
---
author: "Hashmi Mohammed"
title: "JS preparation functions 2025"
date: 2025-01-14
description: "practicing function expressions callbacks IIFE, hoisting, scope"
thumbnail: https://images.pexels.com/photos/6804604/pexels-photo-6804604.jpeg
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

### arrow functions

``` javascript
const add = function(num1, num2) {
  return num1 + num2
}

const add = () => {
  return num1 + num2
}
```

* arrow functions are used for cleaner syntax

* implicit "return" keyword

``` javascript
const add = (num1, num2) => num1 + num2
```

* in arrow function we can't able to pass aruguments keyword

``` javascript
// normal function
function normal () {
  console.log(arguments)
}

console.log(normal(1,2,3,4))
// this will work

const argumentArrow = () => {
  console.log(arguments)
}

console.log(argumentArrow(1,2,34));
// this will not work in arrow function as for arrow function we need to define
// arguments
```


* using the *this* keyword

```javascript
let user = {
  name: 'hashmi',
  rc1: () => {
    console.log(`I am ${this.name}`);
  },
  rc2() => {
    console.log(`I am ${this.name}`);
  }
}

console.log(`this is rc1 output , ${user.rc1()}`);
console.log(`this is rc2 output , ${user.rc2()}`);
```
