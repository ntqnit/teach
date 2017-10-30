## 1.3 CSS样式规则和CSS加载的方式

### 1.CSS样式规则

CSS 规则由两个主要的部分构成：选择器，以及一条或多条声明:

![](http://www.runoob.com/images/selector.gif)

选择器通常是您需要改变样式的 HTML 元素。

每条声明由一个属性和一个值组成。

属性（property）是您希望设置的样式属性（style attribute）。

每个属性有一个值。

属性和值被冒号分开。

### 2. CSS加载的方式

**1.引入外部文件**

```html
<link href="outer.css" rel="stylesheet" type="text/css"></link>
```

HTML文档中使用&lt;link&gt;元素引入外部样式文件，引入外部样式文件应在&lt;head&gt;元素中增加&lt;link&gt;子元素。&lt;link&gt;元素的href属性值是外部CSS文件的地址，可以使本地的CSS文件，也可以引入远程服务器上的CSS资源。

**2.导入外部样式单**

```html
<style type="text/css">
    @import "../outer.css";
    @import url('outer.css');
</style>
```

导入外部样式表单需要在&lt;style&gt;元素中执行@import进行导入。

**3.使用内部CSS样式**

一般来说我们不建议使用内部CSS样式：

* 复用性小。
* 导致HTML文档过大，会导致网络负载严重。
* 修改整站风格时，需要对每个网页文件进行样式修改。

```html
<style type="text/css">
样式单文件定义
</style>
```

**4.使用内联CSS样式**

内联样式只对单个标签有效，不会影响整个文件。

在HTML元素中使用style属性定义内联样式。

```html
<div style="property1:value1;property2:value2;"/>
```



