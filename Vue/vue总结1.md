## 关于Vue创建实例和生命周期
### 创建实例以及各种选项的理解
    var vm= new Vue({
    el:'#app',// vue实例的HTML页面挂载目标 这里指的是index.html中的#app
    data(){ // 定义和组件挂钩的数据
    },
    props:{},// 从父组件接受的数据
    conputed:{},// 观察单个数据变化
    watch:{}, // 观察多个数据变化，
    methods:{}, // 定义组件方法，用this.fn访问
    components:{}, // 注册需要的组件
    render: // createElement()创建App组件，把App组件挂载到index->#app中(实际是替换了)
    })
### 生命周期
  1、beforeCreate 此时$el、data 的值都为undefined
  2、created创建之后，此时可以拿到data的值，但是$el依旧为undefined
  3、mount之前，$el的值为“虚拟”的元素节点
  4、mounted之后，mounted之前，“虚拟”的dom节点被真实的dom节点替换，并将
  其插入到dom树中，于是在触发mounted时，可以获取到$el为真实的dom元素()
  myVue.$el===document.getElementById("app-8")  // true
### Vue Router

