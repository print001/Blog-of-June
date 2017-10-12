### 1 如何实现倒计时秒杀功能
    getMonth(),getDate(),getHours(),getMinutes(),getSeconds()
### 2 ES6箭头函数的理解
    
### 3 同源策略 跨域的方式有哪些
      1、浏览器的同源策略，限制了来自不同源的"document"或脚本，对当前"document"读取或设置某些属性。 （白帽子讲web安全[1]）
      2、从一个域上加载的脚本不允许访问另外一个域的文档属性。
### 4 轮播图实现和优化
      
### 5 ES6中的特性是什么，为什么
### 6 函数调用的方式有哪些，区别是什么
    方法调用模式
    函数调用模式
    构造器调用模式
    apply调用模式
### 7 原型链(要非常清楚)
### 8 用过什么框架，iquery
### 9 说说异步编程
### 10 回调地狱是什么，有什么问题，异常捕获怎么做
### 11 promise是什么，有多个then，第一个then出错了 后面的then会执行吗？ 如何在这种情况下让后面的than执行
### 12 学习js的时候遇到过什么坑， js那些知识比较难
### 13 登陆状态怎么保持
### 14 本地存储 cookie,webstorage,session 区别，特点
    答：cookie是客户端的状态保持方案。cookie的内容主要包括：名字，值，过期时间，路径和域。路径与域一起构成cookie的作用范围。若不设置过期时间，则表示这
    个cookie的生命期为浏览器会话期间，关闭浏览器窗口，cookie就消失。
    session机制是一种服务器端的机制，服务器使用一种类似于散列表的结构（也可能就是使用散列表）来保存信息。
    1、cookie数据存放在客户的浏览器上，session数据放在服务器上。
    2、cookie不是很安全，别人可以分析存放在本地的COOKIE并进行COOKIE欺骗
       考虑到安全应当使用session。
    3、session会在一定时间内保存在服务器上。当访问增多，会比较占用你服务器的性能
       考虑到减轻服务器性能方面，应当使用COOKIE。
    4、单个cookie保存的数据不能超过4K，很多浏览器都限制一个站点最多保存20个cookie。
    webstorage 是HTML5引入的客户端存储方式。
    能够对浏览器使用事件钩子，例如offline，online，storage change
    比cookies更便于管理，没有额外的的请求头部数据
    提供更大的空间以存贮日益剧增的复杂数据
### 15 前端优化有哪些
    性能优化：1、减少http请求，合理设置 HTTP缓存
             2、使用浏览器缓存
             3、启用压缩
             4、CSS Sprites合并 CSS图片，减少请求数的又一个好办法。
             5、LazyLoad Images
             6、CSS放在页面最上部，javascript放在页面最下面
             7、减少cookie传输
             8、异步请求Callback（就是将一些行为样式提取出来，慢慢的加载信息的内容）
             9、减少cookie传输
             10、减少DOM操作
### 16 一个dom有两个节点 找出公共父节点
### 17 说一下强缓存和协商缓存,浏览器缓存问题
    前端缓存机制，如果去掉etags\last-modefied\cache-control这些控制缓存的字段，浏览器会怎么处理缓存 
         http://www.cnblogs.com/wangpenghui522/p/5498427.html    
         1、cache-control和expires
         Cache-Control与Expires的作用一致，都是指明当前资源的有效期，控制浏览器是否直接从浏览器缓存取数据还是
         重新发请求到服务器取数据。只不过Cache-Control的选择更多，设置更细致，如果同时设置的话，其优先级高于Expires。
         2、etags和last-modefied
         配置Last-Modified/ETag的情况下，浏览器再次访问统一URI的资源，还是会发送请求到服务器询问文件是否已经修改，
         如果没有，服务器会只发送一个304回给浏览器，告诉浏览器直接从自己本地的缓存取数据；如果修改过那就整个数据重新
         发给浏览器；
