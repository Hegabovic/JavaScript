<div id="top"></div>

[//]: # ([![LinkedIn][linkedin-shield]][linkedin-url])

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/Hegabovic/JavaScript.git">
    <img src="images/logo.png" alt="Logo" width="80" height="80">
  </a>

<h3 align="center">Understand JavaScript</h3>

  <p align="center">
    from zero to hero tutorial
    <br />
    <a href="https://github.com/Hegabovic/JavaScript.git"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/Hegabovic/JavaScript.git">View Demo</a>
    ·
    <a href="https://github.com/Hegabovic/issues">Report Bug</a>
    ·
    <a href="https://github.com/Hegabovic/issues">Request Feature</a>
  </p>
</div>



<!-- TABLE OF CONTENTS -->

<details>
<summary>Table of Contents</summary>
<ol>
    <li>
      <a href="#about-the-course">About The Course</a>
    </li>
    <li>
      <a href="#JavaScript-Features">JavaScript Features</a>
      <ul>
        <li><a href="#Type-system-of-JS">Type system of JS </a></li>
        <li><a href="#Where-To-Write-JS">Where To Write JS</a></li>
            <ul>
               <li><a href="#Internal-script">internal script</a></li>
               <li><a href="#External-script">External script</a></li>
            </ul>
      </ul>
    <li><a href="#Primitive-type-variables">Primitive type variables</a></li>
    <li><a href="#Number-type-declaration">Number type declaration</a></li>
      <ul>
        <li><a href="#Literal-creation">Literal creation</a></li>
        <li><a href="#Constructor-creation">Constructor creation</a></li>
      </ul>
    <li><a href="#Number-Literals-representation">Number Literals representation</a></li>
    <li><a href="#Dialogs">Dialogs</a></li>
    <li><a href="#parseInt-parseFloat-Algorithms">parseInt, parseFloat Algorithms</a></li>
    <li><a href="#NaN-not-a-number">NaN: not a number</a></li>
</ol>
</details>

<!-- ABOUT THE PROJECT -->
## about-the-course
javascript has many features, a long the way you will understand every point of the following
after studying the following you will have a solid background to kick-start your career in JS

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- JavaScript Features -->
## JavaScript Features
1. Loosely type language: not strongly typed language <br>
Variables type will be determined according to its value, note that you can know 
the type of any variable using `typeof(variable-name);` or `typeof variable-name; ` and it returns small letter
```sh
var x;           // type of x is undefined (not initlized)
var x = 10;      // type of x is number
var x = "ITI";   // type of x is string
```
2. Object based language
   * User defined objects
   * Language objects (Numbers, Math, Date, String,...)
   * Browser objects also called BOM (navigator, window, History)
   * HTML objects also called DOM 
3. Interpreted language <br>
it isn't a compiled language, and it operates from top to bottom : left to right
4. event handling 
5. Integrated with HTML 
6. Case Sensitive <br>
`var a;` is very different from `var A;`
<p align="right">(<a href="#top">back to top</a>)</p>

## Type system of JS 
### primitive types 
   * Undefined
   * String
   * Number
   * Null
   * boolean
### Object types
   * Date
   * Array

<p align="right">(<a href="#top">back to top</a>)</p>

## Where To Write JS
### Internal script 
1. internal HTML: Within script tag 
```sh
    <head>
        <script>
              // code
        </script>
    </head>
```
2. allowed writing Script codes inside body tag within script
```sh
    <body>
        <script>
              // code
        </script>
    </body>
```
3. inline script: event handling scripts
```sh
 <button onclick="function call();"/>   
```
<p align="right">(<a href="#top">back to top</a>)</p>

### External script
 - put script tag `<script></script>` before the end of the body tag.
```sh
    <body>
        
        <script src="test.js" ></script>
    </body>
```
 - javascript is a client side language so the user might close script running from browser settings.
```sh
 <noscript>
  <h3> Enable JS </h3>
 </noscript>   
```

<p align="right">(<a href="#top">back to top</a>)</p>

## Primitive type variables
- semicolon `;` is optional in JS. <br>
- `null` is used to reset reference.<br>
```sh
 var x ;         // Without initial value : variable from type undefined : undefined
 var x = 10;     // x value =  10  from type: number
 var x = "ITI";  // x value =  ITI from type: string
 var x = true;   // x value = true from type: boolean
 var x = null;   // x value = null from type: `OBJECT`  
```
<p align="right">(<a href="#top">back to top</a>)</p>

### Number type declaration 
to declare variable from type number:
### Literal creation 
 ```sh
   var x = 10;  // from type `Number`: prototype name : object Name
   x.toFixed(2); // create a wrapper object from type Number then access toFixed function then delete wrapper object
   
 ```
### Constructor creation: 
   - use keyword `new` plus `prototype` name.<br>
   - better as performance wise.
   - if you will use this variable so many times in your application use constructor creation, will create the object only 
one time, less hitting on the memory.<br>
   - in memory: reference and object, to get the value of the reference use `.valueof()` 
  ```sh
   var a = new Number(10);  // from type `Number`: prototype name : object Name
 ```
to compare between literal creation and constructor creation
 ```sh
   var x = 10; 
   var y = 10; 
   x == y >> TRUE 
   var a = new Number(10);
   var b = new Number(10);
   a == b >> False                    // because a,b are holding different identities (addresses)
   a.valueof() == b.valueof() >> TRUE // both have same state 
 ```
### Number Object language Object: not user defined object 
```sh
   var a = new Number(10); // you can put your own function in Number wrapper Object
   a.sayHello = function () {alert("Hello");};
 ```
to call your added function (constructor creation)
```sh
   a.sayHello();
 ```

<p align="right">(<a href="#top">back to top</a>)</p>

### Number Literals representation:
```sh
   var x = 1024;        // decimal : radix : 10 
   var x_hexa = 0x400;  // hexa_decimal
   var x_octal= 010;    // octal 
   var oneMillion = 1e6;
 ```
```sh
   var t1 = 123.2345;
   var t2 = 12345.678;
   t1.toPrecision(4) // use only four digits and round but it is mostly used to butify the numbers  
 ```
to change radix representation for your number, radix must be between 2 and 36.
```sh
(12345).toString(2);  // from decimal to binary 
(12345).toString(3);  // from decimal to radix 3 
(12345).toString(16); // from decimal to radix 16
(12343).toLocalString("ar-EG"); 
 ```
<p align="right">(<a href="#top">back to top</a>)</p>

### Dialogs 
 - `alert("String"|value)` : display it, then click ok to close the alert. has no return `(meaning return undefined)`
 - `prompt("message","default value")`: it always returns a String
   * `parseInt("String")`   >> return number(integral)
   * `parseFloat("String")` >> return number(may contain fraction part)
 - `confirm("massage")`: ok  (return true), cancel | if user clicked Esc (return false)
```sh
prompt("Enter Your Name","default-value");
confirm("Do you want to repeat ?");
 ```
<p align="right">(<a href="#top">back to top</a>)</p>

### parseInt, parseFloat Algorithms
 - Trimming String :remove spaces from start and end of input string `parseInt("  123  ")` => `parseInt("123")`
 - if length of result of trimmed String = 0 >> `return NaN` parseInt("  ") => parseInt("") => NaN <br>
 - else if length is greater than 0
   - check first letter in string if it is a digit => `return it` else return `NaN`
   - stop if `character is letter` or `reached to end of String` parseInt(" A1234 ") => parseInt("A1234") => `NaN`<br>

<p align="right">(<a href="#top">back to top</a>)</p>

### NaN: not a number
 - from type `Number`
 - NaN not equal anything even NaN (NaN==NaN => false)
 - NaN is a toxic value : NaN + 200 => NaN
 - to check NaN use `isNaN("String")`

<p align="right">(<a href="#top">back to top</a>)</p>

















