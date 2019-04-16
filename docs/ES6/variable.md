## var
*ES5中唯一的变量声明方式，存在的严重问题如下：*
1. 可以重复声明
``` js
var a = 1;
console.log(a); // 1
var a = 2;
console.log(a); // 2
```
2. 没有块级作用域概念

    *ps: "块" 指 语法块，即 {}*
``` js
if (true) {
      var b = 1;
      console.log(b); // 1
}
console.log(b); // 1
```
3. 没有常量概念，不能限制修改
``` js
var PI = 3.14;
PI = 3.15;
PI = 3.16; // 可以随意修改
```

## let
*ES6中用作声明变量*
- 变量禁止重复声明，解决上述问题1
``` js
let a = 1;
let a = 2; // 报错，Identifier 'a' has already been declared.
```
- 变量支持块级作用域，解决上述问题2
``` js
if (true) {
      let b = 1;
      console.log(b); // 1
}
console.log(b); // 报错，c is not defined.
```
## const
*ES6中用作声明常量*
- 常量不可被修改，解决上述问题3
``` js
const PI = 3.14;
PI = 3.15; // 报错, Assignment to constant variable.
```
ps: **const** 声明方式也存在块级作用域，同 **let** 一致。