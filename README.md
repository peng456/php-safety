# php-safety
php。安全问题。

累死了，面试了一天。

安全分很多方面。我们来一一聊聊

SQL注入
解决方案：
PDO 绑定参数
最根本： 避免数据变成代码被执行，


$stmt = $mysqli->prepare("DELETE FROM planet WHERE name = ?");
$stmt->bind_param('s', "earth");
$stmt->execute();

预编译
：预处理语句针对SQL注入是非常有用的，因为参数值发送后使用不同的协议，保证了数据的合法性。



XSS 与CSRF

跨站脚本攻击（Cross）
恶意攻击者，会在 向 web 页面中 插入恶意script代码。当用户浏览页面时，其中的恶意脚本会执行===》干坏事

分两种： 1、内部攻击： 程序自身漏洞，造成跨站语句。
        2、外部攻击： 

XSS可分为3种： 存储型（持久型）、反射型（非持久型）、基于DOM的

存储型： 脚本存储在服务器。当浏览器请求数据时,从服务器传回，并执行
        
反射型XSS： 

当用户点击一个 ### 恶意链接，或者提交一个  ### 表单，或者进入一个 ### 恶意网站时，注入脚本   进入   被攻击者的网站  。Web服务器将注入脚本，比如一个错误信息，搜索结果等 返回到用户的浏览器上。浏览器会执行这段脚本，因为，它认为这个响应来自可信任的服务器。

        基于DOM的XSS
被执行的恶意脚本会修改页面脚本结构。


输入过滤

Cookie 安全


禁用mysql_ 函数

数据库存储用户密码时，怎么做菜安全


验证session 问题

安全的Session 问题


目录权限安全

包含本地与远程文件

文件上传PHP脚本

evel 函数执行脚本

disable_functions  关闭 高位函数

FPM 独立用户与组，给每个目录特定权限

了解Hash 与 Encrypt 区别

Same-origin policy

Web应用程序安全 （http://phpsecurity.readthedocs.io/en/latest/index.html）

配置文件

注册全局文件

错误报告


线程安全 问题


多进程并发  问题（比如文件的读写）











