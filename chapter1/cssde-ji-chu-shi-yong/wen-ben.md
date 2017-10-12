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





