## 2.2盒子模型内外边距和边框介绍

![](/assets/pic/box-border2.png)

### 1.边框

用 border 属性给元素四周指定统一的边框。在属性值中指定边框的宽度（通常是以显示到屏幕上的像素为单位）， 样式， 还有颜色。

样式包括：

![](/assets/pic/border.png)

你也可以通过设置样式为 `none` 或 `hidden` 来明确地移除边框，或者设置边框颜色为 `transparent` 来让边框不可见，后者不会改变布局。

如果一次只指定某一个方向的边框，就用属性：`border-top，border-right， border-bottom，border-left`。 你可以用这些属性指定某个方向上的边框，或者不同方向上的不同边框。

下面的规则设置了一个标题元素的背景色和顶部边框：

```css
h3 {
  border-top: 4px solid #7c7; /* 中绿 */
  background-color: #efe;     /* 浅绿 */
  color: #050;                /* 深绿 */
  }
```

结果如下：  
![](/assets/pic/border-result.png)

### 2.外边距和内边距

使用外边距和内边距调整元素的位置，并在其周围创建空间。

用`margin`属性或者 `padding` 属性分别设置外边距和内边距的宽度。

如果你指定一个宽度，它将会作用于元素四周（上、右、下、左）。

如果你指定两个宽度， 第一个宽度会作用于顶部和底部，第二个宽度作用于右边和左边。

你也可以按照顺序指定四个宽度： 上、右、下、左。

下面的规则通过给元素四周设置红色边框，标记出了类名为  `remark` 的段落元素。

文本周围的内边距将边框与文字拉开一点距离。

左外边距使得段落相对于其余文本产生缩进：

```css
p.remark {
  border: 2px solid red;
  padding: 4px;
  margin-left: 24px;
  }
```

结果如下：  
![](/assets/pic/border-margin.png)

> 注意：外边距margin可以为负。



