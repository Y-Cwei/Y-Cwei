# elm_app-v2.0

> A Vue.js project

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

For detailed explanation on how things work, checkout the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).

# vue1.0升级为vue2.0
* vue-router变化
	* 初始化路由
	* v-link ==> <router-link>
	* keep-alive ===> <keep-alive>
* v-for指令
	* 移除$index
	* v-for=”(item, index) in items”
* v-el与v-ref指令
	* ref指令 ref=’xxx’
	* this.$refs.xxx
* 组件的模板
	* 只允许有一个根标签
* 组件间通信
	* $dispatch()/$broadcast()被移除, 只留下$emit
	* events选项被移除, 通过v-on指令绑定监听
	* 不能直接在子组件中修改父组件传入的prop
* 过渡
	* <transition>
	* transitions选项被移除
	* 过滤css
     .fade-enter: 进入的开始状态(不可见), 在此指定进入显示前不可见的样式
       .fade-leave-active: 离开的结束状态(不可见), 在此指定离开后不可见的样式
       .fade-enter-active: 进入的结束状态(可见), 在此指定显示的transition
       .fade-leave-active: 离开的结束状态(不可见),在此指定隐藏的transition
	* JS动画
     <transition name="drop"
            @before-enter="beforeDrop"
            @enter="dropping"
            @after-enter="afterDrop"
            v-bind:css="false">
* 虚拟DOM/组件的生命周期
	* 生命周期回调函数有增减
	* 移除: ready()
	* 增加: mounted() / beforeUpdate() / afterUpdate()

