# JavaScript

## Glossary

1. `Primitive`
   - It is a Grouped DataType (mean in this datatype hading we have multiple types).
   - `Primitive` Datatype means is a data which is not an `Object` and has no `methods` and `properties`.
   - Most are Immutable means can't changed at any specific index , but value can resign even `Object` , `Array`.
   - **NOTE** :- if you are beginner than no need to read below lines.
     - No `methods` but it can behave like they do . WHAT ???????????????
     - When we try to access `methods` or `properties` on `Primitive` values than `JS` automatically `Boxes` the `Primitive` values into temporary `Object` and that `Object` have those `methods` and `properties` .
     - It access the `methods` and `properties` on that wrapper `Object` , rather than on `Primitive` values itself.
     - As per this here all before the `methods` syntax automatically add  `Object.prototype`.[methodName] 
     - If Object is String than `String.prototype`.[methodName] 
2.

## TOC

1. [string](#string)
2. [Number](#numbers)
3. [Array](#array)

## todo's

- [ ] todo add some history

## Common Things

1. `Object.length` - it return the length of Object
2. `Object.type` - it return the type of Object

## string

- `String` represent the sequence of character
- available in almost most of the programming language
- `Primitive` value .

1. Creating The stings

- as string literals

```js
let str1 = "Hello JS";
let str2 = "Hello Js 2";
let str3 = `Hello Js 3`;
console.log(typeof str1, typeof str2, typeof str3); // string
```

- as Object _rarely_ used

```js
let strObj = new String("Hello String from String Object");
console.log(typeof strObj); // object
```
- we can access the string character using their index
```js
let str = 'Hello World';
console.log(str[0]); // H
```
String.prototype
1. Common Methods

   a. `length`
      1. return the string length , count the character in string
      2. code example
      ```js
      let str = "Hello";
      console.log(str.length); // 4
      ```
      ***
   b. `charAt(index)`
      3. return the character at specific index
      4. code example

   ```js
   let str = "Hello";
   console.log(str.charAt(1)); // e
   console.log(str.charAt()); // H
   ```

       - if index is `out of range` even for negative value than it return `' '` (empty string).
       - if we want the a `UTF-16` value from the index than we can use `charCodeAt(index)`

    ```js
    let a = "Hello World";
    console.log(a.charCodeAt()); // zero index 47
    console.log(a.charCodeAt(2)); // zero index 108
    ```
    - if we want to use negative values as index than we  can use `at(index)` 
    - negative values than it given index from last of the string 
    - -1 -> last character 
    - -2 -> second last character ..... so on 
   c. `concat(s1,s2,s3,sN)`
      1. Combines the multiple string into one string
      2. code eg

   ```js
   let str1 = "Hello";
   let str2 = "World";
   console.log(str1.concat(" ", str2)); // "Hello World"
   ```

   d. `includes(substr,position)`
      3. it return `true` or `false` whether the given substring found in string , we can optional give index position to start searching by default is `0`
      4. code

   ```js
   let str = "Hello World";
   console.log(str.includes("World")); // true
   ```

   e. `indexOf(searchString,fromIndex)`
      5. it return index of first occurrence of the give search string
      6.  if given search string not found than it return -1
      7.  code

   ```js
   let str = "Hello World";
   console.log(str.indexOf("World")); // 6
   ```

   - if we have need from last than we can use `lastIndexOf()`

   f. `slice(beginIndex, endIndex)`
      1. it cut and return the given as per begin and end index(not include)
      2. id do not modify the original string
      3. code

   ```js
   let str = "Hello World";
   let newStr = str.slice(2, 5); /// llo
   console.log(newStr);
   ```

   g. `substring(indexStart, indexEnd)`
      4. similar to `slice(beginIndex, endIndex)` , but include the end index
      5. code

   ```js
   let str = "Hello World";
   console.log(str.substring(0, 5)); // "Hello"
   ```

   h. `Case Change`
      6. `UpperCase` to `LowerCase` :- `'Hello Js'.toUpperCase()` -_output_-> `'HELLO JS'`
      7. `LowerCase` to `UpperCase` :- `'Hello Js'.toLowerCase()` -_output_-> `'hello js'`
   i. `trim()`
      8. Remove White Space from end and start of the sting
      9. code eg

   ```js
   let str = "  Hello World  ";
   console.log(str.trim()); // "Hello World"
   ```

   - we have more two option for removing white space from start `trimStart()` and removing space from end of the string `trimEnd()`

   j. `split(delimiter,limit)`
     1. split (broke) the string as per delimiter into substring of array we can optional specify the maxLimit of split
     2. code eg

   ```js
   let str = "Hello World";
   console.log(str.split(" ")); // ["Hello", "World"]
   ```

   - if delimiter is not found than return original string

   k. `replace(searchValue, newValue)`
     1. replace the _first_ occurrences `searchValue` with `newValue`
     2. code eg

   ```js
   let str = "Hello World";
   console.log(str.replace("World", "Everyone")); // "Hello Everyone"
   ```

   - if `searchValue` not found than it return original string
   - if we want to replace the all occurrence of the substring than we can use `replaceAll()`

   l. `startsWith(str,position)` and `endsWith(str,position)`
     1. it check the given sting is string or ending with specific substr or not
     2. return boolean values

   ```js
   let s = "Hello World";
   console.log(s.startsWith("H")); // true
   console.log(s.endsWith("D")); // false;
   ```

- string Operator :- `string1` + `string2` eg.:- `Hello ` + `World` = `Hello World`
- this is just a some overview of string `methods` and `properties`, for more info you can search on web , or [visit mdn](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)


## Numbers

- Number represent floating-point number like `100` or `3.14`
- `JS` dose not have any differences datatype for storing `int` or `float` datatype like `C` , `C++` programming language
- `JS` also have `BigInt` datatype for extremely large number , but it doesn't replace normal numbers

1. Declaring Number
 ```js
   let n = 100;
   let n1 = Number(100);
   let n2 = new Number(100); // as object
```
- converting into number
- ```js
   number -> number
   undefined -> NaN
   null ->  0
   true -> 1 and false -> 0
   strNumber -> number eg :- '1' -> 1 , '122' - > 122
   if fail to convert strNumber into the number than NaN eg:- 'Hello' - > NaN
   whitespace -> 0
   ```
- white space ignore
- `Infinity` and `-Infinity` both are number
2. Some Methods and properties
   a. `toFixed(digit)` 
      - format the number using fixed Point notions 
      - return type will `String`
      ```js
      let num = 123.456;
      console.log(num.toFixed(2)); // "123.46"
      console.log(num.toFixed('2')); // "123.46"
      console.log(num.toFixed('HI')); // "123"
      ``` 
   b. `toString(radix)` 
      - Convert(return) number into string as per  `radix` by default value is `10`    
      - `radix` must be between `2` to `36` other wise throw `RangeError`      
   ```js
   10.toString(2) -> 1010  
   10.toString(3) -> 101  
   10.toString(4) -> 22  
   10.toString(5) -> 20  
   10.toString(6) -> 14  
   10.toString(7) -> 13  
   10.toString(8) -> 12  
   10.toString(9) -> 11  
   10.toString(10) -> 10  
   10.toString(11) -> a  
   10.toString(12) -> a  
   10.toString(13) -> a  
   10.toString(14) -> a  
   10.toString(15) -> a  
   10.toString(16) -> a  
   10.toString(17) -> a  
   10.toString(18) -> a  
   10.toString(19) -> a  
   10.toString(20) -> a  
   10.toString(21) -> a  
   10.toString(22) -> a  
   10.toString(23) -> a  
   10.toString(24) -> a  
   10.toString(25) -> a  
   10.toString(26) -> a  
   10.toString(27) -> a  
   10.toString(28) -> a  
   10.toString(29) -> a  
   10.toString(30) -> a  
   10.toString(31) -> a  
   10.toString(32) -> a  
   10.toString(33) -> a  
   10.toString(34) -> a  
   10.toString(35) -> a  
   10.toString(36) -> a  
   ```
   c. `Number.parseInt(value)`  and `parseInt(value)` , `Number.parseFloat(value)`  and `parseFloat(value)`
      - both are same `parseInt == Number.parseInt` - > `true`
      - both are same `parseFloat == Number.parseFloat` - > `true`
      - `parseInt(value)` and `parseFloat(value)` are available at Global
   ```js
   console.log(parseInt(100.2)) // 100 
   console.log(Number.parseInt(100.2)) // 100


   console.log(Number.parseFloat('121.12')) // 121.12
   console.log(parseFloat('121.12')) // 121.12
   ``` 
   d. `isNaN(value)` , `isFinite(value)`
      - `isNaN(value)` return `true` if given value is `Not a Number` other wise `false`
      - `isFinite(value)` return `true` if given value is `Finite` other wise `false`

3. `Math` Object
- it only work with `Number` 
- we can not use with `new` keyword , that mean we don't need to invoke it , most global object 
- all `methods` and `properties` are statics 

The Math object in JavaScript provides mathematical constants and methods for performing mathematical operations. It's a static object, so you don't need to create an instance of it.
Constants

- `Math.PI`: Ratio of a circle's circumference to its diameter (≈3.14159)
- `Math.E`: Euler's number (≈2.71828)
- `Math.LN2`: Natural logarithm of 2 (≈0.69314)
- `Math.LN10`: Natural logarithm of 10 (≈2.30258)
- `Math.LOG2E`: Base 2 logarithm of E (≈1.44269)
- `Math.LOG10E`: Base 10 logarithm of E (≈0.43429)
- `Math.SQRT1_2`: Square root of 1/2 (≈0.70710)
- `Math.SQRT2`: Square root of 2 (≈1.41421)

Methods
Basic Operations

- `Math.abs(x)`: Returns the absolute value of x
- `Math.sign(x)`: Returns the sign of x (-1, 0, or 1)
- `Math.max(x, y, ...)`: Returns the largest of zero or more numbers
- `Math.min(x, y, ...)`: Returns the smallest of zero or more numbers

Rounding

- `Math.round(x)`: Rounds x to the nearest integer
- `Math.ceil(x)`: Rounds x up to the nearest integer
- `Math.floor(x)`: Rounds x down to the nearest integer
- `Math.trunc(x)`: Returns the integer part of x by removing fractional digits

Exponential and Logarithmic

- `Math.pow(base, exponent)`: Returns base raised to the power of exponent
- `Math.sqrt(x)`: Returns the square root of x
- `Math.cbrt(x)`: Returns the cube root of x
- `Math.exp(x)`: Returns E^x
- `Math.log(x)`: Returns the natural logarithm (base E) of x
- `Math.log10(x)`: Returns the base 10 logarithm of x
- `Math.log2(x)`: Returns the base 2 logarithm of x

Trigonometric

- `Math.sin(x)`: Returns the sine of x (x in radians)
- `Math.cos(x)`: Returns the cosine of x (x in radians)
- `Math.tan(x)`: Returns the tangent of x (x in radians)
- `Math.asin(x)`: Returns the arcsine of x
- `Math.acos(x)`: Returns the arccosine of x
- `Math.atan(x)`: Returns the arctangent of x
- `Math.atan2(y, x)`: Returns the arctangent of the quotient of its arguments

Other

- `Math.random()`: Returns a pseudo-random number between 0 and 1 , _MOST IMP_


## Array
- collection of element (DataType can be different )