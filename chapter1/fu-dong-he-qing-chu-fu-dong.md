## 2.4 浮动和清除浮动

### 1.什么是浮动

我们可以用一句话描述浮动的元素的特点：**浮动元素会脱离文档流并向左/向右浮动，直到碰到父元素或者另一个浮动元素。**

```css
div{float：left/right};
```

**浮动会脱离文档流**  
脱离文档，也就是说浮动不会影响普通元素的布局。我们可以直接理解成，浮动的元素在普通文档流的上面一层，更靠近屏幕的上层。

![](/assets/pic/float1.png)

默认三个设置了宽高的`block`元素，本来会格子独占一行；如果框1设置了`float:right`，他会忽略框2和框3，直到碰到父元素；如果，框1设置成`float:left`，就会覆盖住处在普通文档流中的框2。\(框1浮动后，框1原本在普通文档流中的位置被框2顶替，而框1向左浮动后，由于处在普通文档流的上层，就会盖住框2\)。

**浮动可以内联排列**  
浮动会向左/向右浮动，直到碰到另一个浮动元素为止，这是浮动可以内联排列的特征。也就是说，浮动可以设置宽高，并且能够一行多个，是介于block和inline之间的存在。

![](/assets/pic/float2.png)

从上图可以看出，对多个元素设置浮动，可以实现类似`inline-block`的效果；但是如果每个元素的高度不一致，**会出现“卡住”的情况**。

然而，浮动也会导致一些我们不希望看见的事情发生。

**浮动会导致父元素高度坍塌**

浮动会脱离文档流，这个问题对整个页面布局有很大的影响。

```html
.box-wrapper { border: 5px solid red; } 
.box-wrapper .box { float: left; width: 100px; height: 100px; margin: 20px; background-color: green; } 
 <div class="box-wrapper"> 
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div> 
 </div>
```

结果如下，浮动元素脱离了文档流，并不占据文档流的位置，自然父元素也就不能被撑开，所以没了高度。

![](/assets/pic/float3.png)

很明显，这样的效果并不符合我们的预期，所以我们需要想办法解决这个问题。现在，我们需要清除浮动！

### 2.如何清除浮动

**清除浮动**  
清除浮动的底层原理是在被清除浮动的元素上边或者下边添加足够的清除空间。  
要注意了，**我们是通过在别的元素上清除浮动来实现撑开高度的， 而不是在浮动元素上。**  
还是接着上面的例子，我们简单修改一下HTML代码：

```html
 <div class="box-wrapper">
     <div class="box"></div>
     <div class="box"></div>
     <div class="box"></div>
     <div style="clear:both;"></div>
 </div>
```

![](/assets/pic/float4.png)

哈哈，好像问题解决了！但是要注意的是，我们是在原来的页面中添加了一个空的div元素，并且增加样式`clear:both`，不可以在已经浮动的元素中增加清除浮动的样式，这样只会让其不去进行位置浮动，但是仍然是脱离文档流的，依然不能撑开高度。如下图：

![](/assets/pic/float5.png)

**清除浮动的最佳实践**

```css
.clearfix:after {content:""; display:block; height:0; visibility:hidden; clear:both; }

.clearfix { *zoom:1; }
```

1\)` display:block `使生成的元素以块级元素显示,占满剩余空间。

2\) `height:0` 避免生成内容破坏原有布局的高度。

3\) `visibility:hidden` 使生成的内容不可见，并允许可能被生成内容盖住的内容可以进行点击和交互。

4）通过` content:"."`生成内容作为最后一个元素，至于content里面是点还是其他都是可以的。

5）`zoom：1 `触发IE hasLayout。

通过分析发现，除了`clear：both`用来闭合浮动的，其他代码无非都是为了隐藏掉content生成的内容。

**触发BFC**

BFC全称是块状格式化上下文，它是按照块级盒子布局的。我们了解他的特征、触发方式、常见使用场景这些就够了。

**BFC的主要特征**

✦ BFC容器是一个隔离的容器，和其他元素互不干扰；所以我们可以用触发两个元素的BFC来解决垂直边距折叠问题。  
✦ BFC可以包含浮动；通常用来解决浮动父元素高度坍塌的问题。

其中，BFC清除浮动就是用的“包含浮动”这条特性。  
那么，怎样才能触发BFC呢？

**BFC的触发方式**

我们可以给父元素添加以下属性来触发BFC：  
✦ `float` 为 `left` \| `right`  
✦ `overflow` 为 `hidden` \| `auto` \| `scorll`  
✦ `display` 为 `table-cell` \| `table-caption` \| `inline-block` \| `flex` \| `inline-flex`  
✦ `position` 为 `absolute` \| `fixed`

所以我们可以给父元素设置`overflow:auto`来简单的实现BFC清除浮动，但是为了兼容IE最好用`overflow:hidden`。但是这样元素阴影或下拉菜单会被截断，比较局限。所以以上的BFC触发方法都可以用来解决浮动问题，但是要选择合适的使用场景。

### 3.总结

有很多方法可以进行清除浮动这样的操作，归根到底，从原理上讲其实分为两种。

其一，通过在浮动元素的末尾添加一个空元素，设置 clear：both属性。（after伪元素其实也是通过 content 在元素的后面生成了内容为一个点的块级元素）；

其二，使父元素触发BFC。（通过设置父元素 overflow 或者display：table 属性来闭合浮动）

