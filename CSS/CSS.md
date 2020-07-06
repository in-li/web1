# CSS

+ id选择器

```html
<div id="one"></div>
```
```css
#one{

}
```

+ class类选择器

```html
<div class="one"></div>
```
```css
.one{

}
```

+ 标签选择器

```css
span{} 
div{}
所有 span div 都有效果 
```

+ 通配符选择器

```css
* {} 所有标签都有效果
```

+ 属性选择器

```css
[id 或者 id=“”]{

}
```

+ 优先级

!important > 行间样式 > id > class|属性选择器 > 标签选择器 > 通配符选择器

+ css权重

```
！important     infinity
行间样式          1000    256进制
id                100
class|属性|伪类    10
标签                1
通配符              0 
```

+ 父子选择器

```html
<div>
<span>123</span>
<div>
<span>456</span>
```
```css
让123样式改变 div span{

}
```

+ 直接子元素选择器

```css
div > em {

}div下直接子元素em
```

+ 并列选择器

```html
<div class="one">1</div>
```
```css
div.one{

}
```

+ css基础属性

```css
font-size:12px; 字体大小

font-weight:bold bolder 100 200; 字体加粗 和<strong></strong>效果一样

font-style:italic(斜体) 字体样式

font-family:arial;  字体

color:字体颜色 1. green 颜色英语单词 2. #ff4400 颜色代码  3. 颜色函数 r:red g:green: b:blue rgb()

border:1px solid black; 边框
border:border-width border-style:solid 实线 dashed 虚线   

width： px;高

heght:  px;宽
```