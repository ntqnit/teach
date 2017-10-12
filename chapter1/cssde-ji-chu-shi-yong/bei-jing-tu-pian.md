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
body {background-color:#b0c4de;}
```

### 3.背景平铺重复设置

background-repeat属性控制背景图像的平铺重复效果。

![](/assets/pic/bg-repeat.png)

### 4.背景图片固定

在默认情况下，组件里的背景图片会随着滚动条的滚动而自动滚动，我们要把backgroun-attachment的属性设为fixed,那么背景图片就会被固定在该组件中，不会随滚动条的滚动而移动。

```css
body{background-attachment: fixed;}
```





