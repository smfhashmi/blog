---
author: "Hashmi Mohammed"
title: "Closures | Lexical scope"
date: 2025-01-15
description: "practicing closures and lexical scope and output based questions"
thumbnail: https://images.pexels.com/photos/574073/pexels-photo-574073.jpeg
tags: ["js_prep_2025", "closures"]
---

## Lexical scope

a lexical scope in javascript means a variable defined outside the function can
be accessible inside a function and the opposite is not true

:white_check_mark:

```javascript
var username = 'hashmi'
// Global scope
function local() {
  // Local scope
  console.log(username);
}
local()
```

the above example is called lexical scope ``var`` defined outside the function
can be accessible inside a function

:x:

```javascript
function local() {
  var username = 'hashmi';
}
console.log(username);
```

## closure

```javascript
// global scope
function local() {
  var username = 'hashmi'
  function displayName() {
    alert(username)
  }
  displayName()
}
local()
```

- the `displayName` function in the local is called closure

## uses

- closures makes it possible functions to have private variables
- closures make sure to control what is there and not present in a function

``` javascript
function myfunc() {
  var name = 'hashmi'
  function displayName() {
    console.log(`displayname is ${name}`)
  }
  return displayName;
}

myfunc()();
```

``` javascript
function myfunc () {
  var name = 'hashmi'
  function displayName (num) {
    console.log(`displayname is ${name} and number is ${num}`)
  }
  return displayName
}

myfunc()(5)
```

- we can called the insider function with double parathesis

## closure scope chain

every closure has 3 scopes

- local scope
- outer functions scope
- global scope


## Block scope and shadowing

``` javascript
let count = 0;
(function printCount() {
  if (count === 0) {
    let count = 1 // shadowing
    console.log(count) //o/p = 1
  }
  console.log(count) // o/p = 0
}

)()

```

## time optimization

closures can be very helpful in optimizing the time

```javascript
// Time optimization

function timeOptimization () {
  let a = []
  for (let i = 0; i < 1000000; i++) {
    a[i] = i * i
  }

  return function (index) {
    console.log(a[index])
  }
}

const closure = timeOptimization()
console.time('5')
closure(6)
console.timeEnd('5')
```

## what is module pattern ?

``` javascript
var Module = (function () {
  function private() {
    console.log('private')
  }

  return {
    public: function () {
      console.log('public');
    }
  }
}
)()

Module.public()
Module.private()
```

##  Rewrite the function in such a way the output gets printed once even though the function is called multiple times.


``` javascript
function like () {
  let called = 0
  return function () {
    if (called > 0) {
      console.log('liked')
    } else {
      called++
    }
  }
}

like()
```

## using caching or memoize

``` javascript
function memoize(func) {
  let res = {};

  return function (...args) {
    const argsIndex = JSON.stringify(args);
    if (!res[argsIndex]) 
             res[argsIndex] = func(...args);
    return res[argsIndex];
  };
}

const clumsysquare = memoize((num) => {
  for (let i = 1; i <= 100000000; i++) {}

  return num * 2;
});

```
