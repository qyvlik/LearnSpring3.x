# chapter2

1. 查看看效果

> 运行之前请先执行 `chapter2.sql` 构建数据库。默认数据库名为 `test`，用户名为 `root`，密码为 `root`。在 `applicationContext.xml` 中修改。

> 默认是 MySQL 5

http://localhost:8080/chapter2/index.html

2. 例子讲解

当浏览器打开 `http://localhost:8080/chapter2/index.html` 时，由 `@Controller` 注解的类 `LoginController` 截获这个动作，发送 `login`。

在 `baobaotao-servlet.xml` 中。设置了字符串或者 `ModelAndView` 到 `jsp` 的映射。

发送的 `login` 对应到  `login.jsp`。

在 `login.jsp` 发送表单到 `loginCheck.html` 由 `@Controller` 注解的类 `LoginController`截获这个类。由 `ModelAndView loginCheck(HttpServletRequest request, LoginCommand loginCommand)` 方法处理。

再返回一个 `ModelAndView` ，再由 `baobaotao-servlet.xml` 指定的 `jsp` 进行响应。
