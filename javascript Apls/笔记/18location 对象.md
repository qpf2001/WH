# location 对象

什么是location对象

window对象给我们提供了一个location属性，用于获取或设置窗体的url,并且用于解析url，因为这个属性返回的是一个对象，所以我们将这个对象也称之为loction对象！

## url

统一资源定位符，是互联网上标准资源的地址。互联网上的每个文件都有一个唯一的url,它包含的信息指出文件的位置以及浏览器因该怎么去处理它。

#### url 的一般语法格式

~~~js
protocol://host[:port]/path/[?query]#fragment
http://www.itcast.cn/index.html?name=andy&age=18#link
~~~

~~~~js
protocol : 通信协议，常用的http,ftp,maito
host     : 主机（域名）www.itcast.cn
prot     : 端口号，可选，省略时使用方案默认的端口，如http默认端口就是80
pathname     : 路径，由零个或者多个‘/’符号隔开的字符串，一般用来表示主机上的一个目录或文件地址
query    : 参数， 以键值的形式，通过&符号分割开来
fragment : 片段，#后面的内容 常见于链接锚点
~~~~

#### location 对象属性

~~~
location.href  : 获取或者设置整个url
location.host  : 返回主机（域名）www.itcast.cn
location.prot  : 端口号,如果未写，返回空的字符串
location.pathname  : 返回路径
location.query :返回参数
location.fragment : 返回片段 #后面内容 常见于链接锚点
~~~

#### location 对象方法

~~~js
location.assign()  : 跟href一样，可以跳转页面（也称为重定向页面）
location.replace() : 替换当前页面，应为不记录历史，所以不能后退页面
location.reload()  : 重新加载页面，相当于刷新按钮，或者按下F5,如果参数为true，强制刷新 ctrl+f5
~~~