### 18 websocket 聊天室如果发送失败了，怎么解决，如何做到发送文件，websocket的使用，底层是如何处理的
### 18 什么是xss 如何防止
    XSS（cross-site scripting跨域脚本攻击）攻击是最常见的Web攻击，其重点是“跨域”和“客户端执行”。有人将XSS攻击分为三种，分别是：
        1. Reflected XSS（基于反射的XSS攻击）
        2. Stored XSS（基于存储的XSS攻击）
        3. DOM-based or local XSS（基于DOM或本地的XSS攻击）
        CSRF:跨站请求伪造， 攻击者盗用了你的身份，以你的名义发送恶意请求
### 19 事件机制，事件绑定，冒泡到document还是window
### 20 tap怎么回事 和click的区别
### 21 video格式不支持如何给出提示
### 21 短轮询 comet 长轮询都介绍一下
    长链接：
        HTTP长连接，与一般每次发起http请求或响应都要建立一个tcp连接不同，http长连接利用同一个tcp连接处理多个http请求和响应，
        也叫HTTP keep-alive，或者http连接重用。使用http长连接可以提高http请求/响应的性能。
    短链接：
        每次请求都重新建立一个链接
    长链接短链接的优缺点：
        由上可以看出，长连接可以省去较多的TCP建立和关闭的操作，减少浪费，节约时间。
        对于频繁请求资源的客户端适合使用长连接。在长连接的应用场景下，client端一般不会主动关闭连接，当client与server之间的连接一直不关闭，
        随着客户端连接越来越多，server会保持过多连接。这时候server端需要采取一些策略，如关闭一些长时间没有请求发生的连接，
        这样可以避免一些恶意连接导致server端服务受损；如果条件允许则可以限制每个客户端的最大长连接数，这样可以完全避免恶意的客户端拖垮整体后端服务。
        短连接对于服务器来说管理较为简单，存在的连接都是有用的连接，不需要额外的控制手段。但如果客户请求频繁，
        将在TCP的建立和关闭操作上浪费较多时间和带宽。长连接和短连接的产生在于client和server采取的关闭策略。
        不同的应用场景适合采用不同的策略。
    长轮询：
        http 长轮询是服务器收到请求后如果有数据, 立刻响应请求; 如果没有数据就会 hold 一段时间, 这段时间内如果有数据立刻响应请求; 如果时间到了还没有数据, 
        则响应 http 请求;浏览器受到 http 响应后立在发送一个同样 http 请求查询是否有数据;
        http 长轮询的局限:
        浏览器端对统一服务器同时 http 连接有最大限制, 最好同一用户只存在一个长轮询;
        服务器端没有数据 hold 住连接时会造成浪费, 容易产生服务器瓶颈;
    comet:
        客户端发起请求之后，保持长连接，服务器有消息时就推送给客户端 优缺点：一个明显的好处是服务器完全能够控制更新数据的时间和频率。另外，这种方法效率高，
        因为始终保持连接。缺点是保持连接状态会浪费服务器端的资源。服务器推送还比较容易中断。
    http://caibaojian.com/http-connection-and-websocket.html
### 22 跨域的方法 
    什么是跨域：当协议、子域名、主域名、端口号中任意一各不相同时，都算不同的“域”。
    1、JSONP 以下是实现方法
    //创建一个script元素
    var  Scr = document.reateElement('script');
    //声明类型
    Scr.type='text/javascript';
    //添加src属性，引入跨域访问的url
    Scr.src='http://www.b.com/gerinfo.php';
    //在页面中添加新创建的script元素
    document.getElementsByTagName('head')[0].appendChild(Scr)
    2、跨域资源共享（CORS）
     * IE10以下的版本都不支持
      * 只需要在服务器端头部加上下面两句代码：
      header( "Access-Control-Allow-Origin:*" );
      header( "Access-Control-Allow-Methods:POST,GET" );
    3、代理：通过后台(ASP、PHP、JAVA、ASP.NET)获取其他域名下的内容，然后再把获得内容返回到前端
    4、处理跨域的方法3 -- XHR2 （H5）
### 23 因为引用计数产生的内存泄漏，在ES6中的解决办法是什么
    es6 中的let命令 用来声明块级变量 不存在函数声明提升
