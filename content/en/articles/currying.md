---
author: "Hashmi Mohammed"
title: Currying | partial application
date: 2025-01-15
description: "using currying and some output based questions for practice"
thumbnail: https://images.pexels.com/photos/674483/pexels-photo-674483.jpeg
tags: ["js_prep_2025", "closures"]
---

currying in javascript

```javascript
function f (a) {
  return function (b) {
    return `${a}, ${b}`
  }
}
console.log(f(5)(6))

```
