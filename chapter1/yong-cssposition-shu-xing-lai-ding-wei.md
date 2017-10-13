## 2.5 CSS position属性

CSS 有三种基本的定位机制：普通流、浮动和绝对定位。  
我们已经学习了普通流和浮动的相关内容，本节我们介绍定位相关内容。

position属性设置元素定位类型，可以通过top,bottom,right,left属性，控制元素的定位位置。  
position属性值有static，relative，absolute，fixed四个值。

###1.static静态定位

HTML元素的默认值，即没有定位，元素出现在正常的流中。
静态定位的元素不会受到top,bottom,right,left属性的影响。

###2.fixed固定定位
* 脱离标准流，在页面中不占位置 。
* 不管页面有多大，永远相对于浏览器的边框来定位 。

```css
    *{
            margin: 0;
            padding: 0;
        }
        .c1{
            width: 100px;
            height: 100px;
            background-color: brown;
        }

        .c2{
            width: 100px;
            height: 100px;
            background-color: blue;
        }

        .c3{
            width: 100px;
            height: 100px;
            background-color: black;
            position: fixed;/*固定定位，不占位置，永远相对于浏览器来定位，不管窗口上下拉动，都不会消失（如广告位）*/
            left:20px;
            top:20px;
        }
```

```html
<body>
         <div class="c1"></div>
         <div class="c2"></div>
         <div class="c3"></div>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>...
</body>
```
###3.relative 相对定位
* 不脱离标准流，在页面中占位置 。
* 相对于自己原来的位置来进行定位 。
```css
     *{
            margin: 0;
            padding: 0;
        }
        .c1{
            width: 100px;
            height: 100px;
            background-color: brown;
        }

        .c2{
            width: 100px;
            height: 100px;
            background-color: blue;
            position: relative;/*相对定位，占位置，相对于自己原来的位置定位*/
            left: 20px;
            top:20px;
        }

        .c3{
            width: 100px;
            height: 100px;
            background-color: black;
        }
```
```html
<body>
    <div class="c1"></div>
    <div class="c2"></div>
    <div class="c3"></div>
</body>
```


