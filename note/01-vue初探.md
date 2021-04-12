### 模板语法
> 表达式： 
> 1. 运算
> 2. 三元运算符
> 3. 不能够方JS语法
> 4. 函数执行的返回值
```html
<div id="app">{{msg}}</div>
```
### 直接给data中的对象增加或者删除属性无法成为响应式的
> 正确做法就是
> vm.$set(vm.obj,'age',10);
> vm.$set(vm.obj);
```js
vm.data.obj.name = '123123'
```
### 数组
```js
vm.obj.arr[1] = 1;
也无法起作用    
```

### Vue的以下实例方法
>  vm.$mount()
>  vm.$el
> vm.$set/vm.$delete
> vm.watch() 监视数据的变化
> vm.$nextTick 获取DOM元素
> vm.$data


### 实例上的属性

### 指令 v-
> 有特定功能的指令，可以操作DOM元素
> v-for 遍历
> v-html 使用innerHTML渲染
> v-once 只渲染一次
> v-bind 绑定
> v-model 表单元素  双向的数据绑定
> v-on 绑定事件 @
> v-show v-if / v-else


### 指令复习
v-for (数组，对象，数字，字符串)
v-once(只渲染一次)
v-html
v-text
v-bind: 双向绑定数据
v-model 表单元素双向绑定
v-on 
v-if/v-else: 操作DOM元素的显示或者隐藏（添加和移除)
v-show 通过有display:none;来控制隐藏

### 事件修饰符(modifiers)
> event.preventDefault|event.stopPropagation 阻止默认事件| 阻止冒泡
> （Vue关心的：数据你来，DOM元素我来）
> .stop
> .prevent
> .capture (事件传播：捕获，冒泡) 改成捕获来处理事件 (DOM2支持)
> .self 表示事件源是自己的时候才会被触发
> .once 只触发一次
> .passive  滚动（onScroll）的默认行为会被立即触发（移动端的时候，让滚动立即执行
> 看起来更流畅）

### 表单修饰符
.number 将用户输入的东西转为数字
.lazy (比如input失去焦点的时候才出发更新视图)
.trim 自动过滤收尾空白

## 注册自定义指
```js
// 注意区分
<input v-focus="red"> //(变量red)
<input v-focus="'red'">//(字符串red)
```
### 注册成局部指令
```js
Vue.directive('')
```
### 注册成全局指令