1.客户端与服务器

### 1.1 上网的目的

- 刷微博
- 看新闻
- 在线听音乐
- 在线看电影
- .....

上网的==**本质目的**==：通过互联网的形式来==**获取和消费资源**==

### 1.2服务器

上网过程中，负责==**存放和对外提供资源**==的电脑，叫做服务器

![](D:\前端学习\Ajax  git\Ajax code\day1\Typora img (第一天)\AJax img.jpg)

### 1.3客户端

上网过程中，负责==**获取和消费资源**==的电脑，叫做客户端

![](D:\前端学习\Ajax  git\Ajax code\day1\Typora img (第一天)\Snipaste_2023-04-13_11-33-58.jpg)

# 2.URL地址

### 2.1URL地址的概念

URL（全称是Uniform Resource Locator）中文叫==**统一资源定位符**==，用于标识互联网上每个资源的唯一存放位置。浏览器只有通过URL地址，才能正确定位资源的存放位置，从而成功访问到对应的资源。

常见的URL举例：

http://www.baidu.com

http://www.taobao.com

http://www.cnblogs.com/liulongbinblogs/p/11649393.html

### 2.2URL地址的组成部分

URL地址一般由三部分组成：

1. 客服端与服务器之间的==**通信协议**==
2. 存有该资源的==**服务器名称**==
3. 资源在服务器上==**具体的存放位置**==

![](D:\前端学习\Ajax  git\Ajax code\day1\Typora img (第一天)\img.png)

# 3.客户端与服务器的通信过程

### 3.1图解客户端与服务器的通信过程

![](D:\前端学习\Ajax  git\Ajax code\day1\Typora img (第一天)\Snipaste_2023-04-13_18-27-32.jpg)

==注意：==

1. 客户端与服务器之间的通信过程，分为==**请求**==—==**处理**==—==**响应**==三个步骤
2. 网页中的每一个资源，都是通过==**请求**==—==**处理**==—==**响应**==的方式从服务器获取回来的

### 3.2基于浏览器的开发者工具分析通信过程

![](D:\前端学习\Ajax  git\Ajax code\day1\Typora img (第一天)\图片1.png)

1. 打开Chrome浏览器
2. <u>Ctrl+shift+I</u>打开Chrome的开发者工具
3. 切换到Network面板
4. 选中Doc 页签
5. 刷新页面，分析客户端与服务器的通信过程

# 4服务器对外提供了哪些资源

### 4.1例举网页中常见的资源

![](D:\前端学习\Ajax  git\Ajax code\day1\Typora img (第一天)\Snipaste_2023-04-13_18-49-11.jpg)

### 4.2数据也是资源

==**网页中的数据，也是服务器对外提供的一种资源。**==例如股票数据、各行业排行榜。

![](D:\前端学习\Ajax  git\Ajax code\day1\Typora img (第一天)\图片2.png) ![](D:\前端学习\Ajax  git\Ajax code\day1\Typora img (第一天)\图片3.png) 

### 4.3数据是网页的灵魂

![](D:\前端学习\Ajax  git\Ajax code\day1\Typora img (第一天)\Snipaste_2023-04-13_18-54-41.jpg) 

### 4.4网页中如何请求数据

==数据、也是==**服务器**对外提供的一种资源。只要是资源，必然要通过==**请求**==—==**处理**==—==**响应**==的方式进行获取

![](D:\前端学习\Ajax  git\Ajax code\day1\Typora img (第一天)\Snipaste_2023-04-13_19-28-24.jpg) 

 如果要在网页中请求服务器上的数据资源，则需要用到==XMLHttpRequest==对象

XMLHttpRequest（简称 xhr）是浏览器提供的 js 成员，通过它，可以请求服务器上的数据资源。

最简单的方法： **`let xhrObj = new XMLHttpRequest()`**

### 4.5资源的请求方式

客户端请求服务器时,==请求的方法==有很多种，最常见的两种请求方法分别为==*get*==和==*post*==

- ==**get请求**==通常用于==**获取服务端资源**==（向服务器要资源）

​       例如：根据URL地址，从服务器获取HTML文件、css文件、js文件、图片文件、数据资源等

- ==**post请求**==通常用于==**向服务器提交数据**==（往服务器发送资源）

​       例如：登陆时向服务器==提交的登录信息==、注册时向服务器==提交的注册信息==、添加用户时向服务器==提交的用户信息==等各种==**数据提交操作**==

# 5.了解Ajax

### 5.1什么是Ajax

Ajax的全称是Asynchronous JavaScript And XML  (异步 JavaScript 和 XML)。

通俗的理解：在网页中==**利用 XMLHttpRequest对象 和服务器进行数据交互的方式，就是Ajax**==