### 24 js中基本类型在内存中存储方式是什么，引用类型的存储方式是什么
### 25 封装的js插件，事件委托
    用立即执行函数(匿名函数)，封装js插件 对与ES6 使用module对插件封装
    事件委托：事件委托是通过事件冒泡的原理，利用父级去触发子级的事件
    好处:不用重复绑定多个事件，原生写法
    _wrap.addEventListener('click', function(ev){
     var ev = ev || event; 
     if( ev.target.nodeName == 'LI' ) {
      ev.target.style.background = '#8EC0E4'; 
      console.log( ev.target.innerHTML ); } // 找到父级 ul#wrap
       this.style.border = '2px solid #f00'; }); 
    $('#wrap').on('click', 'li', function(ev) { // this 指向委托的对象 li 
    $(this).css('background', '#D4DFE6'); // 找到父级 ul#wrap $(ev.delegateTarget).css('border', '2px solid #f00'); }) 

### 26 从输入url到看到页面发生了什么 
    http://www.cnblogs.com/kongxy/p/4615226.html
    DNS解析：浏览器缓存->系统缓存->路由器缓存->ISP DNS缓存->递归搜索
    TCP连接：浏览器最终得到了解析后的IP，并尝试用这个IP和服务器在三次握手后建立一个TCP连接
    发送HTTP请求：
    服务器处理请求并返回HTTP报文
    浏览器解析渲染页面：浏览器接收到HTTP响应，关闭TCP连接； HTML解析出DOM Tree->CSS解析出Style Rules->将二者关联生成Render Tree
    ->Layout 根据Render Tree计算每个节点的信息->Painting 根据计算好的信息绘制整个页面 
### 27 实现深拷贝
    深拷贝和浅拷贝：浅复制只复制一层对象的属性，复制属性地址，而深复制则递归复制了所有层级。
    var y = $.extend({}, x),          //shallow copy
       z = $.extend(true, {}, x);    //deep copy        
### 28 类数组有哪些 
    arguements,nodeList   
### 29 for in的缺点
    for in能访问可遍历的，实例和原型中的属性  
### 30 forEach()
    对数组中的没一项运行给定函数，没有返回值     

### 32 模块化, webpack, AMD和CMD
    1、commonJS:每个文件就是一个模块，有自己的作用域。在一个文件里面定义的变量、函数、类，都是私有的，对其他文件不可见。
    定义输出module.exports.name 加载模块require('')
    2、AMD(异步模块定义)：实现js文件的异步加载，避免网页失去响应；管理模块之间的依赖性，便于代码的编写和维护。
        require.js 用法 define([依赖的模块]，function(模块){}) require([依赖的模块]，function(){}) require.config
    3、CMD(通用模块定义)：
    AMD推崇依赖前置，在定义模块的时候就要声明其依赖的模块
    CMD推崇就近依赖，只有在用到某个模块的时候再去require
    4、webpack: 模块化，析你的项目结构，找到JavaScript模块以及其它的一些浏览器不能直接运行的拓展语言（Scss，TypeScript等），
    并将其打包为合适的格式以供浏览器使用。    
### 33 Symbol，写一个应用实例，并说出它的其他应用场景 
    1、什么是Symbol：ES6引入的新的基本数据类型，表示独一无二的值 防止变量名冲突
    2、用法：let s1 = Symbol('描述');s1.toString() // "Symbol(foo)"描述可不加
    a[s1](){}
    3、应用实例：消除魔术字符串、
### 34 事件循环知道吗？描述一下它的实现原理和应用场景。
    http://www.ruanyifeng.com/blog/2013/10/event_loop.html 
### 35 HTML5、ES6新特性 
    HTML5:
       1、新增了语义化的标签
       2、canvas、svg、vedio audio、
       3、webstorage
       4、引入了应用程序缓存 manifest
       5、 表单控件 calendar、date、time、email、url、search;
       6、 新的技术webworker, websocket, Geolocation;
     ES6:  
       1、新增代码块命令：let const
       2、新增解构赋值、symbol基本数据类型
       3、函数对象的扩展、promise对象 set map iterator calss module 
### 36 性能优化中离线操作 
    manifest? 
### 37 delegate bind on (jquery事件委托和异步编程)
     delegate()方法属于异步式加载绑定，dom元素加载未完成之前，可以委托给delegate() 方法来实现的绑定操作。    