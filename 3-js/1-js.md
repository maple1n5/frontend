# JavaScript

## 简介

JS 是一种运行在客户端（浏览器）的编程语言，可以用来创建动态更新的内容，控制多媒体，制作图像动画等交互效果。

JavaScript 程序不能独立运行，它需要被嵌入 HTML 中，然后浏览器才能执行 JavaScript 代码。通过 `script` 标签将 JavaScript 代码引入到 HTML 中，有两种方式：

**内部方式：**

~~~html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>JavaScript 基础 - 引入方式</title>
</head>
<body>
  <!-- 内联形式：通过 script 标签包裹 JavaScript 代码 -->
  <script>
    alert('嗨，你好！')
  </script>
</body>
</html>
~~~

**外部方式：**

~~~javascript
// demo.js
document.write('嗨, 你好！')
~~~

~~~html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>JavaScript 基础 - 引入方式</title>
</head>
<body>
  <!-- 外部形式：通过 script 的 src 属性引入独立的 .js 文件 -->
  <script src="demo.js"></script>
</body>
</html>
~~~

如果 script 标签使用 src 属性引入了某 .js 文件，那么 标签的代码会被忽略！！！如下代码所示：

~~~html
<!-- 外部形式：通过 script 的 src 属性引入独立的 .js 文件 -->
<script src="demo.js">
    // 此处的代码会被忽略掉！！！！
    alert(666);  
</script>
~~~

## 注释

单行注释：`//`

多行注释：`/* */`

## 输入和输出

输出语句：

~~~javascript
// 1. 输出语句

//  1.1 alert 页面弹出警示框
// alert('你好,js')

// 1.2 document.write 向页面文档输入内容 显示到页面body标签之内, 可以正常的解析标签
document.write('今日特价')
document.write('<h4>今日特价</h4>')

// 1.3 console.log 给我们程序员调试使用的   console 控制台
console.log('给咱们程序员使用的')
~~~

输出语句：

向 `prompt()` 输入任意内容会以弹窗形式出现在浏览器中，一般提示用户输入一些内容。

~~~html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>JavaScript 基础 - 输入输出</title>
</head>
<body>
  
  <script> 
    // 1. 输入的任意数字，都会以弹窗形式展示
    document.write('要输出的内容')
    alert('要输出的内容');

    // 2. 以弹窗形式提示用户输入姓名，注意这里的文字使用英文的引号
    prompt('请输入您的姓名:')
  </script>
</body>
</html>
~~~

## 变量

声明(定义)变量有两部分构成：声明关键字、变量名（标识）。

~~~javascript
// 声明
let age

// 赋值
age = 18

// 更新
age = 19
~~~

在较旧的 JavaScript，使用关键字 var 来声明变量 ，而不是 let

var 现在开发中一般不再使用它，只是我们可能再老版程序中看到它。

let 为了解决 var 的一些问题。

var 声明一些不合理的地方：

1. 可以先使用，在声明 (不合理)
2. var 声明过的变量可以重复声明(不合理)
3. 比如变量提升、全局变量、没有块级作用域等等

**结论：**

> var 就是个bug，别迷恋它了，以后声明变量我们统一使用 **let** 

### 命名规则

1. 只能是字母、数字、下划线、$，且不能能数字开头
2. **字母区分大小写**，如 Age 和 age 是不同的变量
3. JavaScript 内部已占用于单词（关键字或保留字）不允许使用
4. 尽量保证变量具有一定的语义，见字知义

**规范：**

1. 起名要有意义
2. **遵守小驼峰命名法**

