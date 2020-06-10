## JavaScript Questions
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

https://ithelp.ithome.com.tw/articles/10197529
<br/><br/>

:white_check_mark: 3. Explain What Is The New Feature In ES6?

Arrow Function, Class, Promise, Block-Scoped Constructs Let and Const, Template Literals
<br/><br/>

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

<br/><br/>

7. Explan What Is Callbacks?

Take another function as another function's parameter, called by another function. 
<br/><br/>

8. Explan What Is Async/Await?

Related Reference : [簡單理解 JavaScript Async 和 Await](https://www.oxxostudio.tw/articles/201908/js-async-await.html
)
<br/><br/>

9. Explan What Is Hoisting?

Please see the related reference below, it's very clear.<br/>
You can use "let/const" instead of var to avoid hoisting, actually let/const has hoisting, but they have TDZ(Temporal Dead Zone).

Related Reference : [我知道你懂 hoisting，可是你了解到多深？](https://blog.techbridge.cc/2018/11/10/javascript-hoisting/)
<br/><br/>

10. Following The Previous Question, Explan What Is Let/Const?

Let and Const is block scope, Var is function scope,<br/>
Let is for variable,<br/>
Const is for const variable, can't reassignment.<br/>

Related Reference :  [let與const](https://ithelp.ithome.com.tw/articles/10185142)
<br/><br/>

11. Following The Previous Question, explan What Is TDZ?

Let/const has hoisting indeed, TDZ is if you try to access a variable after hoisting and before assigning value, browser will throw the error notification.
<br/><br/>

12. Explan What Is "this"?
<br/><br/>

13. Explan What Is Call By Value, Call By Reference And Call By Sharing?

**Call By Value** : 

<p align="center">
<img src="img/callByValue.png" alt="callByValue" title="callByValue" width="60%">
</p>

When you declare a primitive type (string, number, boolean, null, undefined, symbol) for example variable a , it will has own memory location and store it's own value in it, then assign another variable b equal to a, b also has own memory location and store a's value in it. b's value ```WILL NOT CHANGE``` when a's value changes, a and b's memory location is isolate, they won't interrupt each other.  

Example : https://jsfiddle.net/yschen25/9v0t2fx6/
<br/><br/>

**Call By Reference** : 

<p align="center">
<img src="img/callByReference.png" alt="callByReference" title="callByReference" width="60%">
</p>

When you declare variable a as an object or function, it will has own memory location and store it's own value in it, then assign b equal to a, b ```WILL NOT``` has an own memory location, a and b will has same memory location, b's value ```WILL CHANGE``` when a's value changes. 

Example : https://jsfiddle.net/yschen25/ov3rq5me
<br/><br/>

**Call By Sharing** : If there are an array1 equal to [1,2,3], assign array2 equal to array1, array1 = [1,2,3], then reassign array1 to [4,5,6], it ```WILL NOT``` change array2's value. But if assign arry1[0] = 4, it will change array2 to [4,2,3] (e.g., use array literals, object literals assign value again)

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

15. What Is The Difference between Null and Undifined?

Undefined means a variable has been declared but has not yet been assigned a value.<br/>
let a;<br/>
console.log(a);         // undefined<br/>
console.log(typeof a);  // undefined<br/>

Null is an assignment value. It can be assigned to a variable as a representation of no value.<br/>
let a = null;<br/>
console.log(a);         // null<br/>
console.log(typeof a);  // object<br/>

null == undefined   // true<br/>
null === undefined  // false
<br/><br/>

16. What Is Event Bubbling And How To Stop IT?

(1)The event first triggers on the innermost target element, and then triggers on the ancestors (parents) of the target element in the same nesting hierarchy till it reaches the outermost DOM element or document object.<br/>
(2)Using event.stopPropagation()
<br/><br/>

17. What Is IIFE(Immediately Invoked Function Expression)?
<br/><br/>

18. What Is Prototype?
<br/><br/>

19. What Is Event Loop?
<br/><br/>

20. What Is Functional Programming?
<br/><br/>

21. What Is Function Statements And Function Expressions?
