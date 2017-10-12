## 1.7 CSS颜色

颜色是由红（RED），绿（GREEN），蓝（BLUE ）光线的显示结合。

CSS的颜色可以通过以下等方法指定：十六进制颜色、RGB颜色、RGBA颜色、颜色名等值指定。



所有主要浏览器都支持十六进制颜色值。

指定一个十六进制的颜色其组成部分是：＃RRGGBB，其中RR（红色），GG（绿色）和BB（蓝色）。所有值必须介于0和FF之间。

例如，＃0000FF值呈现为蓝色，因为蓝色的组成设置为最高值（FF）而其他设置为0。

```css
p
{
background-color:#ff0000;
}
```



RGB颜色值在所有主要浏览器都支持。

RGB颜色值指定：RGB（红，绿，蓝）。每个参数（红色，绿色和蓝色）定义颜色的亮度，可在0和255之间，或一个百分比值（从0％到100％）之间的整数。

例如RGB（0,0,255）值呈现为蓝色，因为蓝色的参数设置为最高值（255）而其他设置为0。

此外，下面的值定义相同的颜色：RGB（0,0,255），RGB（0％，0％，100％）。

```css
p
{
background-color:rgb(255,0,0);
}
```



RGBA颜色值被IE9, Firefox3+, Chrome, Safari,和Opera10+支持。

RGBA颜色值是RGB颜色值alpha通道的延伸 - 指定对象的透明度。

RGBA颜色值指定：RGBA（红，绿，蓝，alpha）。 Alpha参数是一个介于0.0（完全透明）和1.0（完全不透明）之间的参数。

```css
p
{
background-color:rgba(255,0,0,0.5);
}
```




