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
the type of any variable using `typeof(variable-name);` or `typeof variable-name; ` and it returns small letter, and you
can use another property, and it is better `variable-name.constructor.name` will return the original type no matter 
the creation was either literal or construction. 
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
 - to check NaN use `isNaN("String")`<br>

division on zero in javaScript will not throw exception
    * number / zero  => infinity <br>
    * number / -zero => - infinity <br>
    * infinity / infinity => NaN <br>

<p align="right">(<a href="#top">back to top</a>)</p>

### Casting: Convert type to another type
##explicit cast (Number, + operator)
1. Number , + have the same algorithm <br>
   *Trim for input String
      - check String length = 0 > return 0
      - if all characters inside string is digits or not
         - return `number`
         - else return `NaN` <br>
YOU CAN REPLACE ALL `Number` WITH `+` AND GET `SAME RESULT`
Number(new Data()); => return `number in milliseconds` 
Number(false);     => `0`
Number(true);      => `1`
Number(null)       => `0`
Number(undefined)  => `undefined`
Number(" \n\t")    => `0`
```sh
   Number("    ");    // output will be 0
   Number("  123");   // output will be 123
   Number(" 123ABC"); // output will be NaN
   ```
## implicit cast : coercion 
- `+ operator` is used convert second operand to String,used for concatenation
- All other operators are casting string to number

## Equality check VS Strict check
 - Equality check `==` only check the content regardless the type of the operands
 - Strict check `===` check if `two operands` from the `same type` 
   - if false => return false 
   - if true => evaluate value of operands 
 ## Scopes 
   1. global scope
   ```sh
   var test = 10; //global scope
    testTwo = 20; // global scope variable without keyword var must be initlized 
   ```
   2. local scope Also call function scope 
  ```sh
   function myFunc(){
     var test = 10;  //variable is in local scope cant be accessed outside the function
     takeCare = 911; // this variable is Accessible as global variable after the function calling occurence   
   } 
   myFunc();   
   ```
`takeCare` is Accessible as `global variable` After the function call occurrence 

## Object from String:
length property is read only 
methods: 
1. manipulate String
   - charAt(index)
```sh
   myString = "ITI Alexandria Branch"
   myString.charAt(0);                  // return 'I'
   myString.charAt(myString.length);    // return ' ' empty string
```
   - indexOf("ch,word,number",number-of-start-from-index)
```sh
myString.indexOf("A");  // 4
myString.indexOf("@");  // -1 doesnt exist 
myString.subString(myString.indexOf(Alex)); // return  'Alexandria Branch' 
```
   - lastIndexOf()
```sh
myString.lastIndexOf("h"); // 20 
```
   - subString(start,end?)
```sh
subString(0,3);  => return string from index 0 to index 2 
subString(0);    => return end String.Length
subString(5,1);  => swap two values (1,5)
subString(-1);   => start from index 0
subString(5,-1); => subString(-1,5) => subString(0,5) 
```
   - slice(start,end?)
```sh
myStr.slice(-6);  // return 'Branch'
myStr.slice(0,3); // return 'ITI'
```
   - substr(start-position,length)
