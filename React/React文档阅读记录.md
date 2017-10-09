## React 文档阅读笔记
***
2017.10.04
***
###Components和Props
Components是什么？
   Components是组件的概念，把页面分成各个部分独立开发，最后拼凑起来整个页面
定义Compones的方法
   1、functional 
    function Welcome(props) {
    return <h1>Hello, {props.name}</h1>;}