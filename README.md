# go-dev-tools
个人使用Golang进行后端开发时封装的一些工具对象

**这里封装都是写工具的初级原型, 具体融合到项目中时可能需要做一些修改**

**懒得封装到兼容性很高, 我个人认为纯粹调包开发非常无聊而且包内有些功能也用不上, 抽空自己造一造轮子其实挺有意思的**

----
- ### middlewares.CacheMiddleware
  + 缓存中间件, 提供加载, 存储, 清理缓存的功能函数, 具体函数功能请看注释(PS: 所有代码的注释都是英文写的, 懒得在写代码的时候切换输入法😂)

- ### middlewares.CORSMiddleware
  + 跨域中间件, 解决前后端分离项目的跨域问题, 本质上修改响应头, 添加跨域相关的控制Headers信息

- ### middlewares.FlowLimitMiddleware
  + 限流中间件, 利用标准库中的Token Bucket算法函数, 控制单位时间内处理的请求数量, 实现限流效果


----
- ### utils.GinStyleLogger
  + 日志输出对象, 帮助我们输出格式和Gin框架默认日志格式一样的日志信息(PS: 个人认为在不考虑使用日志信息做数据分析的情况下, Gin框架本身的日志格式挺好看的, zap或者logrus都很好用! 就是配置起来参数太多了)

- ### utils.rotateFileWriter
  + 循环文件写入器, 可以帮助我们自己实现循环文件日志
  
- ### utils.stringTools
  + 字符串和Byte数组常用的一些操作的函数, 详情看代码和注释
  
- ### utils.timeTools
  + 日期, 时间, 时间戳常用的一些操作函数, 详情看代码和注释