### 5.2为什么要学Ajax

之前所学的技术，只能把网页做的更美观漂亮，或添加一些动画效果，但是。==Ajax==能让我们轻松实现**网页**与**服务器**之间的==数据交互==  

![](D:\前端学习\Ajax  git\Ajax code\day1\Typora img (第一天)\Snipaste_2023-04-13_19-49-28.jpg) 

### 5.3Ajax的典型应用常景

1. **用户名检测**：注册用户是，通过Ajax的形式，动态==检测用户名受否被占用==

![](D:\前端学习\Ajax  git\Ajax code\day1\Typora img (第一天)\图片4.png) 

------



2. **搜索提示**：当输入搜索关键字时，通过Ajax的形式，动态==加载搜索提示列表==

![](D:\前端学习\Ajax  git\Ajax code\day1\Typora img (第一天)\图片5.png) 

------



3. **数据分页显示**：当点击页码值的时候，通过Ajax的形式，==根据页码值动态刷新表格的数据==

![](D:\前端学习\Ajax  git\Ajax code\day1\Typora img (第一天)\图片6.png) 

------

 **数据的增删改查**：数据的添加、删除、修改、查询操作，都需要通过Ajax的形式，来实现数据的交互

![](D:\前端学习\Ajax  git\Ajax code\day1\Typora img (第一天)\图片7.png)

# 6.jQuery中的Ajax

### 6.1了解jQuery中的Ajax

浏览器提供的==XMLhttpRequest 用法比较复杂==所以jQuery对XMLHttpRequest 进行了封装，提供了一系列Ajax相关的函数，极大的==降低了Ajax的使用难度==

jQuery中发起的Ajax 请求最常用的三个方法如下：

- ==**$.get()**==
- ==**$.post()**==
- ==**$.ajax()**==

### 6.2 $.get()函数的语法

jQuery中 **$.get()**函数功能单一，专门用来发起**get请求**，从而将服务器上的资源请求到客户端来进行使用。

**$.get()** 的函数语法如下：

~~~JavaScript
$.get(url,[data],[callback])   //[] 可选参数  
~~~

其中，三个参数各自代表的含义如下：

![](D:\前端学习\Ajax  git\Ajax code\day1\Typora img (第一天)\Snipaste_2023-04-13_20-13-46.jpg) 

### 6.2 $.get() 发起==不带参数==的请求

使用$.get() 函数发起不带参数的请求时，直接提供==请求的URL地址==和==请求成功之后的回调函数==即可

示例代码如下： 

~~~JavaScript
$.get('http://www.liulongbin.top:3006/api/getbooks',function(res){
      console.log(res)  //这里的 res 是服务器返回的数据
      })
~~~

![](D:\前端学习\Ajax  git\Ajax code\day1\Typora img (第一天)\1.png) 



------



### 6.2 $.get() 发起==带参数==的请求

使用$.get() 函数发起带参数的请求时，实例代码如下：

~~~JavaScript
$.get('http://www.liulongbin.top:3006/api/getbooks', {id : 1}, function(res){
      console.log(res)  //这里的 res 是服务器返回的数据
      })
~~~

![](D:\前端学习\Ajax  git\Ajax code\day1\Typora img (第一天)\2.png) 

### 6.3$.post()函数的语法

jQuery中 **$.post()**函数功能单一，专门用来发起**post请求**，从而向服务器提交数据。

**$.post()** 函数的语法如下：

~~~JavaScript
$.post( url , [data], [callback] )
~~~

其中，三个参数各自代表的含义如下：

![](D:\前端学习\Ajax  git\Ajax code\day1\Typora img (第一天)\Snipaste_2023-04-14_09-26-10.jpg) 

### 6.3$.post()向服务器提交数据

使用$.post() 向服务器提交数据的示例代码如下：

~~~JavaScript
$.post(
'http://www.liulongbin.top:3006/api/addbook', //请求的URL地址
    { bookname：'水浒传'，author: '施耐庵', publisher:'上海图书出版社'}，  //提交的数据
    function(res)  {  // 回调函数
     console.log(res)
    }
 )
~~~

### 6.4 $.Ajax()函数的语法

相比于jQuery.get() 和 jQuery.post() 函数，jQuery中提供的 $.ajax()函数，是一个功能比较综合的函数，它允许我们对Ajax请求进行更详细的配置。

$.ajax() 函数的基本语法如下：

~~~JavaScript
$.ajax({
    type: '',   // 请求的方式，例如 GET 或 POST
    url: '',    // 请求的 URL 地址
    data: { },  // 这次请求要携带的数据
    success： function（res) { }  // 请求成功之后的回调函数
})
~~~