```sh
substr(0,3); //return 'ITI'
```
   - split("splitter) 
```sh
split("") => return Array
"1,2,3,4,5".split(","); => return ["1","2","3","4","5"]
```
   - replace("","") OR replace(regex,value)
```sh
myString.replace("A","@"); // return "ITI @lexandria Branch" CHANGE ONLY FIRST OCCURENCE
myString.replace(/n/g,"s");
```
2. format string
   - .toUpperCase()
   - .toLowerCase()
   - .bold()
```sh
myString.bold().italics();   // method chaining is allowed in JS 
```




# Arrays In JavaScript 
In javascript: an Array is a Collection of Arranged Data
    * array object `doent have` to be `fixed size` .
    * Data `doenst have` to be `homogenous`.

## declare array object
1. Literal creation 
```sh
var myArr=[];           // Create for array object with length=0
var myArr=[1,2,3,4]     // Create an array object from type array with length 4 started from index 0 to index 3
```
2. Constructor creation
```sh
var myArr = new Array();        // Create for array object with length=0 
var myArr = new Array(5);       // Create an array obj from type array length=5, data initalized by `Undefined`
var myArr = new Array[1,2,3,4]; // Create an array obj from type array length=4, data initalizedby `passed_Data` 
```
###### `Dense Array` means that the `indexes` is `Numeric`. <br>
###### `Associative Array` **special type** of object `arr["ID"]=10;` means that keys are `Strings`. **not recommended** <br>


Using `Indexer` you can `set`, `get`, `add`,and `delete` data 

```sh
myArr[0]=100;    // set data
myArr[1];        // get data
myArr[5]=100;    // add data  will add holes with `undefined` value until it reach the index you wanted NOT RECOMMENDED
delete myArr[2]  // replace value of index 2 with `undefined` NOT RECOMMENDED
```
## Methods available with array object
* properties: 
    - .length: `Dense array` : keys are numbers. <br>
* Methods:
1. For `Adding` new items ( append , prepend , insert ) <br>
    * `push`,`unshift`,`splice` >> update original array
```sh
var myArr = [10,20,30,40,50,60];
myArr.push(70);   // add in last position  
myArr.unshift(5);  //add at index zero      
```
myArr.splice(target-index,0,value which will be added)    => 0: indicate : insertion
myArr.splice(target-index,2,value which will be removed)  => 2: means delete 2 items starting with target-index
```sh
myArray.splice(1,0,5);       //  adding [10,5,20,30,40,50,60]
myArray.splice(1,2,100,100); // reomving [10,100,100,40,50,60]
```

2. For looping :forEach
    * `forEch` is a function you `have to call` using `Array Object`<br>
```sh
myArr.filter(function(val){return val % 2 == 0; })
     .forEach(function(el.i){console.log(i +" : "+el);});
```
3. For `removing` (from end, from start, in between)
      * `pop`,`shift`,`splice` >> update original array
```sh
myArr.pop(70);   // remove from last position  
myArr.shift(5);  //remove at index zero 
```
4. Manipulation:
   * Filter<br>
     * by default `filter()` is `looping`
     * always return array object, You can take it and save it in another variable
```sh
var myArr = [1,2,3,4,5,6];
var result = myArr.filter(function(val){return val % 2 == 0;});
```
   * Sort >> update original array <br>
     - `default soring` is based on `ASSCII table` for `Strings`
     - To sort numbers you need to pass a function to help to sort 
     `- anonymous function: function without name: call backs :
        pass function to another function as a parameter`
```sh
var arr =[500,15,100,2,-20]; // not sorted
arr.sort(function(x,y){return x-y;});
```
   * reverse()
```sh
var arr =[500,15,100,2,-20]; // not sorted
arr.sort(function(x,y){return x-y;}).reverse();  // sorted and reversed
```
   * Map
     * return new version of the array without modifying the original array
```sh
var names =["Abdullah","Ahmed","Mahmoud","Hegab"];
var result = names.map(function(val){return val + "@mcit.gov.eg";})
the output will be ["Abdullah@mcit.gov.eg","Ahmed@mcit.gov.eg","Mahmoud@mcit.gov.eg","Hegab@mcit.gov.eg"];
```
   * slice(start,?end)
     * return array without any update in original array
```sh
var myArr = [10,20,30,40,50];
var result = myArr.slice(1,4);
```
   * reduce , reduceRight
     * one value from array values
     * myArr.reduce(function(prev,next){return p +=n;},initialize)
   ```sh
var myArr = [1,2,3,4,5,6,7]; 
myArr.reduce(function(prev,next){return p +=n;});      //28
myArr.reduce(function(prev,next){return p +=n;},100); //128
```
   * Some
     * return > boolean (True,False)
     * at least one element match condition
```sh
var myArr = [100,3,20,4];
var test = myArr.some(function(v){return v % 2 == 0;});
```
   * Every
     * return > boolean (True,False)
     * all elements match condition
```sh
var test = myArr.every(function(v){return v % 2 == 0;});
```
   * concat
```sh
var arrOne = [1,2,3,4];
var arrTwo = [10,20,30,40,50];
var arrThree = arrOne.concat(arrTwo);
```
   * join (separator)
```sh
var arrOne = [1,2,3,4];
arrOne.join("@"); [1@2@3@4];
arrOne.eval(join("+"));  // evel NOT RECOMMENDED
```

# Date , Boolean , Math










### NOTES 
if you want to loop over associative arrays use `for in`

for(var i in Object_name){
    console.log(i);  // this means the keys
    console.log(i+ ":" + person[i]);  // this means the keys
}

* Filter call back function >> (element value,index,traversed object)











### BOM ,and DOM

### Events:


































