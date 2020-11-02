1. 請問 this 將會出現什麼答案？
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

