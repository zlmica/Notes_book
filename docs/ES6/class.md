## 类的创建

``` js
class Person {
    constructor(){
    // 构造函数
    }

    sayHi() {
        console.log('Hi');
    }
}
let p = new Person();
p.sayHi(); // Hi
```

## 类的继承

``` js
// extends 关键字
class Woman extends Person {
      
}
// 如果子类没有定义constructor方法，这个方法会被默认添加，代码如下。也就是说，不管有没有显式定义，任何一个子类都有constructor方法
class Woman extends Person {
    constructor(){
        // 调用父类的 constructor
        super()
    }
}
let p = new Woman();
p.sayHi(); // Hi
```
ps: 这些关键字只是语法糖，书写统一方便

***