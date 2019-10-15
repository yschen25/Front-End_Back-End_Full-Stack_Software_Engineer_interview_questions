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
<br/>

2. Explain What Is Promise?

<br/>

3. Explain What Is The Difference Between ES5 And ES6?

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

5. Explain What Is The Difference Between map(), forEach()?

| Methods | map() | foEach() |
|---|---|---|
| Return | Returns a new array | **DOES NOT** return a new array, returns undefined |
| | **DOES NOT** change the original array | |
| |The function is not executed for array elements without values.| The function is not executed for array elements without values. |

6. Explan What Is Callbacks?
<br/>

7. Explan What Is Async/Await?
<br/>

8. Explan What Is Hoisting?
<br/>

// let, const

Related Reference : [我知道你懂 hoisting，可是你了解到多深？](https://blog.techbridge.cc/2018/11/10/javascript-hoisting/)
<br/>

9. Explan What Is "this"?
<br/>

10. Explan What Is Call By Value, Call By Reference And Call By Sharing?

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

Example :
<br/>

Call By Sharing : 
// array literals, object literals

Related Reference : [談談 JavaScript 中 by reference 和 by value 的重要觀念](https://pjchender.blogspot.com/2016/03/javascriptby-referenceby-value.html)
[你不可不知的 JavaScript 二三事](https://ithelp.ithome.com.tw/articles/10209104)
<br/>
<br/>

11. Following The Previous Question, Explan What Is Shallow Copy And Deep Copy?

Related Reference : [關於 JS 中的淺拷貝和深拷貝](https://larry850806.github.io/2016/09/20/shallow-vs-deep-copy/)
<br/>
