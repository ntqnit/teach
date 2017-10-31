## 1.9 文本

### 1.文本的颜色

颜色属性被用来设置文字的颜色。

颜色是通过CSS最经常的指定：

* 十六进制值 - 如:＃FF0000。
* 一个RGB值-如:RGB\(255,0,0\)。
* 颜色的名称 - 如:red。

```css
body {color:red;} 
h1 {color:#00ff00;} 
h2 {color:rgb(255,0,0);}
```

### 2.文本的水平对齐方式

文本排列属性是用来设置文本的水平对齐方式。

文本可居中或对齐到左或右,两端对齐.

当text-align设置为"justify"，每一行被展开为宽度相等，左，右外边距是对齐（如杂志和报纸）。

![](/assets/pic/text-align.png)

```html
    <style>
        p {
            text-align: justify;
        }
    </style>

    <body>
        <p>Be careful to perform the actions in the correct sequence.</p>    
    </body>
```

### 3.文本修饰

text-decoration属性一般用于删除链接的下划线。

```html
<style>
    a {
    text-decoration:none;
    }
</style>

<body>
    <a href="#">百度</a>
</body>
```

### 4.文本转换

文本转换属性是用来指定在一个文本中的大写和小写字母。

可用于所有字句变成大写或小写字母，或每个单词的首字母大写。

```html
<style>
    .uppercase {
        text-transform:uppercase;
        }
    .lowercase {
        text-transform:lowercase;
        }
            /* 首字母大写 */
    .capitalize {
        text-transform:capitalize;
        }
</style>
<body>
    <p class="uppercase">Hello,World!</p>
    <p class="lowercase">Hello,World!</p>
    <p class="capitalize">hello,world!</p>
</body>
```

### 5.文本缩进

text-indent属性控制**首行文本**的缩进。

属性值可以是固定值（包括负数），也可是百分比。

> 注意em单位一般代表网页中一个字符的大小。

```html
<style>
    p {
    text-indent:2em;
    }
</style>

<p>
        南通青鸟教育集团成立于2006年2月，学校秉承“学习改变命运、实训提升实力”的理念，以就业为导向，强势发展校企合作、
        定向培养，借助南通和长三角地区软件和服务外包兴旺发达的产业优势，累计为南通、上海、南京等城市培养和输送专业人才6000余人。
</p>
```

### 6.字符间距和字间距

* letter-spacing属性控制字符的间距。属性值可以是正负数。

* word-spacing属性控制字间距。

我们在这里设置CODING COFFEE的产品页和首页。

```css
p{
    word-spacing: 5px;
    letter-spacing: 5px;
 }
```

### 7.行间距

line-height属性控制行间距（简称行高）。

```html
<style>
    p.small {
        line-height:10px;
        }
    p.big{
        line-height:30px;
        }
</style>

<p>
In object-oriented terminology, a class is a term that describes a group or collection of objects with common properties.
</p>
<p class="small">
In object-oriented terminology, a class is a term that describes a group or collection of objects with common properties.
</p>
<p class="big">
In object-oriented terminology, a class is a term that describes a group or collection of objects with common properties. 
</p>
```

### 8.元素的垂直对齐方式

vertical-align属性控制元素垂直对齐方式。

**vertical-align被用于垂直对齐inline元素，也就是display值为inline和inline-block的元素。**

> todo 未完成



