1. 父传子有哪些方式

1. 子组件在props创建属性，接收父组建传的值；
props用数组的方式接收；或者接收字符串的对象方式；或者使用对象形式接收，如果是数组的类型，需要内部以函数接收；

2. 非props父组件的属性，会自动绑定到子组件中；‘

2. 子传父有哪些方式
需要通过自定义事件实现，子组件数据变化时，通过$emit()触发自定义事件；
子组件设定v-model，通过props与自定义事件实现；


3. 如何让 CSS 只在当前组件中起作用

在组件中的style前面加上scoped，<style scoped>

4. keep-alive 的作用是什么

keep-alive是vue中的内置组件，能在组件切换过程中将状态保留在内存中，防止重复渲染DOM

keep-alive 包裹动态组件时，会缓存不活动的组件实例，而不是销毁它们

keep-alive可以设置以下props属性：

include - 字符串或正则表达式。只有名称匹配的组件会被缓存
exclude - 字符串或正则表达式。任何名称匹配的组件都不会被缓存
max - 数字。最多可以缓存多少组件实例


5. vue中如何获取DOM
1、在组件的DOM部分，任意标签中写上“ref="xxx"”；2、通过组件对象“this.$refs.xxx”获取到元素即可。


6. 请说出 Vue CLI 项目中src目录每个文件夹的文件的用法

assets 文件夹是放静态资源
components 文件夹是放全局组件的
App.vue 入口页面 根组件
main.js 入口文件 加载组件 初始化等

7. 单页面应用的优缺点
优点：
1. 前后端分离，提高开发效率；
2. 业务场景转换，可以进行局部的更新；
3. 用户体验感好，类似本地应用；

缺点：
1. 不利于SEO;
2. 初次首屏加载速度慢；
3. 页面复杂度高；


8. $router和$route的区别

1. router是VueRouter的一个对象，通过Vue.use(VueRouter)和VueRouter构造函数得到一个router的实例对象，这个对象中是一个全局的对象，包含了所有的路由包含了许多关键的对象和属性。例如history对象

$router.push({path:’/path’}); 本质是向history栈中添加一个路由，在我们看来是 切换路由，但本质是在添加一个history记录

$router.replace({path:’/path’}); 替换路由，没有历史记录

2. route是一个跳转的路由对象，每一个路由都会有一个route对象，是一个局部的对象，可以获取对应的name,path,params,query等

$route.path
字符串，等于当前路由对象的路径，会被解析为绝对路径，如 “/index/” 。

$route.params
————————————————
版权声明：本文为CSDN博主「陌子无尘」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/qq_36942042/article/details/102503807

9.  怎么定义 vue-router 的动态路由? 怎么获取传过来的值？
hash: 使⽤ URL hash 值来作路由。⽀持所有浏览器，包括不⽀持 HTML5History Api 的浏览器；
history : 依赖 HTML5 History API 和服务器配置。具体可以查看 HTML5History 模式；
abstract : ⽀持所有 JavaScript 运⾏环境，如 Node.js 服务器端。如果发现没有浏览器的 API，路由会⾃动强制进⼊这个模式.



10. vue-router有几种模式，分别是什么



