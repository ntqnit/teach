## 1.10 CSS列表

CSS列表属性作用如下：

* 设置不同的列表项标记为有序列表。
* 设置不同的列表项标记为无序列表。
* 设置列表项标记为图像。

### 1.使用不同的列表项标记

使用list-style-type改变列表项标记。

```css
<style>
ul.a {list-style-type:circle;}
ul.b {list-style-type:square;}
ol.c {list-style-type:upper-roman;}
ol.d {list-style-type:lower-alpha;}
</style>
```

```html
<ul class="a">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Coca Cola</li>
</ul>
<ul class="b">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Coca Cola</li>
</ul>
<p>有序列表实例:</p>
<ol class="c">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Coca Cola</li>
</ol>
<ol class="d">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Coca Cola</li>
</ol>
```

### 2.使用图片作为列表项

使用list-style-image可以用图片作为列表的标记项。

```css
<style>
	ul 
	{
		list-style-image:url('sqpurple.gif');
	}
</style>
```

```html
<ul>
<li>Coffee</li>
<li>Tea</li>
<li>Coca Cola</li>
</ul>
```



