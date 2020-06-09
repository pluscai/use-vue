# 一、Essentials

## 1.1 Installation

### NPM

> NPM is the recommended installation method when building large scale applications with Vue.

开发应用程序时，Vue推荐用NPM,能够很好的和webpack结合起来。 



### CLI

>  Vue provides an [official CLI](https://github.com/vuejs/vue-cli) for quickly scaffolding ambitious Single Page Applications. It provides batteries-included build setups for a modern frontend workflow. It takes only a few minutes to get up and running with hot-reload, lint-on-save, and production-ready builds.

Vue官方提供了CLI工具，快速搭建一个应用，并内置了热重载、代码检测、构建发布。



### Explanation of Different Builds

#### Runtime+Compiler VS Runtime-only

> Since the runtime-only builds are roughly 30% lighter-weight than their full-build counterparts, you should use it whenever you can.

正式发布的版本中，用runtime的，因为所有vue代码都已经在compiler阶段被编译成了原生js，发布版本中只管运行就行了。

#### Development vs Production Mode

> CommonJS and ES Module builds are intended for bundlers, therefore we don’t provide minified versions for them. You will be responsible for minifying the final bundle yourself.

在webpack类似打包工具中，需要自己通过配置方式从开发模式切换到生产模式。



#### CSP environment

Content Security Policy(CSP)环境中不能使用`new Function`,而vue的编译过程（计算表达式时）恰恰依赖此特性，但是runtime-only的构建方式兼容CSP环境，因为不需要编译。



## 1.2 Introduction

### What is Vue.js

- 渐进式框架、核心代码专注于视图层；

- 可以整合进其他库、项目，也可以开发单页面应用  

和react的介绍如此相像啊！



### Getting Started

> We **do not** recommend that beginners start with `vue-cli`, especially if you are not yet familiar with Node.js-based build tools

构建工具都是基于 Node.js的



### Declarative Rendering

>  At the core of Vue.js is a system that enables us to declaratively render data to the DOM using straightforward template syntax

声明式渲染，指的数据渲染和markup标记揉杂在一起，例如：

```vue
<div id="app">
  {{ message }}
</div>
```



### Conditonals and Loops

```vue
<div id="app-3">
  <span v-if="seen">Now you see me</span>
</div>
```

> This example demonstrates that we can bind data to not only text and attributes, but also the **structure** of the DOM

不仅可以将数据与文本、属性值绑定，还能绑定DOM结构、动画效果（DOM元素进行增删改时的动画效果），非常强大哦~



### Handling User Input

> To let users interact with your app, we can use the `v-on` directive to attach event listeners that invoke methods on our Vue instances

vue中用`v-on`指令，监听处理用户交互；`v-model`的双向数据绑定真是香。



### Composing with Components

> This is a contrived example, but we have managed to separate our app into two smaller units, and the child is reasonably well-decoupled from the parent via the props interface. We can now further improve our `<todo-item>` component with more complex template and logic without affecting the parent app.

原来Vue中的父组件给子组件传递数据也是用的`props`,跟react是一样的。





## 1.3 The Vue Instance

### Creating a Vue Instance

```vue
var vm = new Vue({
  // options
})
```

>  When you create a Vue instance, you pass in an **options object**. The majority of this guide describes how you can use these options to create your desired behavior.

整个文档就是关于如何写options里的代码来达到目的。



### Data and Methods

- 数据改变，视图层会re-render，这点和React是一样的

- vue实例本身也提供了一些有用的方法和属性，以`$`开头（和用户自定义的属性作区分）



### Instance Lifecycle Hooks







## 1.4 Template Syntax

## 1.5 Computed Properties and Watchers

## 1.6 Class and Style Bindings

## 1.7 Conditonal Rendering

## 1.8 List Rendering

## 1.9 Event Handling

## 1.10 Form Input Bindings

## 1.11 Components Basics

## 二、Components In-Depth

## 三、Transitons & Animation



# 四、Reuseability & Compostion



# 五、Tooling



# 六、Scaling Up



# 七、Internals



# 八、Migrating



# 九、Meta



