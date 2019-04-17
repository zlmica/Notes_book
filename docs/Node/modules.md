## http 

``` js
// 引入 http 模块
const http = require('http');
// 创建一个服务
let server = http.createServer((req, res) => {
    res.write('Hello World');
    res.end();
})
// 监听 3000 端口
server.listen(3000);
```

## fs

通常我们会用异步读写

``` js

```