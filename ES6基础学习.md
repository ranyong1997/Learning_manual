# ES6基础学习

## 什么是let命令

> 用来声明变量，只在let命令所在的代码块内有效

```javascript
{
    let a = 10;
    var b = 1;
}

a // a is not defined
b // 1
```

上面的代码块之中，分别用let和var声明了两个变量。然后在代码块之外调用这两个变量，结果let声明的变量报错，var声明的变量返回了正常的值。这表明let声明的变量只在它所在的代码块有效。

`for`循环的计数器，就很适合let命令。

```javascript
for(let i = 0;i<10;i++) {
    // ...
}
console.log(i);
// ReferenceError: i is not defined
```

上面代码中，计数器`i`只在`for`循环体内有效，在循环体外就会报错。

下面的代码如果使用var,最后输出的是10。

```javascript
var a = []
for (var i = 0;i<10;i++){
    a[i] = function(){
        console.log(i);
    };
}
a[6](); // 10
```

