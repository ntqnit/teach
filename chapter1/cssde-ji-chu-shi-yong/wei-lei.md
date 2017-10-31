## 1.6 伪类

CSS伪类是添加到选择器的关键字，指定要选择的元素的特殊状态。例如，`:hover` 将在用户悬停在选择器指定的元素上时应用样式。

### 1.anchor伪类

链接的不同状态都可以以不同的方式显示。

```html
<style>
a:link {color:#000000;}    /* 未访问链接*/
a:visited {color:#00FF00;}  /* 已访问链接 */
a:hover {color:#FF00FF;}  /* 鼠标移动到链接上 */
a:active {color:#0000FF;}  /* 鼠标点击时 */
</style>
<body>
<p><b><a href="/css/" target="_blank">这是一个链接</a></b></p>
<p><b>注意：</b> a:hover 必须在 a:link 和 a:visited 之后，需要严格按顺序才能看到效果。</p>
<p><b>注意：</b> a:active 必须在 a:hover 之后。</p>
</body>
```

> 注意：在CSS定义中，a:hover必须被置于a:link和a:visited之后，a:active必须被置于  
> a:hover之后，才是有效的。伪类的名称不区分大小写。

### 2.first-child伪类

:first-child CSS 伪类代表了一组兄弟元素中的第一个元素。被匹配的元素需要具有一个父级元素。

```css
element:first-child { style properties }
```

上面的CSS作用于下面的HTML:

```css
span:first-child {
    background-color: lime;
}
```

```html
<div>
  <span>This span is limed!</span>
  <span>This span is not. :(</span>
</div>
```

![](/assets/pic/first-child.png)

### 3.first-line伪类

"first-line" 伪元素用于向文本的首行设置特殊样式。

在下面的例子中，浏览器会根据 "first-line" 伪元素中的样式对p元素的第一行文本进行格式化：

```html
<style>
p:first-line {
   color:red;
    }
</style>
<body>
<p>A smooth, mild blend of coffees from Mexico, A smooth, mild blend of coffees from Mexico,A smooth, mild blend of coffees from Mexico,A smooth, mild blend of coffees from Mexico,A smooth, mild blend of coffees from Mexico,A smooth, mild blend of coffees from Mexico,A smooth, mild blend of coffees from Mexico,A smooth, mild blend of coffees from Mexico,A smooth, mild blend of coffees from Mexico,A smooth, mild blend of coffees from Mexico,A smooth, mild blend of coffees from Mexico,A smooth, mild blend of coffees from Mexico,A smooth, mild blend of coffees from Mexico,A smooth, mild blend of coffees from Mexico,</p>
</body>
```

> 注意："first-line" 伪元素只能用于块级元素。

下面的属性可应用于 "first-line" 伪元素：

> font properties
>
> color properties
>
> background properties
>
> word-spacing
>
> letter-spacing
>
> text-decoration
>
> vertical-align
>
> text-transform
>
> line-height
>
> clear

### 4.:before伪类

":before" 伪元素可以在元素的内容前面插入新内容。

下面的例子在每个&lt;h1&gt;元素前面插入一幅图片：

```html
<style>
p:before
{ 
content:"台词：-";
background-color:yellow;
color:red;
font-weight:bold;
}
</style>
<body>
    <p>The :before pseudo-element inserts content before an element.</p>
    <p><b>注意:</b>仅当 !DOCTYPE 已经声明 IE8 支持这个内容属性</p>
</body>
```

> 大家应该想到了，既然有:before伪类，自然就有:after伪类，大家可以自行学习。
>
> 在css中实际上提供了非常多的伪类可以使用，我们指数选择了一些常用的进行介绍，其他伪类的学习，需要大家自主学习。



