## 2.2盒子模型内外边距和边框介绍

### 1.边框

用 border 属性给元素四周指定统一的边框。在属性值中指定边框的宽度（通常是以显示到屏幕上的像素为单位）， 样式， 还有颜色。

样式包括：

![](/assets/pic/border.png)

你也可以通过设置样式为 `none` 或 `hidden` 来明确地移除边框，或者设置边框颜色为 `transparent` 来让边框不可见，后者不会改变布局。

如果一次只指定某一个方向的边框，就用属性： border-top，border-right， [`border-bottom`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/border-bottom)， [`border-left`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/border-left)。 你可以用这些属性指定某个方向上的边框，或者不同方向上的不同边框。

