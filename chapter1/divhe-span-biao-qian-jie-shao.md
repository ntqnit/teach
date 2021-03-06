### 1.2 DIV和SPAN标签简介

我们在之前的练习中发现，HTML标签具有不同的特性。

实际上，我们可以将HTML元素分为两大类：区块元素和内联元素。

### 1.内联元素和区块元素

**区块元素**

* 总是在新的一行上显示。

* 高度、行高、宽度、内边距、外边距等都是可控制的。

* 高度默认为0，是根据元素内的内容而决定的，宽度是父元素的宽度，但是可以通过css控制它，显示的指定他的宽度和高度，可以利用浮动和定位来将他与其他的块元素也显示在一行上。

* 实例: &lt;h1&gt;, &lt;p&gt;, &lt;ul&gt;, &lt;table&gt;。

**内联元素**

* 内联元素和其他的元素显示在一行上。

* **上下边距**、高度，宽度都是不可改变的，他的宽度是根据他的显示文本和图像的宽度。

* 实例: &lt;b&gt;, &lt;td&gt;, &lt;a&gt;, &lt;img&gt;。

![](/assets/pic/08-1-3-1.png)![](/assets/pic/08-1-3-2.png)

### 1.**&lt;div&gt;元素**

* HTML &lt;div&gt;元素是块级元素，它可用于组合其他HTML元素的容器。

* &lt;div&gt;元素没有特定的含义。由于它属于块级元素，浏览器会在其前后显示换行。

* 如果与 CSS 一同使用，&lt;div&gt;元素可用于对大的内容块设置样式属性。

![](/assets/pic/08-1-3-3.png)

```html
<title>三列布局</title>
<style>
    body{ margin:0; padding:0; font-size:30px; font-weight:bold}
    div{ text-align:center; line-height:50px}
    .left{ width:240px; height:600px; background:#ccc; position:absolute; left:0; top:0}
    .main{ height:600px; margin:0 240px; background:#9CF}
    .right{ height:600px; width:240px; position:absolute; top:0; right:0; background:#FCC;}
</style>
</head>
<body>
    <div class="left">left</div>
    <div class="main">main</div>
    <div class="right">right</div>
</body>
```

### 2**. &lt;span&gt;元素**

* HTML &lt;span&gt;元素是内联元素，可用作文本的容器
* &lt;span&gt;元素也没有特定的含义。
* 当与 CSS 一同使用时，&lt;span&gt;元素可用于为部分文本设置样式属性。



