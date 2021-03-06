## 1.5 选择器

> 装修队CSS已经进场了，但是我们要小心控制装修队，可不能让装修队在家里胡作非为。  
> 所以我们要使用选择器精准的选择网页中需要装修的地方。

### 1.通配符选择器

使用"\*"表示通配符，用来选择页面所有元素的样式。

```css
*{ margin:0;
   padding:0;}
```

### 2.类选择器

类选择器指定的样式对指定class属性的元素起作用。使用“.”标识一个类选择符，类名可以任意。

```css
.myclass{...}
```

### 3.ID选择器

ID选择器中的样式会对具有指定id属性的HTML元素起作用。

HTML元素以id属性来设置id选择器,CSS中id选择器以"\#"来定义。

> 需要注意的是id在HTML文档中具有唯一性，是不可以重复的。

```css
#idValue{ ...}
```

### 4.包含选择器

包涵选择器用于指定处于某个选择器对应的内部元素。

```css
h1 em {color:red;}
```

### 5.子选择器

子选择器要求目标选择器必须作为外部选择器对应的元素的直接子元素**。**

```css
parent>child{width: 200px; height: 35px;}
```

```html
<style>

</style>
<div class="a">
        <p>A smooth, mild <span class="b">blend of coffees</span> from Mexico, </p>
        <div>A smooth, <p>mild</p>mild</div>
</div>
```

### 6.群组选择器

群组选择器使用逗号对选择符进行分隔。

> 我们可以将逗号读成“和”。

```css
h1,p,myClass,#main{
    font-size:20px;
}
```



