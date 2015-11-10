# nodejsDemo

## Introduction

  学习[Node入门](http://www.nodebeginner.org/index-zh-cn.html)照着写的示例

## 理解记录

  1. **index.js**
    * 提供程序主入口，类似于main()
    * 提供路由字典

    ```
    var handle = {}
    ```

  2. **server.js**
    * 提供http服务器运行代码
      1. request,使用router来选择对应的功能模块进行处理
      2. response,向下传递
  3. **router.js**
    * 提供路由功能
      1. 找不到模块(404)
      2. 找到了，将request与response继续向下传递
  4. **requestHandlers.js**
    * 各个功能模块实现
      1. 解析request，(这步应该可以单独拿出来)
      2. 将结果通过response发回，error提示
