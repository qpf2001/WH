# window对象常见事件

~~~js
 window.onload = function () {};
 window.addEventListener("load", function () {});
~~~

window.onload是窗口加载事件，当文档内容完全加载完成会触发该事件(包括图像，脚本文件，css文件等，) 就调用的处理函数 

### 注意：

1. 有了Window.onload就可以把js代码写在页面元素的上方，因为onload是等页面元素全部加载完毕，再去执行处理函数
2. window.onload，传统的注册事件方式只能写一次，如果有多个，会以最后一个window.onload为准
3. 如果使用addEventListener 则没有限制

#### 窗口加载事件

~~~js
 document.addEventListener("DOMContentLoaded", function () {}
~~~

DOMContentLoaded 事件触发时，仅当DOM加载完成，不包含样式表，图片，flash等，IE9以上才支持

如果页面元素非常多的话，从用户访问到onload触发可能需要较长的时间，交互效果就不能实现，必然影响用户的体验，此时用DOMContentLoaded 事件比较合适

#### 调整窗口大小事件

~~~js
 window.onresize = function () {};
 window.addEventListener("resize", function () {});
~~~

window.onresize 是调整窗口大小加载事件，当触发时就可以调用的处理函数

##### 注意：

+ 只要窗口大小发生像素变化，就会出发这个事件
+ 我们经常利用这个事件完成响应式布局，window,innerWidth 当前屏幕宽度