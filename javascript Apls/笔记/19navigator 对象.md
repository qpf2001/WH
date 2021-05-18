# navigator 对象

navigator 对象包含有关浏览器的信息，它有很多属性，我们最常用的是userAgent,该属性可以返回由客户机发送服务器的 user-agent 头部值。

实现代码效果如下：

~~~js
<script>
        if ((navigator.userAgent.match(/(phone|pad|pod|iPhone|iPod|ios|iPad|Android|Mobile|BlackBerry|IEMobile|MQQBrowser|JUC|Fennec|wOSBrowser|BrowserNG|WebOS|Symbian|Windows Phone)/i))) {
            window.location.href = ""; //手机
        }else {
            window.location.href = ""; //电脑
        }
    </script>
~~~

