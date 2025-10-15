# HTML

## 简介

HTML 超文本标记语言 —— HyperText Markup Language。

- 超文本：链接
- 标记：标记也叫标签，带尖括号的文本



## 骨架

双标签：成对出现的标签，如 `<h1>标题<h1>`

单标签：只有开始标签，没有结束标签，如 `<hr>`



HTML 骨架

- html 整个网页
- head 网页头部
- title 网页标题
- body 网页主体

~~~html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>

</body>
</html>
~~~

## 标签关系

父子关系：`<html><body></body></html>`

兄弟关系：`<head></head><body></body>`

## 注释

~~~
<!-- 我是一行注释 -->
~~~

## 标签

### 标题 h

标签名：`h1 ~ h6`：双标签，其中 `h1` 只能用一次，用来放新闻标题或网页 Logo。

### 段落标签 p

标签名 `p`：双标签，独占一行，段落之间存在间隙。

### 换行 br

换行：`<br>`，单标签。

### 水平线 hr

水平线：`<hr>` ，单标签。

### 加粗 strong b

加粗：`<strong>、<b>`，双标签。

### 倾斜 em i

倾斜：`<em>, <i>`，双标签。

### 下划线 ins u

下划线：`<ins>, <u>`，双标签。

### 删除线 del s

删除线：`<del>, <s>`，双标签。

### 图像 img

`<img src="图片的 URL">`，属性：

- `alt`：图片无法显示时的替换文本
- `title`：鼠标悬停时显示的文本
- `width`：图片宽度，数字
- `height`：图片高度，数字

### 超链接 a

`<a href="https://www.baidu.com">跳转到百度</a>`

- `href` 属性值是跳转地址，是超链接的必须属性
- `href` 属性值写为 `#`，表示空链接，页面不会跳转，在当前页面刷新一次
- 超链接默认是在当前窗口跳转页面，添加 `target="_blank"` 实现新窗口打开页面

### 音频标签 audio 

`<audio src="音频的 URL"></audio>`

- src：必填
- controls：显示控制面板
- loop：循环播放
- autoplay：自动播放

书写 HTML5 属性时，如果属性名和属性值相同，可以简写为一个单词。

### 视频标签 video

`<video src="音频的 URL"></video >`

- src：必填
- controls：显示控制面板
- loop：循环播放
- muted：静音播放
- autoplay：自动播放

### 列表 ul ol dl

作用：布局内容排列整齐的区域。

列表分类：无序列表、有序列表、定义列表。

#### 无序列表

布局排列整齐的不需要规定顺序的区域。

~~~html
<ul>
    <li>第一项</li>
    <li>第二项</li>
    <li>第三项</li>
</ul>
~~~

注意事项：

- `ul` 标签里面只能包裹 `li` 标签
- `li` 标签里面可以包裹任何内容

#### 有序列表

作用：布局排列整齐的需要规定顺序的区域。

~~~html
<ol>
    <li>第一项</li>
    <li>第二项</li>
    <li>第三项</li>
</ol>
~~~

#### 定义列表

`dl` 嵌套 `dt` 和 `dd`

`dl` 是定义列表，`dt` 是定义列表的标题，`dd` 是定义列表的描述 / 详情。

~~~html
<dl>
    <dt>列表标题</dt>
    <dd>列表描述 / 详情</dd>
</dl>
~~~

注意事项：

- `dl` 里面只能包含 `dt` 和 `dd`
- `dt` 和 `dd` 里面可以包含任何内容

### 表格 table

网页中的表格与 Excel 表格类似，用来展示数据。

标签：`table` 嵌套 `tr`，`tr` 嵌套 `td / th`。

| 标签名  | 说明       |
| ------- | ---------- |
| `table` | 表格       |
| `tr`    | 行         |
| `th`    | 表头单元格 |
| `td`    | 内容单元格 |

提示：在网页中，表格默认没有边框线，使用 border 属性可以为表格添加边框线。

~~~html
<table border>
    <tr>
        <th>标签名</th>
        <th>说明</th>
    </tr>
    <tr>
        <td>table</td>
        <td>表格</td>
    </tr>
</table>
~~~

#### 合并单元格

- 跨行合并，保留最上单元格，添加属性 `rowspan`
- 跨列合并，保留最左单元格，添加属性 `colspan`

~~~html
<table border="1">
    <tr>
        <td rowspan="3">A</td>
        <td>B</td>
        <td rowspan="2">C</td>
    </tr>
    <tr>
        <td>D</td>
    </tr>
    <tr>
        <td>E</td>
        <td>F</td>
    </tr>
</table>
~~~

### 表单

`<input type="..." >`，其中 type:

- `text`：文本框
- `password`：密码框
- `radio`：单选框
- `checkbox`：多选框
- `file`：上传文件

#### 文本类型 text

其中，`text`、`password`：

- `placeholder`：提示信息

#### 单选 radio

`radio`：

- `name`：控件分组
- `checked`：默认选中

~~~html
<input type="radio" name="gender" checked> 男
<input type="radio" name="gender"> 女
~~~

#### 文件 file

`file`：

- `multiple`：实现文件多选功能

#### 多选 checkbox

`checkbox`：

~~~html
<label>
    <input type="checkbox" name="hobby" value="reading"> 阅读
</label>
<label>
    <input type="checkbox" name="hobby" value="sports"> 运动
</label>
<label>
    <input type="checkbox" name="hobby" value="music"> 音乐
</label>
<label>
    <input type="checkbox" name="hobby" value="travel"> 旅行
</label>
~~~

### 下拉 select option

标签：`select` 嵌套 `option`，`select` 是下拉菜单整体，`option` 是下拉菜单的每一项

- 默认显示第一项，`selected` 属性实现默认选中功能

~~~html
<select>
    <option>北京</option>
    <option>上海</option>
    <option>广州</option>
    <option>深圳</option>
    <option selected>武汉</option>
</select>
~~~

### 文本域 textarea

作用：多行输入文本的表单控件。

~~~html
<textarea>默认提示文字</textarea>
~~~

实际开发中，使用 CSS 设置 文本域的尺寸、一般禁用右下角的拖拽功能。

### 标签 label

`label`：作用：网页中，某个标签的说明文本。

经验：用 label 标签绑定文字和表单控件的关系，增大表单控件的点击范围。

~~~html
<label><input type="radio"> 女</label>
~~~

提示：支持 label 标签增大点击范围的表单控件：文本框、密码框、上传文件、单选框、多选框、下拉菜单、文本域等等。

### 按钮 button

~~~html
<button type="">按钮</button>
~~~

`type` 的属性：

- `submit`：提交
- `reset`：重置
- `button`：普通按钮，和 JS 一起用

注意：按钮需配合 form 标签（表单区域）才能实现对应的功能。

### 语义标签 div span

作用：布局网页

- `div`：独占一行
- `span`：不换行

语义布局标签

- `header`：头
- `nav`：导航
- `footer`：底
- `aside`：侧边栏
- `section`：区块
- `article`：文章

显示预留字：

- `&nbsp;`：空格
- `&lt;`：小于
- `&gt;`：大于