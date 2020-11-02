#### Let and Var
```
function x() {

    if (true) {
        var a = 1;
        let b = 2;
    }
    console.log(a);
    console.log(b);
}
x();
```
Ans : 1 / b is not defined

<br/>

```
function x() {

    if (true) {
        console.log(a);
        console.log(b);
        var a = 1;
        let b = 2;
    }

}
x();
```
Ans : undefined / b is not defined

<br/>

#### Hoisting
```
(function () {
    try {
        throw new Error();
    } catch (x) {
        var x = 1, y = 2;
        console.log(x);
    }
    console.log(x);
    console.log(y);
})();
```
Ans : 1 / undefined / 2

<br/>

```
(function() {
	console.log(typeof displayFunc);
	var displayFunc = function(){
		console.log("Hi I am inside displayFunc");
	}
}());
```
??? Ans : undefined

<br/>

```
var employeeId = 'abc123';

function foo() {
	employeeId = '123bcd';
	return;

	function employeeId() {}
}
foo();
console.log(employeeId);
```
??? Ans : 'abc123'

<br/>


#### IIFE 
```
(function(){
  var a = b = 3;
})();

console.log(a);
console.log(b);
```
Ans : a is not defined / 3

<br/>

```
(function(){
  'use strict';
  var a = b = 3;
})();

console.log(a);
console.log(b);
```
Ans : a is not defined / b is not defined

<br/>

```
(function(){
  'use strict';
  var a = window.b = 3;
})();

console.log(a);
console.log(b);
```
Ans : a is not defined / 3

<br/>

#### This
```
function callName() {
  console.log(this.name);
}

var auntie = {
  name: '漂亮阿姨',
  callName: callName,
  watch: {
    name: 'Magic Watch',
    callName: callName,
  },
};

var callName1 = auntie;
var callName2 = auntie.watch;
var callName3 = callName1.callName();
var callName4 = callName2.callName;

callName3;
callName4;
```
Ans：漂亮阿姨 / function callName()

<br/>

```
function callName() {
  console.log(this.name);
}

var auntie = {
  name: '漂亮阿姨',
  callName: callName,
  watch: {
    name: 'Magic Watch',
    callName: callName,
  },
};

var callName1 = auntie;
var callName2 = auntie.watch;
var callName3 = callName1.callName();
var callName4 = callName2.callName();

callName3;
callName4;
```
Ans：漂亮阿姨 / Magic Watch

<br/>

```
var name = "KAKA";
function callName() {
  console.log(this.name);
}

var auntie = {
  name: '漂亮阿姨',
  callName: callName,
  watch: {
    name: 'Magic Watch',
    callName: callName,
  },
};

var callName1 = auntie.callName;

callName1();
```
Ans：undefined

<br/>

```
var name = "KAKA";
function callName() {
  console.log(this.name);
}

var auntie = {
  name: '漂亮阿姨',
  callName: callName,
  watch: {
    name: 'Magic Watch',
    callName: callName,
  },
};

var callName1 = auntie.callName;

callName1();
```
Ans：KAKA <br/>
auntie.callName 賦值給變數 callName1 時，callName 並沒有被呼叫，也就是函式只是另一個函式的參考。因此 callName1() 就只是一般的函式呼叫。

<br/>

```
var name = "KAKA";
function callName() {
  console.log(this.name);
}

var auntie = {
  name: '漂亮阿姨',
  callName: callName,
  watch: {
    name: 'Magic Watch',
    callName: callName,
  },
};

var callName1 = auntie.callName;

callName1;
```
Ans：function callName()

<br/>

```
var name = "KAKA";
function callName() {
  console.log(this.name);
}

var auntie = {
  name: '漂亮阿姨',
  callName: callName,
  watch: {
    name: 'Magic Watch',
    callName: callName,
  },
};

var callName1 = auntie.callName();

callName1;
```
Ans：漂亮阿姨

<br/>

```
function callName(name) {
  console.log(this.name, name);
}

var name = '全域阿姨';
var auntie = {
  name: '漂亮阿姨',
};

cllName(undefined, '小明');
callName.call(auntie, '小明');
```
Ans： 全域阿婆 / undefined，漂亮阿姨 / 小明

<br/>

```
var length = 10;
function fn() {
	console.log(this.length);
}

var obj = {
  length: 5,
  method: function(fn) {
    fn();
    arguments[0]();
  }
};

obj.method(fn, 1);
```
Ans： 10 / 2

<br/>

##### Call by value or reference
```
var arr1 = "john".split('');
var arr2 = arr1.reverse();
var arr3 = "jones".split('');
arr2.push(arr3);
console.log("array 1: length=" + arr1.length + " last=" + arr1.slice(-1));
console.log("array 2: length=" + arr2.length + " last=" + arr2.slice(-1));
```
Ans：array 1: length=5 last=j,o,n,e,s / array 2: length=5 last=j,o,n,e,s"

<br/>

```
var objA = {prop1: 42};
var objB = objA;
objB = {};
console.log(objA)
```
Ans：{prop1: 42}

<br/>

```
var a = {};
var b = a;
var c = b = { number: 1 };
c.name = '小明';
console.log(a);
```
Ans：{}

<br/>

```
var arrA = [0,1,2,3,4,5];
var arrB = arrA.slice();
arrB[0]=42;
console.log(arrA)
```
Ans：[0,1,2,3,4,5]

<br/>

```
var arrA = [{prop1: "value of array A!!"}, {someProp: "also value of array A!"},3,4,5];
var arrB = arrA.slice();
arrB[0].prop1=42;
arrB[3] = 20;
console.log(arrA);
```
Ans：[{prop1: 42}, {someProp: "also value of array A!"}, 3,4,5]

<br/>

#### Write a sum method which will work properly when invoked using either syntax below.
```
console.log(sum(2,3));   // Outputs 5
console.log(sum(2)(3));  // Outputs 5
```

Ans :
```
function sum(x, y) {
  if (y !== undefined) {
    return x + y;
  } else {
    return function(y) { return x + y; };
  }
}
```

<br/>

#### Others
```
function a(a) {
  a();
}

function b(b) {
  b();
}

function c(c) {
  console.log('casper');
}

a(b(c));
```
??? Ans：casper / a is not a function

Related Reference : [37 Essential JavaScript Interview Questions](https://www.toptal.com/javascript/interview-questions), [JavaScript 熱門面試題](https://hackmd.io/@chupai/r1mW5_gEB), [
123-Essential-JavaScript-Interview-Questions](https://github.com/ganqqwerty/123-Essential-JavaScript-Interview-Questions)

