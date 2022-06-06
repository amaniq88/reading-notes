# ES6 Overview
Table of contents
Variable declaration
Constant declaration
Arrow function syntax
Template literals
Implicit returns
Key/property shorthand
Method definition shorthand
Destructuring (object matching)
Array iteration (looping)
Default parameters
Spread syntax
Classes/constructor functions
Inheritance
Modules - export/import
Promises/callbacks
Variables and constant feature comparison
I explain the concepts of scope and the differences between let, var, and const in the Understanding Variables, Scope, and Hoisting in JavaScript resource on DigitalOcean. This table provides a brief overview.

Keyword	Scope	Hoisting	Can Be Reassigned	Can Be Redeclared
var	Function scope	Yes	Yes	Yes
let	Block scope	No	Yes	No
const	Block scope	No	No	No
Variable declaration
ES6 introduced the let keyword, which allows for block-scoped variables which cannot be hoisted or redeclared.

ES5
var x = 0
ES6
let x = 0
MDN Reference: let
Constant declaration
ES6 introduced the const keyword, which cannot be redeclared or reassigned, but is not immutable.

ES6
const CONST_IDENTIFIER = 0 // constants are uppercase by convention
MDN Reference: const
Arrow functions
The arrow function expression syntax is a shorter way of creating a function expression. Arrow functions do not have their own this, do not have prototypes, cannot be used for constructors, and should not be used as object methods.

ES5
function func(a, b, c) {} // function declaration
var func = function (a, b, c) {} // function expression
ES6
let func = (a) => {} // parentheses optional with one parameter
let func = (a, b, c) => {} // parentheses required with multiple parameters
MDN Reference: Arrow functions
Template literals
Concatenation/string interpolation
Expressions can be embedded in template literal strings.

ES5
var str = 'Release date: ' + date
ES6
let str = `Release Date: ${date}`
MDN Reference: Expression interpolation
Multi-line strings
Using template literal syntax, a JavaScript string can span multiple lines without the need for concatenation.

ES5
var str = 'This text ' + 'is on ' + 'multiple lines'
ES6
let str = `This text
            is on
            multiple lines`
Note: Whitespace is preserved in multi-line template literals. See Removing leading whitespace in ES6 template strings.

MDN Reference: Multi-line strings
Implicit returns
The return keyword is implied and can be omitted if using arrow functions without a block body.

ES5
function func(a, b, c) {
  return a + b + c
}
ES6
let func = (a, b, c) => a + b + c // curly brackets must be omitted
MDN Reference: Function body
Key/property shorthand
ES6 introduces a shorter notation for assigning properties to variables of the same name.

ES5
var obj = {
  a: a,
  b: b,
}
ES6
let obj = {
  a,
  b,
}
MDN Reference: Property definitions
Method definition shorthand
The function keyword can be omitted when assigning methods on an object.

ES5
var obj = {
  a: function (c, d) {},
  b: function (e, f) {},
}
ES6
let obj = {
  a(c, d) {},
  b(e, f) {},
}
obj.a() // call method a
MDN Reference: Method definitions
Destructuring (object matching)
Use curly brackets to assign properties of an object to their own variable.

var obj = {a: 1, b: 2, c: 3}
ES5
var a = obj.a
var b = obj.b
var c = obj.c
ES6
let {a, b, c} = obj
MDN Reference: Object initializer
Array iteration (looping)
A more concise syntax has been introduced for iteration through arrays and other iterable objects.

var arr = ['a', 'b', 'c']
ES5
for (var i = 0; i < arr.length; i++) {
  console.log(arr[i])
}
ES6
for (let i of arr) {
  console.log(i)
}
MDN Reference: for...of
Default parameters
Functions can be initialized with default parameters, which will be used only if an argument is not invoked through the function.

ES5
var func = function (a, b) {
  b = b === undefined ? 2 : b
  return a + b
}
ES6
let func = (a, b = 2) => {
  return a + b
}
func(10) // returns 12
func(10, 5) // returns 15
MDN Reference: Default paramters
Spread syntax
Spread syntax can be used to expand an array.

ES6
let arr1 = [1, 2, 3]
let arr2 = ['a', 'b', 'c']
let arr3 = [...arr1, ...arr2]

console.log(arr3) // [1, 2, 3, "a", "b", "c"]
Spread syntax can be used for function arguments.

ES6
let arr1 = [1, 2, 3]
let func = (a, b, c) => a + b + c

console.log(func(...arr1)) // 6
MDN Reference: Spread syntax
Classes/constructor functions
ES6 introducess the class syntax on top of the prototype-based constructor function.

ES5
function Func(a, b) {
  this.a = a
  this.b = b
}

Func.prototype.getSum = function () {
  return this.a + this.b
}

var x = new Func(3, 4)
ES6
class Func {
  constructor(a, b) {
    this.a = a
    this.b = b
  }

  getSum() {
    return this.a + this.b
  }
}

let x = new Func(3, 4)
x.getSum() // returns 7
MDN Reference: Classes
Inheritance
The extends keyword creates a subclass.

ES5
function Inheritance(a, b, c) {
  Func.call(this, a, b)

  this.c = c
}

Inheritance.prototype = Object.create(Func.prototype)
Inheritance.prototype.getProduct = function () {
  return this.a * this.b * this.c
}

var y = new Inheritance(3, 4, 5)
ES6
class Inheritance extends Func {
  constructor(a, b, c) {
    super(a, b)

    this.c = c
  }

  getProduct() {
    return this.a * this.b * this.c
  }
}

let y = new Inheritance(3, 4, 5)
y.getProduct() // 60
MDN Reference: Subclassing with extends
Modules - export/import
Modules can be created to export and import code between files.

index.html
<script src="export.js"></script>
<script type="module" src="import.js"></script>
export.js

let func = (a) => a + a
let obj = {}
let x = 0

export {func, obj, x}
import.js
import {func, obj, x} from './export.js'

console.log(func(3), obj, x)
MDN Reference: export
MDN Reference: import
Promises/Callbacks
Promises represent the completion of an asynchronous function. They can be used as an alternative to chaining functions.

ES5 callback
function doSecond() {
  console.log('Do second.')
}

function doFirst(callback) {
  setTimeout(function () {
    console.log('Do first.')

    callback()
  }, 500)
}

doFirst(doSecond)
ES6 Promise
let doSecond = () => {
  console.log('Do second.')
}

let doFirst = new Promise((resolve, reject) => {
  setTimeout(() => {
    console.log('Do first.')

    resolve()
  }, 500)
})

doFirst.then(doSecond)
An example below using XMLHttpRequest, for demonstrative purposes only (Fetch API would be the proper modern API to use).

ES5 callback
function makeRequest(method, url, callback) {
  var request = new XMLHttpRequest()

  request.open(method, url)
  request.onload = function () {
    callback(null, request.response)
  }
  request.onerror = function () {
    callback(request.response)
  }
  request.send()
}

makeRequest('GET', 'https://url.json', function (err, data) {
  if (err) {
    throw new Error(err)
  } else {
    console.log(data)
  }
})
ES6 Promise
function makeRequest(method, url) {
  return new Promise((resolve, reject) => {
    let request = new XMLHttpRequest()

    request.open(method, url)
    request.onload = resolve
    request.onerror = reject
    request.send()
  })
}

makeRequest('GET', 'https://url.json')
  .then((event) => {
    console.log(event.target.response)
  })
  .catch((err) => {
    throw new Error(err)
  })
  
  
  
  
  
