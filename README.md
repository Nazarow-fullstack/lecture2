# JavaScript Scope and Hoisting

## Table of Contents
1. Scope
   - Global Scope
   - Local Scope
   - Block Scope
2. Hoisting
   - Variable Hoisting
   - Function Hoisting




## Scope
Scope determines the accessibility of variables and functions in different parts of your code. There are several types of scope in JavaScript:
At its core, scope in JavaScript refers to the context or environment in which variables are declared and can be accessed. It dictates the visibility and lifetime of a variable, determining where in your code a particular variable is valid and accessible.
   ### Global Scope
   Variables declared outside any function or block are in the global scope.
   ```javascript
    let a=5  //Global
    let b=8  //Global
    const name="teacher"  //Global
   ```
   ### Local Scope
   work inside function
   ```javascript
function isNum(num) {
    let cnt="" //local
    cnt+=num  //local

    return cnt===num ? false:true  //local
}
console.log(isNum("5"));
   ```
   ### Block Scope
   Scope only work inside loop and condition
   ```javascript
    if(true){
let a=5 //block
let b=6 //block
console.log(a+b) //block
}
   ```

# Hoisting
Before we delve into the specifics, let's demystify what hoisting means in JavaScript. Hoisting is the behind-the-scenes process that moves variable and function declarations to the top of their containing scope during the compilation phase. This allows you to use them before they are officially declared in your code.

![hoisting](https://miro.medium.com/v2/resize:fit:1200/1*kjHbzVknczb2YffCjbbrFA.png)

it`s work with function
```javascript
condole.log(name(5))
function  name(num){
return num-1
}
```


but with var the answer will be unnderfind becouse it  read a var but don`t reat the mean of var
```javascript
condole.log(a)
var a=4
//answer will be underfind
```


Variables defined with let and const are hoisted to the top of the block, but not initialized
```javascript
condole.log(a,b)
let a=4
let b=8
//Cannot access 'a' before initialization
```
#### And it`s called temporary dead zone tdz