### 6.4 使用$.ajax() 发起 GET请求

使用$.ajax() 发起 GET请求时，只需要将==type 属性== 的值设置为 '==GET=='即可

~~~JavaScript
$.ajax({
    type: 'GET',   // 请求的方式，例如 GET 或 POST
    url: 'http://www.liulongbin.top:3006/api/getbooks',    // 请求的 URL 地址
    data: { id: 1 },   // 这次请求要携带的数据
    success： function（res) {  // 请求成功之后的回调函数
        console.log(res)
  } 
})
~~~

### 6.4 使用$.ajax() 发起 POST请求

使用$.ajax() 发起POST请求时，只需要将==type 属性== 的值设置为 '==POST=='即可

~~~javascript
$.ajax({
    type: 'POST',   // 请求的方式
    url: 'http://www.liulongbin.top:3006/api/addbook',  // 请求的url地址
    data: {  // 要提交给服务器的数据
      bookname：'水浒传'，
      author: '施耐庵',
      publisher:'上海图书出版社'
    }，
    success:function(res) {   // 请求成功之后的回调函数
        console.log(res)
    }
})
~~~

# 7.接口

### 7.1 接口的概念

使用Ajax 请求数据时，==被请求的URL地址==，就叫做==数据接口==（简称**接口**）。同时，每个接口必须有==请求方式==

例如：http://www.liulongbin.top:3006/api/getbooks  获取图书列表的接口(GET请求)

​         http://www.liulongbin.top:3006/api/addbook   添加图书的接口（POST请求）

### 7.2 分析接口的请求过程

##### 1.通过GET方式请求接口的过程

![](D:\前端学习\Ajax  git\Ajax code\day1\Typora img (第一天)\Snipaste_2023-04-14_10-42-07.jpg) 

##### 2.通过POST方式请求接口的过程

![](D:\前端学习\Ajax  git\Ajax code\day1\Typora img (第一天)\Snipaste_2023-04-14_10-42-43.jpg) 

### 7.3接口测试工具

##### 1.什么是接口测试工具

为了验证接口能否被正常被访问，我们常常需要使用接口测试工具，来对数据接口进行检测。

==好处==：接口测试工具能让我们在==不写任何代码==的情况下，对接口进行==调用==和==测试==。  

工具： ==post Man==

##### 2.下载网址

网址 <https://www.getpostman.com/downloads/>

##### 3.了解post Man界面的组成部分

![](D:\前端学习\Ajax  git\Ajax code\day1\Typora img (第一天)\Snipaste_2023-04-14_11-01-03.jpg)

### 7.4 使用post Man测试GET接口

![](D:\前端学习\Ajax  git\Ajax code\day1\Typora img (第一天)\图片11.png) 

**步骤：**

1. 选择请求的方式
2. 填写请求的URL地址
3. 填写请求的参数
4. 点击Send按发起GET请求
5. 查看服务器响应的结果

### 7.4 使用post Man测试POST接口 

![](D:\前端学习\Ajax  git\Ajax code\day1\Typora img (第一天)\22.png) 

**步骤：**

1. 选择请求的方式
2. 选择请求的URL地址
3. 选择Body面板并==勾选数据格式==
4. 填写要发送到服务器的数据
5. 点击Send按钮发起POST请求
6. 查看服务器响应的结果

### 7.6接口文档

##### 1.什么是接口文档

接口文档，顾名思义就是==接口的说明文档，他是我们调用接口的依据==。好的接口文档包含了**对接口URL** ，**参数**以及**输出内容**的说明，我们参照接口文档就能方便的知道接口的作用，以及接口如何调用。

##### 2.接口文档组成部分

接口文档可以包含很多信息，也可以按需进行精简，不过，一个合格的接口文档，应该包含以下6项内容，从而为接口的调用提供依据：

1. ==**接口名称**==：用来标识各个接口的简单说明，如**登录接口**，**获取图书列表接口**等
2. ==**接口URL**==:  接口的调用地址
3. ==**调用方式**==：接口的调用方式，如**GET**或**POST**
4. ==**参数格式**==： 接口需要传递的参数，每个参数必须包含**参数名称**、**参数类型**、**是否必选**、**参数说明**
5. ==**响应格式**==：接口的返回值的详细描述，一般包含**数据名称**、**数据类型**、**说明** 3项内容
6. 返回示例(可选)： 通过对象的形式，列举服务器返回数据的结构

# 8.案例—图书管理

### 8.2案例用到的库和插件

用到的css库 bootstrap.css

用到的JavaScript库jQuery.js

用到的vs code 插件 Bootstrap 3 Snippets

# 9案例-聊天机器人

