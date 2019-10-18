## JavaScript Interview Questions

      This document is provided to who wants to prepare front-end interview
      so it doesn't explain the concepts deeply, if you need more details please google it. 
<br/>

1. Explan What Is Closure?

> - Closure gives an ability let inner function gain access to a variable declared in some other function scope, 
we can have private variable through closure w/o environment interference, A function returns another function. <br/>
> - [Without Use Closure](https://jsfiddle.net/yschen25/aofkj153/14/). <br/>
> - [Use Closure](https://jsfiddle.net/yschen25/pvqbxjr7). <br/>
> - More improvement [Use Anonymous And Arrow Function](https://jsfiddle.net/yschen25/rjefc2sg/). <br/>
> - Even use the same function, variables don't disturb each other cuz the excute environment is different [Use The Same Function](https://jsfiddle.net/yschen25/q5ohxarL/). <br/>

Related Reference : [深入淺出瞭解 JavaScript 閉包（closure）](https://pjchender.blogspot.com/2017/05/javascript-closure.html)
<br/><br/>

2. Explain What Is Promise?

<br/><br/>

3. Explain What Is The New Feature In ES6?

Arrow Function, Class, Promise, Block-Scoped Constructs Let and Const, Template Literals
<br/>

4. Explain What Is The Difference Between push(), pop(), unshift(), shift()?

| Methods | push() | pop() | unshift() | shift() | 
|---|---|---|---|---|
|  | **ADD** the element in the **END** of array | **DELETE** the element in the **END** of array | **ADD** the element in the **BEGINNING** of array | **DELETE** the element in the **BEGINNING** of array |
| Return | New length | The removed item | New length | The removed item |

Example : https://jsfiddle.net/yschen25/bcuto13q/
<br/><br/>

5. Explain What Is The Difference Between slice(), splice()?

| Methods |  slice(start index, end index ) | splice(index, howmany, item1, ....., itemX) 
|---|---|---|
|  | (optional, optional) | (required, optional, optional)|
|  | (If use negative numbers it will select from the end of an array, it acts like "0" if omitted ; Whole array will be selected if omitted, use negative numbers will select from the end of an array) | (Specifies at what position to add/remove items, use negative values to specify the position from the end of the array ; The number of items to be removed; The new item(s) to be added to the array) |
| | Starting at the given start argument, and ends at, but does not include | The end doesn't include |
| | **NOT** changes the original array | **CHANGES** the original array |

Example : https://jsfiddle.net/yschen25/vxmp7z3t/
<br/><br/>

6. Explain What Is The Difference Between map(), forEach()?

| Methods | map() | foEach() |
|---|---|---|
| Return | Returns a new array | **DOES NOT** return a new array, returns undefined |
| | **DOES NOT** change the original array | |
| |The function is not executed for array elements without values.| The function is not executed for array elements without values. |

7. Explan What Is Callbacks?
<br/><br/>

8. Explan What Is Async/Await?
<br/><br/>

9. Explan What Is Hoisting?

Please see the related reference below, it's very clear.<br/>
You can use "let/const" instead of var to avoid hoisting, actually let/const has hoisting, but they have TDZ(Temporal Dead Zone).

Related Reference : [我知道你懂 hoisting，可是你了解到多深？](https://blog.techbridge.cc/2018/11/10/javascript-hoisting/)
<br/><br/>

10. Following The Previous Question, explan What Is Let/Const?
<br/><br/>

11. Following The Previous Question, explan What Is TDZ?
<br/><br/>

12. Explan What Is "this"?
<br/><br/>

13. Explan What Is Call By Value, Call By Reference And Call By Sharing?

Call By Value : 

<p align="center">
<img src="img/callByValue.png" alt="callByValue" title="callByValue" width="60%">
</p>

When you declare a primitive type (string, number, boolean, null, undefined, symbol) for example variable a , it will has own memory location and store it's own value in it, then assign another variable b equal to a, b also has own memory location and store a's value in it. b's value ```WILL NOT CHANGE``` when a's value changes, a and b's memory location is isolate, they won't interrupt each other.  

Example : https://jsfiddle.net/yschen25/9v0t2fx6/
<br/><br/>

Call By Reference : 

<p align="center">
<img src="img/callByReference.png" alt="callByReference" title="callByReference" width="60%">
</p>

When you declare variable a as an object or function, it will has own memory location and store it's own value in it, then assign b equal to a, b ```WILL NOT``` has an own memory location, a and b will has same memory location, b's value ```WILL CHANGE``` when a's value changes. 

Example : https://jsfiddle.net/yschen25/ov3rq5me
<br/><br/>

Call By Sharing : If assign value again it will Only change own value. (e.g., use array literals, object literals assign value again)

Example : https://jsfiddle.net/yschen25/7djyawve
<br/>

Related Reference : [談談 JavaScript 中 by reference 和 by value 的重要觀念](https://pjchender.blogspot.com/2016/03/javascriptby-referenceby-value.html), 
[你不可不知的 JavaScript 二三事](https://ithelp.ithome.com.tw/articles/10209104)
<br/><br/>

14. Following The Previous Question, Explan What Is Shallow Copy And Deep Copy?
 
<p align="center">
<img src="img/shallow_deep_copy.png" alt="shallow_deep_copy" title="shallow_deep_copy">
<img src="img/shallow_deep_copy2.png" alt="shallow_deep_copy" title="shallow_deep_copy">
</p>

Shallow Copy : Duplicates as little as possible. If b is a shallow copy of a, b points to a's location in memory, b ```WILL CHANGE``` it's value when change a. 
Metgod => Spread Operator, object.assign

Deep Copy : Duplicates everything. If b is a deep copy of a, a and b has it's own memory location, b ```WILL NOT CHANGE``` it's value when change a. 
Metgod => JSON.parse(JSON.stringify(object)), jQuery's $.extend, lodash's _.cloneDeep

Related Reference : [關於 JS 中的淺拷貝和深拷貝](https://larry850806.github.io/2016/09/20/shallow-vs-deep-copy/),  [JS-淺拷貝(Shallow Copy) VS 深拷貝(Deep Copy)](https://kanboo.github.io/2018/01/27/JS-ShallowCopy-DeepCopy/)
<br/><br/>
