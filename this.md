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
function func() {
  console.log( this.a );
}

var obj = {
  a: 2,
  foo: func
};

obj.foo();  // 2

var func2 = obj.foo;
func2();    // undefined
```

```
var a = 3;
function func() {
  console.log( this.a );
}

var obj = {
  a: 2,
  foo: func
};

obj.foo();  // 2

var func2 = obj.foo;
func2();    // 3
```

```
function func() {
  console.log( this.a );
}

var obj = {
  a: 2,
  foo: func
};

obj.foo(); // 2

var func2 = obj.foo;

func2; // function func()
```

```
function func() {
  console.log( this.a );
}

var obj = {
  a: 2,
  foo: func
};

obj.foo(); // 2

var func2 = obj.foo(); 

func2; // 2
```


