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
> 