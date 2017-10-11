## 1.6伪类

CSS伪类是添加到选择器的关键字，指定要选择的元素的特殊状态。例如，`:hover` 将在用户悬停在选择器指定的元素上时应用样式。

伪类连同伪元素一起, 他们允许你不仅仅是根据文档DOM树中的内容对元素应用样式,而且还允许你根据诸如像导航历史这样的外部因素来应用样式\(`:visited`, 为例\), 同样的,可以根据内容的状态 \(例如 在一些表单元素上的 `:checked` \), 或者鼠标的位置 \(例如`:hover`让你知道是否鼠标在一个元素上悬浮\)来应用样式.

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



