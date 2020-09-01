---
title: JavaScript Destructuring
---

JavaScript destructuring is an alternative way to retrieving information from objects and arrays.

## Object Destructuring

Traditionally in JS if you want to add a property you would use dot-notation. And because of how dot-notation works, if you want to retrieve that property it would also have to be one at a time. The same is true when trying to add multiple properties using JS object literal notation

```js
// Using dot-notation
let name = {}
name.first = 'Fernando'
name.middle = 'Ivan'
name.last = 'Sanchez'


let first = name.first
let middle = name.middle
let last = name.last

```

```js
// Using object literals

let name = {
  first: 'Fernando',
  middle: 'Ivan',
  last: 'Sanchez'
}

let first = name.first
let middle = name.middle
let last = name.last

```

Object destructuring allows us to retrieve multiple keys from an object all at once. Remember **if you want to extract properties from an object, do it on the left side of the equal sign**

```js
let name = {
  first: 'Fernando',
  middle: 'Ivan',
  last: 'Sanchez'
}

let { first, middle, last } = name
```

## Object function destructuring

It is also possible to destructuring the result of a function.

```js

function getName(){
  return{
    first: 'fernando',
    middle: 'ivan',
    last: 'sanchez'
  }
}

let { first, middle, last } = getName()
```

## Array destructuring

Not as common as object destructuring but still useful when the location of the array is a differentiator of that array.

`let name = ['Fernando', 'Ivan', 'Sanchez']`

Similar to object dot literal, we have to retrieve data one by one.

```js
first = name[0]
middle = name[1]
last = name[2]
```

But we destructuring we can do this!

`let [first, middle, last] = name`

## Destructuring renaming

What if we don't want to use the same variable name defined in an object? Let's take this poorly written code ( Please don't use single letter variable names )

```js
let name = {
  f: 'fernando',
  m: 'ivan',
  l: 'sanchez'
}
```

We can rename! 

```
let { f: first, m: middle, l: location } = name
console.log(first) // fernando
console.log(middle) // ivan
console.log(last) // sanchez
```




