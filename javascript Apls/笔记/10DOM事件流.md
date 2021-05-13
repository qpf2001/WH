# DOM事件流

事件流描述的是从页面中接受的事件顺序

事件发生会在元素节点之间按照特定的顺序传播，这个过程称之为DOM事件流

比如给div一个点击事件：

DOM事件流分为三个阶段：

1.捕获阶段

2.当前目标阶段

2.冒泡阶段



+ 事件冒泡：IE最早提出来，事件开始由最具体的元素接受，然后主机逐级向上传播到DOM最顶层节点过程。
+ 事件捕获：网景最早提出来，由DOM最顶层开始，然后逐级向下传播到最具体的元素接受过程

![](C:\Users\Administrator\Desktop\WH\javascript Apls\typora-user-images\393e2d96b0e7bbddc002a7ebf951e5f.jpg)

注意：

1. js代码中只能执行捕获冒泡其中的一个阶段

2. onclick 和 attachEvent 只能得到冒泡阶段

3. 捕获阶段，如果addEventListener是false，那么处于捕获阶段，他们的顺序， document > html > body > dad > son

4. 实际开发中，很少使用事件捕获，更关注事件冒泡

5. 有些事情是没有冒泡的，比如　onblur, onfocus, onmouseenter, onmouseleave

   