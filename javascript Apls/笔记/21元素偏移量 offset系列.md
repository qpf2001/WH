# 21元素偏移量 offset系列

#### offset概述

offset翻译过来就是偏移量，我们使用offset系列相关属性，可以动态得到该属性的位置（偏移），大小等。

+ 获得元素距离带有定位父元素的位置
+ 获得元素自身大小（宽度高度）
+ 注意：这里返回值不带单位

offset系列常见属性：

~~~
element.offsetParent : 返回该元素带有定位的父级元素，如果父级元素没有定位，则返回body
element.offsetTop    : 返回元素相对带有定位父元素上方的偏移
element.offsetLeft   : 返回元素相对带有定位父元素左边框的偏移
element.offsetWidth  : 返回自身包括padding,边框，内容区的宽度，返回数值不带单位
element.offsetHeight : 返回自身包括padding,边框，内容区的高度，返回数值不带单位
~~~

#### offset 与 style 的区别

##### offset

+ offset可以得到任意样式表中的样式值
+ offset系列获得的数值是没有单位的
+ offsetWidth包含padding + border + width
+ offsetWidth 等属性是只读属性，只获取，不能赋值
+ 所以要想获取元素大小位置，用offset合适

##### style

+ style行内样式表中的样式值，
+ style.width获得的是带有单位的字符串
+ style.width获得不包含padding和border的值
+ style.width是可读写属性，可以获取也可以赋值
+ 所以，我们要想给元素更改值，则需要用style改变

#### e.page

e.pagex  鼠标在页面上x轴的位置

e.pageY 鼠标在页面上y轴的位置