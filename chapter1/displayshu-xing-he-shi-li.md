## 2.3 display属性和实例

### 1.元素的显示和隐藏

* 使用`display:none`将元素隐藏起来，此时元素不占用页面空间。
* 使用`display:hidden`也可以隐藏元素，此时元素不占用空间

### 2.通过display改变内联元素或块级元素

\(1\)**display:block就是将元素显示为块级元素**.

**block元素的特点是：**

总是在新行上开始；

高度，行高以及顶和底边距都可控制；

宽度缺省是它的容器的100%，除非设定一个宽度

&lt;div&gt;, &lt;p&gt;, &lt;h1&gt;, &lt;form&gt;, &lt;ul&gt; 和 &lt;li&gt;是块元素的例子。

**\(2\)display:inline就是将元素显示为行内元素.**

**inline元素的特点是：**

和其他元素都在一行上；

高，行高及顶和底外边距不可改变；

宽度就是它的文字或图片的宽度，不可改变。

&lt;span&gt;, &lt;a&gt;, &lt;label&gt;, &lt;input&gt;, &lt;img&gt;, &lt;strong&gt; 和&lt;em&gt;是inline元素的例子。

3.**display:inline-block将对象呈递为内联对象，但是对象的内容作为块对象呈递。旁边的内联对象会被呈递在同一行内，允许空格。\(准确地说，应用此特性的元素呈现为内联对象，周围元素保持在同一行，但可以设置宽度和高度地块元素的属性\)**

### 3.案例

我们现在有一个竖直导航栏，代码如下：

```css
    <style type="text/css">
        ul{
            list-style-type:none; 
            margin: 0;
            padding: 0;
            background-color:#333;
        }

        li a{
            text-decoration: none;
            display: block;
            padding:15px 18px;
            color: white;
        }
        .clear{
            clear: both;
        }
        li a:hover{
            background-color: #ccc;
        }
    </style>
```

```html
        <ul>
            <li>
                <a class="def" href="">主页</a>
            </li>
            <li>
                <a href="">公司简介</a>
            </li>
            <li>
                <a href="">合作案例</a>
            </li>
            <li>
                <a href="">核心技术</a>
            </li>
            <div class="clear"></div>
        </ul>
```



