---
author: "Hashmi Mohammed"
title: "Closures | Lexical scope"
date: 2025-01-15
description: "practicing closures and lexical scope and output based questions"
thumbnail: https://images.pexels.com/photos/574073/pexels-photo-574073.jpeg
tags: ["js_prep_2025", "closures"]
---
# Closures in javascript

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

- we can called the insider function with double parathesis
