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
