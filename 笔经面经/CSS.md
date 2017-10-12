### 1 retina 屏幕是什么
    种具备超高像素密度的液晶屏，同样大小的屏幕上显示的像素点由1个变为多个，如在同样大小的屏幕上，
    苹果设备的retina显示屏中，像素点1个变为4个著作权归作者所有。 在高清显示屏中的位图被放大，图片会变得模糊，
    因此移动端的视觉稿通常会设计为传统PC的2倍那么，前端的应对方案是：设计稿切出来的图片长宽保证为偶数，
    并使用backgroud-size把图片缩小为原来的1/2
### 2 移动端的布局 flexible
    根据不同的dpr和宽度 http://web.jobbole.com/84285/
### 3 怎么实现flexible rem 布局的实现原理 移动端的点透是什么
    点透
        1. A区域是一个浮层，绑定touchstart/touchend事件，事件函数将A区域隐藏。
        2. 点击发生的位置在B区域上方，而B区域恰好能够捕捉click事件（例如原生的a标签），从而被触发。
        3. 这种 在A区域点击，却“透过”A区域，导致B区域也触发 click 事件的情况，我们称之为“点透”。
        所以，避免“点透”的处理方法是：
### 4 异步编程的方式有哪些
    1、回调函数 2、事件监听 3、发布订阅模式 4、Promise构造函数 5、Generator 函数 6、
### 5 CSS布局的属性有哪些
     
### 6 一个有border的div里有张图片，和div的border有空隙，怎么回事
    vertical-align 默认为 baseline 
### 7 position 的几个属性
    absolute relative fixed static inherit
### 8 display 有那几个属性值(10个以上)
    none
    此元素不会被显示。
    block
    此元素将显示为块级元素，此元素前后会带有换行符。
    inline
    默认。此元素会被显示为内联元素，元素前后没有换行符。
    inline-block
    行内块元素。（CSS2.1 新增的值）
    list-item
    此元素会作为列表显示。
    run-in
    此元素会根据上下文作为块级元素或内联元素显示。
    compact
    CSS 中有值 compact，不过由于缺乏广泛支持，已经从 CSS2.1 中删除。
    marker
    CSS 中有值 marker，不过由于缺乏广泛支持，已经从 CSS2.1 中删除。
    table
    此元素会作为块级表格来显示（类似 <table>），表格前后带有换行符。
    inline-table
    此元素会作为内联表格来显示（类似 <table>），表格前后没有换行符。
    table-row-group
    此元素会作为一个或多个行的分组来显示（类似 <tbody>）。
    table-header-group
    此元素会作为一个或多个行的分组来显示（类似 <thead>）。
    table-footer-group
    此元素会作为一个或多个行的分组来显示（类似 <tfoot>）。
    table-row
    此元素会作为一个表格行显示（类似 <tr>）。
    table-column-group
    此元素会作为一个或多个列的分组来显示（类似 <colgroup>）。
    table-column 
    此元素会作为一个单元格列显示（类似 <col>）
    table-cell
    此元素会作为一个表格单元格显示（类似 <td> 和 <th>）
    table-caption
    此元素会作为一个表格标题显示（类似 <caption>）
    inherit
    规定应该从父元素继承 display 属性的值。
### 9 flex布局
    容器属性：http://www.ruanyifeng.com/blog/2015/07/flex-grammar.html
        flex-direction：项目排列方向
        flex-wrap
        flex-flow
        justify-content
        align-items
        align-content
### 10 CSS中的单位
    %
    百分比
    in
    英寸
    cm
    厘米
    mm
    毫米
    em
    1em 等于当前的字体尺寸。
    2em 等于当前字体尺寸的两倍。
    例如，如果某元素以 12pt 显示，那么 2em 是24pt。
    在 CSS 中，em 是非常有用的单位，因为它可以自动适应用户所使用的字体。
    ex
    一个 ex 是一个字体的 x-height。 (x-height 通常是字体尺寸的一半。)
    pt
    磅 (1 pt 等于 1/72 英寸)
    pc
    12 点活字 (1 pc 等于 12 点)
    px
    像素 (计算机屏幕上的一个点)
### 11 盒子模型中的margin折叠问题 
    https://segmentfault.com/a/1190000010521513
### 12 两列等高布局，左右两列中间有个margin=20px，左侧定宽怎么实现，如果左侧不定宽怎么实现
### 13 BFC的定义和特性 
    1、定义：CSS2.1 规范 块级格式化上下文 内部的布局和外部没有关系 浮动元素，绝对定位元素，非块级盒子的块级容器
    （例如inline-blocks，table-cells，and table-captions），以及overflow属性值不是“ visible”
    （visible是overflow的默认值）的块级盒子（视口除外），这些元素就会为他们的内容创建一个BFC。
    2、特性：容器里面的元素不会在布局上影响到外面的元素，并且 BFC 具有普通容器所没有的一些特性。
        A、同一个 BFC 下外边距会发生折叠 ，BFC 可以包含浮动的元素（清除浮动）、BFC 可以阻止元素被浮动元素覆盖、
    3、触发方式：
    body 根元素
    浮动元素：float 除 none 以外的值
    绝对定位元素：position (absolute、fixed)
    display 为 inline-block、table-cells、flex
    overflow 除了 visible 以外的值 (hidden、auto、scroll)    
### 14 如何实现垂直居中
         1、这个方法使用绝对定位的 div，把它的 top 设置为 50％，top margin 设置为负的 content 高度。
         这意味着对象必须在 CSS 中指定固定的高度。
         2、这种方法，在 content 元素外插入一个 div。设置此 div height:50%; margin-bottom:-contentheight;。 
         3、CSS3 top: 50%; left: 50%; transforms:translate(50%,50%) 带上浏览器厂商的前缀
         4、display:table display: table; height: 50px; width: 50px; 
         margin: auto; position: absolute; top: 0; left: 0; bottom: 0; right: 0;  
### 15 CSS3动画
### 16 块级元素、行内元素、行内块级元素都有哪些？使用场景都是什么？为什么要用到行内块级元素          