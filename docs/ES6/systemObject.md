## 数组

### map （映射）
*eg:*
``` js
// 判断数组元素是否大于 0
let arr = [-1, 2, -3, 0, 4];
let res = arr.map((item, index) => item > 0);
console.log(res); // [false, true, false, false, true]
```
### forEach （遍历）
*eg:*
``` js
// 数组循环，跟for循环一样
let arr = [0, 1, 2, 3];
arr.forEach((item, index) => {
    console.log(index, item);
    /*
    0 0
    1 1
    2 2
    3 3
    */
})
```
### filter （过滤）
*eg:*
``` js
// 过滤取偶数
let arr = [0, 1, 2, 3, 4];
let res = arr.filter((item, index) => item % 2 == 0);
console.log(res); // [0, 2, 4]
```
### reduce （返回一个值）
*eg:*
``` js
// 求和
let arr = [0, 1, 2, 3, 4];
let res = arr.reduce((tmp, item, index) => tmp + item);
console.log(res); // 10
```

## 字符串

### 模版字符串
*eg:*
``` js
// ` 反单引号
let str = 'zl';
let age = 18;
console.log(`我叫：${str}，今年：${age}岁了。`); // 我叫zl，今年18岁了。
```
### startsWith
*eg:*
``` js
// 判断是否为一个网址
let str = 'https://www.google.com';
let isUrl = str.startsWith('https://');
console.log(`str为一个网址：${isUrl}`); // str为一个网址：true
```
### endsWith
*eg:*
``` js
// 判断是否为一个疑问句
let str = '吃了吗？';
let isQuestions = str.endsWith('？');
console.log(`str为一个疑问句：${isQuestions}`); // str为一个疑问句：true
```
## JSON标准化
ps: **json**作为传输必须遵循标准写法， **key** 值必须是双引号

*eg:*
``` js
let obj = {a: 1, b: 2};
// 对象转json
let json = JSON.stringify(obj);
console.log(json); // {"a":1,"b":2}
// json转对象
let obj1 = JSON.parse(json); // {a: 1, b: 2}
```

***