## 1.8背景图片

### 1.背景颜色

background-color 属性定义了元素的背景颜色。

页面的背景颜色使用在body的选择器中:

```css
body {background-color:#b0c4de;}
```

### 2.背景图片

background-image 属性描述了元素的背景图像。

默认情况下，背景图像进行平铺重复显示，以覆盖整个元素实体。

```css
background:url(img_flwr.gif);
```

### 3.背景平铺重复设置

background-repeat属性控制背景图像的平铺重复效果。

![](/assets/pic/bg-repeat.png)

### 4.背景图片固定

在默认情况下，组件里的背景图片会随着滚动条的滚动而自动滚动，我们要把backgroun-attachment的属性设为fixed,那么背景图片就会被固定在该组件中，不会随滚动条的滚动而移动。

```css
body{background-attachment: fixed;}
```

### 5.背景图片的定位

可以利用 background-position 属性改变图像在背景中的位置。

![](/assets/pic/bg-position.png)

### 6.背景图片大小

background-size属性指定背景图片大小。

```css
div
{
    background:url(img_flwr.gif);
    background-size:80px 60px;
    background-repeat:no-repeat;
}
```

### ![](/assets/pic/bg-size.png)

### 7.背景的简写属性

为了简化这些属性的代码，我们可以将这些属性合并在同一个属性中.

背景颜色的简写属性为 "background":

当使用简写属性时，属性值的顺序为：

background-color

background-image

background-repeat

background-attachment

background-position

以上属性无需全部使用，你可以按照页面的实际需要使用.

### 8.还记得CODING COFFEE的菜单页吗，我们使用今天所学的知识，为它附上好看的背景吧。



