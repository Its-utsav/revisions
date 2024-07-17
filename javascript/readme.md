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
2.

## TOC

1. [string](#string)

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

   a. `String.prototype.length`
      1. return the string length , count the character in string
      2. code example
      ```js
      let str = "Hello";
      console.log(str.length); // 4
      ```
      ***
   b. `String.prototype.charAt(index)`
      3. return the character at specific index
      4. code example

   ```js
   let str = "Hello";
   console.log(str.charAt(1)); // e
   console.log(str.charAt()); // H
   ```

       - if index is `out of range` even for negative value than it return `' '` (empty string).
       - if we want the a `UTF-16` value from the index than we can use `String.prototype.charCodeAt(index)`

    ```js
    let a = "Hello World";
    console.log(a.charCodeAt()); // zero index 47
    console.log(a.charCodeAt(2)); // zero index 108
    ```
    - if we want to use negative values as index than we  can use `String.prototype.at(index)` 
    - negative values than it given index from last of the string 
    - -1 -> last character 
    - -2 -> second last character ..... so on 
   c. `String.prototype.concat(s1,s2,s3,sN)`
      1. Combines the multiple string into one string
      2. code eg

   ```js
   let str1 = "Hello";
   let str2 = "World";
   console.log(str1.concat(" ", str2)); // "Hello World"
   ```

   d. `String.prototype.includes(substr,position)`
      3. it return `true` or `false` whether the given substring found in string , we can optional give index position to start searching by default is `0`
      4. code

   ```js
   let str = "Hello World";
   console.log(str.includes("World")); // true
   ```

   e. `String.prototype.indexOf(searchString,fromIndex)`
      5. it return index of first occurrence of the give search string
      6.  if given search string not found than it return -1
      7.  code

   ```js
   let str = "Hello World";
   console.log(str.indexOf("World")); // 6
   ```

   - if we have need from last than we can use `String.prototype.lastIndexOf()`

   f. `String.prototype.slice(beginIndex, endIndex)`
      1. it cut and return the given as per begin and end index(not include)
      2. id do not modify the original string
      3. code

   ```js
   let str = "Hello World";
   let newStr = str.slice(2, 5); /// llo
   console.log(newStr);
   ```

   g. `String.prototype.substring(indexStart, indexEnd)`
      4. similar to `String.prototype.slice(beginIndex, endIndex)` , but include the end index
      5. code

   ```js
   let str = "Hello World";
   console.log(str.substring(0, 5)); // "Hello"
   ```

   h. `Case Change`
      6. `UpperCase` to `LowerCase` :- `'Hello Js'.toUpperCase()` -_output_-> `'HELLO JS'`
      7. `LowerCase` to `UpperCase` :- `'Hello Js'.toLowerCase()` -_output_-> `'hello js'`
   i. `String.prototype.trim()`
      8. Remove White Space from end and start of the sting
      9. code eg

   ```js
   let str = "  Hello World  ";
   console.log(str.trim()); // "Hello World"
   ```

   - we have more two option for removing white space from start `String.prototype.trimStart()` and removing space from end of the string `String.prototype.trimEnd()`

   j. `String.prototype.split(delimiter,limit)`
     1. split (broke) the string as per delimiter into substring of array we can optional specify the maxLimit of split
     2. code eg

   ```js
   let str = "Hello World";
   console.log(str.split(" ")); // ["Hello", "World"]
   ```

   - if delimiter is not found than return original string

   k. `String.prototype.replace(searchValue, newValue)`
     1. replace the _first_ occurrences `searchValue` with `newValue`
     2. code eg

   ```js
   let str = "Hello World";
   console.log(str.replace("World", "Everyone")); // "Hello Everyone"
   ```

   - if `searchValue` not found than it return original string
   - if we want to replace the all occurrence of the substring than we can use `String.prototype.replaceAll()`

   l. `String.prototype.startsWith(str,position)` and `String.prototype.endsWith(str,position)`
     1. it check the given sting is string or ending with specific substr or not
     2. return boolean values

   ```js
   let s = "Hello World";
   console.log(s.startsWith("H")); // true
   console.log(s.endsWith("D")); // false;
   ```

   m. 

3.
