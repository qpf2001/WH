# BOM概述

BOM(Brower Object Model)即浏览器对象模型，它提供了独立于内容而与浏览器窗口进行交互的对象，其核心就是window.

BOM是由一些列的相关对象构成，并且每个对象都提供了很多的方法与属性

BOM缺乏标准，javascript的语法标准化组织是ECMA,  DOM的标准化组织是Wc3，BOM最初是Netscape浏览器标准的一部分。

#### DOM

+ 文档对象模型
+ DOM就是把文档当作一个对象来看
+ DOM的顶级对象就是document
+ DOM主要就是学习操作页面元素
+ DOM是W3C标准规范

#### BOM

+ 浏览器对象模型
+ 把浏览器当作一个对象来看
+ BOM的顶级对象就是window
+ BOM学习的是浏览器窗口交互的一些对象
+ BOM是浏览器厂商在各自浏览器上定义的，兼容性比较差

#### BOM的构成

window 是浏览器的顶级对象

1. 他是js访问浏览器的一个接口
2. 他是一个全局对象，定义在全局作用域中的变量，函数都会变成window对象的属性和方法

在点用的时候，可以省略window，前面学习的对话框都属于window对象方法，比如 alert(), prompt()

