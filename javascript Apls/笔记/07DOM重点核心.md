# DOM重点核心

文档对象模型（Document Object Model，简称DOM）

他是W3C组织推荐的可处理扩展标记语言（HTML或者XML）的标准编程接口

W3C已经定义了一系列的DOM接口，可以通过这些接口改变网页的内容，结构和样式

1.对于JAVAScript,为了能使JavaScript操作HTML，javaacript就有了一套自己的dom编程接口 

2.对于HTML ， DOM使得HTML形成一颗DOM树，包含文档，元素节点

我们获取过来的DOM元素是一个对象（Object）,所以称为文档对象模型

![](C:\Users\Administrator\Desktop\WH\javascript Apls\typora-user-images\1611799149409.png)

关于Dom操作，主要针对元素的操，主要有创建，增，删，改，查，属性操作，事件操作

### 创建

1. document.write
2. innerHTML
3. createElement



### 增

1. appendChild
2. inserBefore



### 删

1. removeChild



### 改

   修改元素属性：DOM元素的内容，属性，表单的值等

1. 修改元素属性：src，href , title,
2. 修改普通元素内容：InnerHTML, innerText
3. 修改表单元素：value，type, disabledent等
4. 修改元素样式： style,className



### 查

主要获取查询DOM元素

1. DOM提供的API方法：getElementByid, getElementByTagName 古老用法，不太推荐
2. H5提供的方法： querySelector, querySelectorAll 提倡
3. 利用节点操作获取元素， 父（parentNode)   子（child)   兄（perviousElementSibling, nextElementSibling)提倡



### 属性操作

1. setAttribute : 设置DOM的属性值
2. getAttribute : 得到DOM的属性值
3. removeAttribute移除属性



### 事件操作

~~~~html
onclick:         鼠标点击左键触发
onmouseover:     鼠标经过出发
onmouseout:      鼠标离开触发
onfocus:         鼠标焦点触发
onblur:          失去鼠标焦点触发
onmousemove:     鼠标移动触发
onmouseup:       鼠标弹起触发
onmousedown      鼠标按下触发

~~~~





 