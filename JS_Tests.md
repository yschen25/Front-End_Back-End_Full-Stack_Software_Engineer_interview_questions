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

#### IIFE 
```
(function(){
  var a = b = 3;
})();

console.log(a);
console.log(b);
```
Ans : a is not defined / 3

```
(function(){
  'use strict';
  var a = b = 3;
})();

console.log(a);
console.log(b);
```
Ans : a is not defined / b is not defined

```
(function(){
  'use strict';
  var a = window.b = 3;
})();

console.log(a);
console.log(b);
```
Ans : a is not defined / 3

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



==
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


