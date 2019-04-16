## Promise
*eg:*
``` js
let a = 1;
// 创建一个 Promise 对象
// 每个 Promise 定义都是一样的，在构造函数里传入一个匿名函数，参数是 resolve 和 reject，分别代表成功和失败时候的处理。
let p = new Promise((resolve, reject) => {
    if (a > 0) {
        resolve('success');
    } else {
        reject();
    }    
})
// 调用
p.then((success) => {
    console.log(success); // success
}, (err)=>{
    console.log(err);
})
// 第二种写法
p.then((success) => {
    console.log(success); // success
}).catch((err) => {
    console.log(err);
})
// 它的主要交互方式是通过 then 函数，如果 Promise 成功执行 resolve 了，那么它就会将 resolve 的值传给最近的 then 函数，作为它的 then 函数的参数。

let p1 = new Promise((resolve, reject) => {
    if (a < 0) {
        resolve('success');
    } else {
        reject('faild');
    }    
})
p1.then((success) => {
    console.log(success);
}).catch((err) => {
    console.log(err); // faild
})
// 如果出错 reject，那就走 catch 来捕获异常。

// all 可以封装处理多个异步
Promise.all([p, p1, p2]).then((data) => {
    // 所有成功走这里
    // data 是一个数组，元素分别为三个异步方法成功的结果
}).catch((err) => {
    // 三个中只要有个出错，就会走这里
})
```
## async/await
*此为ES7的内容*

*eg:*
``` js
async function func() {
    let data1 = await $ajax({url: url1});
    let data2 = await $ajax({url: url2, data: data1});
    let data3 = await $ajax({url: url3, data: data2});
    console.log(data1, data2, data3); 
    // 此处代码不能直接运行，只做举例演示，表示可以直接获取到三个变量的值
    // ps: 这里只是个语法糖，写法方便，看着像同步，其实还是异步处理
}
```
***
