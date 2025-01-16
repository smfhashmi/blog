---
author: "Hashmi Mohammed"
title: Currying | partial application
date: 2025-01-15
description: "using currying and some output based questions for practice"
thumbnail: https://images.pexels.com/photos/674483/pexels-photo-674483.jpeg
tags: ["js_prep_2025", "closures"]
---

## currying in javascript

```javascript
function f (a) {
  return function (b) {
    return `${a}, ${b}`
  }
}
console.log(f(5)(6))

```

## infinite currying in javascript

```javascript
function add (a) {
  return function (b) {
    if (b) return add(a + b)
    return a
  }
}

add(2)(3)(4)()
```

## real world scenario applying currying Manipulating DOM

```html

<div>
  <h1 id="header">Hashmi</h1>
</div>

```

``` javascript
const updateElemText = id => content => document.querySelector(`#${id}`).textContent= content;

const updateHeaderText = updateElemText('header');
updateHeaderText('Hello!');

```
