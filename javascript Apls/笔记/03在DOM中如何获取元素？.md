



# 03在DOM中如何获取元素？

+ 根据ID获取
+ 根据标签名获取
+ 通过HTML5新增的方法获取
+ 特殊元素获取



## 根据ID获取

~~~html
<div id="nam">秦培峰</div>
    <script>
      //1.因为我们的文档是从上往下加载的，所以的先有标签，所以script写在标签下面
      //2.get 获得element元素by通过 驼峰命名法
      //3.参数id大小写敏感的字符串
      //4.返回的是一个元素对象
      //5.console.dir打印我们返回的元素对象，更好的查看里面的属性和方法
      var name = document.getElementById("nam");
      console.log(nam);
      console.log(typeof nam);
      console.dir(nam);
    </script>
~~~



## 根据标签名获取

~~~
 1.document.getElementsByTagName("标签名")
~~~



~~~html
<body>
    <ul>
      <li>阿峰</li>
      <li>阿峰</li>
      <li>阿峰</li>
      <li>阿峰</li>
      <li>阿峰</li>
    </ul>
    <ol id="ol">
      <li>王江林</li>
      <li>王江林</li>
      <li>王江林</li>
      <li>王江林</li>
    </ol>
    <ol>
      <li>亲凯文</li>
      <li>亲凯文</li>
      <li>亲凯文</li>
      <li>亲凯文</li>
    </ol>
    <script>
      document.getElement;
      //1.返回的是 获取过来的对象的集合 以伪数组的形式储存
      var lis = document.getElementsByTagName("li");
      console.log(lis);
      console.log(lis[0]);
      //2.依次打印里面的元素对象，可以采用遍历对象的方式
      for (var i = 0; i < lis.length; i++) {
        console.log(lis[i]);
      }
      //3.如果一个页面中只有一个li 返回的还是伪数组的形式
      //4.如果没有这个元素，则返回空的伪数组的形式
      //5.element.getElementsByTagName("标签名");父元素必须是指定的单个元素
      //var ol = document.getElementsByTagName("ol");
      //console.log(ol[0].getElementsByTagName("li"));
      var ol = document.getElementById("ol");
      console.log(ol.getElementsByTagName("li"));
    </script>
  </body>
~~~



还可以获取某个元素（父元素）内部所有指定标签的子元素

~~~html
2.element.getElementsByTagName("标签名")
~~~

注意：父元素必须是**单个对象（必须指明是哪一个元素对象）**获取的时候不包括元素自己



## 通过H5新增的方法来获取

**需要考虑兼容性问题**

~~~html
1.document.getElementsByClassName("类名")//根据类名返回对象集合
2.document.querySelector(".box")返回指定选择器的第一个元素， 切记里面的选择器需要加符号 .bax #nav
3.querSelectorAll()返回选择器的所有元素对象集合
~~~

~~~html
 <body>
    <div class="box">123</div>
    <div class="box">123</div>
    <ul id="nav">
      <li>首页</li>
      <li>关于我们</li>
    </ul>
    <script>
      //1.getElementsByClassName 根据类名获得某些元素
      var boxs = document.getElementsByClassName("box");
      console.log(boxs);
      //2.querySelector 返回指定选择器的第一个元素， 切记里面的选择器需要加符号 .bax #nav
      var firstBox = document.querySelector(".box");
      console.log(firstBox);
      var nav = document.querySelector("#nav");
      console.log(nav);
      var li = document.querySelector("li");
      console.log(li);
      //3.querSelectorAll()返回选择器的所有元素对象集合
      var all = document.querySelectorAll(".box");
      console.log(all);
      var lis = document.querySelectorAll("li");
      console.log(lis);
    </script>
  </body>
~~~



## 获取特殊元素

##### 获取body元素

~~~html
<body>
    <script>
      //1.获取body元素
      var bodyEle = document.body;
      console.log(bodyEle);
      console.dir(bodyEle);
      //2.获取html元素
      var htmlEle = document.documentElement;
      console.log(htmlEle);
    </script>
  </body>
~~~



