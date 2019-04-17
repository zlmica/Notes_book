## 展开数组/对象
**... 符号**

...[1, 2, 3] 等价于 1, 2, 3

...{a: 1, b:2, c: 3} 等价于 a: 1, b: 2, c: 3

``` js
// 数组
let arr = [1, 2, 3];
let arr1 = ...arr;
console.log(arr1); // [1, 2, 3]
// 对象
let obj = {a: 1, b:2, c: 3};
let obj1 = ...obj;
console.log(obj1); // {a: 1, b:2, c: 3}
// 合并数组
let arr2 = [1, 2, 3];
let arr3 = [0, ...arr2]; // [0, 1, 2, 3]
let arr4 = [...arr2, ...arr3]; // [1, 2, 3, 0, 1, 2, 3]
// 对象也可以这样合并
```

## 剩余参数

``` js
function func(a, b, ...arg) {
      console.log(a, b, arg);
}
func(0, 1, 2, 3, 4); // 0, 1, [2, 3, 4]
```

***