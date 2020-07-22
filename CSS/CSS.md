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

height:  px;宽

text-align: center right left; 对齐方式

line-height:  px;单行文本高度 

text-indent:2em;首行缩进

text-decoration:underline line-through;元素的文本修饰

cursor: pointer(手形)  显示的光标的类型（形状）

hover 鼠标指针浮动在其上的元素

```

## 动画

+ @keyframes

```css
规定动画。
from等价于 0%。
to等价于 100%。
```
+ animation

```css
所有动画属性的简写属性，除了 animation-play-state 属性。
CSS animation 属性是 animation-name，animation-duration, animation-timing-function，animation-delay，animation-iteration-count，animation-direction，animation-fill-mode 和 animation-play-state 属性的一个简写属性形式。
```
+ animation-name

```css
animation-name 规定 @keyframes 动画的名称。

值：

none
特殊关键字，表示无关键帧。可以不改变其他标识符的顺序而使动画失效，或者使层叠的动画样式失效。

IDENT
标识动画的字符串，由大小写敏感的字母a-z、数字0-9、下划线(_)和/或横线(-)组成。第一个非横线字符必须是字母，数字不能在字母前面，不允许两个横线出现在开始位置。
```
+ animation-duration

```css
animation-duration 规定动画完成一个周期所花费的秒或毫秒。

值

<time>
一个动画周期的时长，单位为秒(s)或者毫秒(ms)，无单位值无效。
```
+ animation-timing-function

```css
animation-timing-function属性定义CSS动画在每一动画周期中执行的节奏。可能值为一或多个 <timing-function>。对于关键帧动画来说，timing function作用于一个关键帧周期而非整个动画周期，即从关键帧开始开始，到关键帧结束结束。

值

<timingfunction>
每个 <timing-function>代表了应用于动画的timing function，定义于animation-property.
```
+ animation-delay

```css
animation-delay CSS属性定义动画于何时开始，即从动画应用在元素上到动画开始的这段时间的长度。0s是该属性的默认值，代表动画在应用到元素上后立即开始执行。否则，该属性的值代表动画样式应用到元素上后到开始执行前的时间长度；定义一个负值会让动画立即开始。但是动画会从它的动画序列中某位置开始。例如，如果设定值为-1s，动画会从它的动画序列的第1秒位置处立即开始。
如果为动画延迟指定了一个负值，但起始值是隐藏的，则从动画应用于元素的那一刻起就获取起始值。

值

<time>
从动画样式应用到元素上到元素开始执行动画的时间差。该值可用单位为秒(s)和毫秒(ms)。如果未设置单位，定义无效。
```
+ animation-iteration-count

```css
animation-iteration-count  CSS 属性   定义动画在结束前运行的次数 可以是1次 无限循环，如果指定了多个值，每次播放动画时，将使用列表中的下一个值，在使用最后一个值后循环回第一个值。

值

infinite
无限循环播放动画.

<number>
动画播放的次数；默认值为1。可以用小数定义循环，来播放动画周期的一部分：例如，0.5 将播放到动画周期的一半。不可为负值。
```
+ animation-direction

```css
animation-direction CSS 属性指示动画是否反向播放，它通常在简写属性animation中设定

值

normal
每个循环内动画向前循环，换言之，每个动画循环结束，动画重置到起点重新开始，这是默认属性。

alternate
动画交替反向运行，反向运行时，动画按步后退，同时，带时间功能的函数也反向，比如，ease-in 在反向时成为ease-out。计数取决于开始时是奇数迭代还是偶数迭代

reverse
反向运行动画，每周期结束动画由尾到头运行。

alternate-reverse
反向交替， 反向开始交替
动画第一次运行时是反向的，然后下一次是正向，后面依次循环。决定奇数次或偶数次的计数从1开始。
```
+ animation-fill-mode

```css
animation-fill-mode 设置CSS动画在执行之前和之后如何将样式应用于其目标。

值

none
当动画未执行时，动画将不会将任何样式应用于目标，而是已经赋予给该元素的 CSS 规则来显示该元素。这是默认值。

forwards
目标将保留由执行期间遇到的最后一个关键帧计算值。 最后一个关键帧取决于animation-direction和animation-iteration-count的值：
animation-direction	animation-iteration-count last keyframe encountered
normal	           even or odd	     100% or to
reverse	           even or odd	     0% or from
alternate	       even	             0% or from
alternate	       odd	             100% or to
alternate-reverse  even	             100% or to
alternate-reverse  odd	             0% or from

backwards
动画将在应用于目标时立即应用第一个关键帧中定义的值，并在animation-delay期间保留此值。 第一个关键帧取决于animation-direction的值：
animation-direction	            first relevant keyframe
normal or alternate	            0% or from
reverse or alternate-reverse	100% or to

both
动画将遵循forwards和backwards的规则，从而在两个方向上扩展动画属性。
```
+ animation-play-state

```css
animation-play-state 属性定义一个动画是否运行或者暂停。可以通过查询它来确定动画是否正在运行。另外，它的值可以被设置为暂停和恢复的动画的重放。恢复一个已暂停的动画，将从它开始暂停的时候，而不是从动画序列的起点开始在动画。

值

running
当前动画正在运行。

paused
当前动画已被停止。
```

## 背景

+ background-color

```css
CSS属性中的 background-color 会设置元素的背景色, 属性的值为颜色值或关键字"transparent"二者选其一.

值

<color>
一个描述背景统一颜色的 CSS <color> 值。即使一个或几个的 background-image 被定义，如果图像是不透明的，通过透明度该颜色也能影响到渲染。在 CSS 中，transparent 是一种颜色。
```

+ background-image

```css
CSS background-image 属性用于为一个元素设置一个或者多个背景图像。

语法

每个背景图像被明确规定为关键字 none 或是一个 <image> 值。

可以提供由逗号分隔的多个值来指定多个背景图像：

background-image:
  linear-gradient(to bottom, rgba(255,255,0,0.5), rgba(0,0,255,0.5)),
  url('https://mdn.mozillademos.org/files/7693/catfront.png');

值

none
是一个表示无背景图的关键字。

<image>
<image> 用来标记将要显示的图片. 支持多背景设置，背景之间以逗号隔开.
```

+ background-repeat

```css
 background-repeat CSS 属性定义背景图像的重复方式。背景图像可以沿着水平轴，垂直轴，两个轴重复，或者根本不重复。

 语法

/* 单值语法 */
background-repeat: repeat-x;
background-repeat: repeat-y;
background-repeat: repeat;
background-repeat: space;
background-repeat: round;
background-repeat: no-repeat;

/* 双值语法: 水平horizontal | 垂直vertical */
background-repeat: repeat space;
background-repeat: repeat repeat;
background-repeat: round space;
background-repeat: no-repeat round;

background-repeat: inherit;

值

repeat	
图像会按需重复来覆盖整个背景图片所在的区域. 最后一个图像会被裁剪, 如果它的大小不合适的话.

space	
图像会尽可能得重复, 但是不会裁剪. 第一个和最后一个图像会被固定在元素(element)的相应的边上, 同时空白会均匀地分布在图像之间. background-position属性会被忽视, 除非只有一个图像能被无裁剪地显示. 只在一种情况下裁剪会发生, 那就是图像太大了以至于没有足够的空间来完整显示一个图像.

round	
随着允许的空间在尺寸上的增长, 被重复的图像将会伸展(没有空隙), 直到有足够的空间来添加一个图像. 当下一个图像被添加后, 所有的当前的图像会被压缩来腾出空间. 例如, 一个图像原始大小是260px, 重复三次之后, 可能会被伸展到300px, 直到另一个图像被加进来. 这样他们就可能被压缩到225px.

译者注: 关键是浏览器怎么计算什么时候应该添加一个图像进来, 而不是继续伸展.

no-repeat	
图像不会被重复(因为背景图像所在的区域将可能没有完全被覆盖). 那个没有被重复的背景图像的位置是由background-position属性来决定.
```

+ background-position

```css
background-position 为每一个背景图片设置初始位置。 这个位置是相对于由 background-origin 定义的位置图层的。

语法

/* Keyword values */
background-position: top;
background-position: bottom;
background-position: left;
background-position: right;
background-position: center;

/* <percentage> values */
background-position: 25% 75%;

/* <length> values */
background-position: 0 0;
background-position: 1cm 2cm;
background-position: 10ch 8em;

/* Multiple images */
background-position: 0 0, center;

/* Edge offsets values */
background-position: bottom 10px right 20px;
background-position: right 3em bottom 10px;
background-position: bottom 10px right;
background-position: top right 10px;

/* Global values */
background-position: inherit;
background-position: initial;
background-position: unset; 

值

关键字 center，用来居中背景图片。
关键字 top, left, bottom, right 中的一个。用来指定把这个项目（原文为 item）放在哪一个边缘。另一个维度被设置成 50%，所以这个项目（原文为 item）被放在指定边缘的中间位置。
<length> 或 <percentage>。指定相对于左边缘的 x 坐标，y 坐标被设置成 50%。
如果一个值是  top 或  bottom，那么另一个值不应该是 top 或 bottom。
如果一个值是  left 或   right，那么另一个值不应该是 left 或 right 。
+50px（将图片的左边界对齐容器的中线）
0px（图片的左边界与容器左边界重合）
-100px（将图片相对容器左移100px，这意味着图片中部的100px内容将出现在容器中）
-200px（将图片相对容器左移200px，这意味着图片右部分的100px内容将出现在容器中）
-250px（将图片相对容器左移250px，这意味着图片的右边界对齐容器的中线）
    另外需要注意，如果背景图片的大小和容器一样，那设置百分比的值将永远无效，因为“容器和图片的差”为0（图片永远填满容器，并且图片的相对位置和容器的相对位置永远重合）。在这种情况下，需要为偏移使用绝对值（例如px）。
```

+ background-attachment

```css
background-attachment CSS 属性决定背景图像的位置是在视口内固定，或者随着包含它的区块滚动。

值

fixed
此关键属性值表示背景相对于视口固定。即使一个元素拥有滚动机制，背景也不会随着元素的内容滚动。
local
此关键属性值表示背景相对于元素的内容固定。如果一个元素拥有滚动机制，背景将会随着元素的内容滚动， 并且背景的绘制区域和定位区域是相对于可滚动的区域而不是包含他们的边框。
scroll
此关键属性值表示背景相对于元素本身固定， 而不是随着它的内容滚动（对元素边框是有效的）。
```

+ background-size

```css
background-size 设置背景图片大小。图片可以保有其原有的尺寸，或者拉伸到新的尺寸，或者在保持其原有比例的同时缩放到元素的可用空间的尺寸。

值

单张图片的背景大小可以使用以下三种方法中的一种来规定：
使用关键词 contain
使用关键词 cover
设定宽度和高度值
```

+ background-clip

```css
background-clip  设置元素的背景（背景图片或颜色）是否延伸到边框、内边距盒子、内容盒子下面。

值

border-box
背景延伸至边框外沿（但是在边框下层）。
padding-box
背景延伸至内边距（padding）外沿。不会绘制到边框处。
content-box
背景被裁剪至内容区（content box）外沿。
text 
背景被裁剪成文字的前景色。
```

+ background-origin

```css
background-origin 规定了指定背景图片background-image 属性的原点位置的背景相对区域.

值

border-box
背景图片的摆放以border区域为参考
padding-box
背景图片的摆放以padding区域为参考
content-box
背景图片的摆放以content区域为参考
```

##  position

```css
position 属性值的含义：
static
元素框正常生成。块级元素生成一个矩形框，作为文档流的一部分，行内元素则会创建一个或多个行框，置于其父元素中。
relative
元素框偏移某个距离。元素仍保持其未定位前的形状，它原本所占的空间仍保留。
absolute
元素框从文档流完全删除，并相对于其包含块定位。包含块可能是文档中的另一个元素或者是初始包含块。元素原先在正常文档流中所占的空间会关闭，就好像元素原来不存在一样。元素定位后生成一个块级框，而不论原来它在正常流中生成何种类型的框。
fixed
元素框的表现类似于将 position 设置为 absolute，不过其包含块是视窗本身。
```

## overflow

```css
值
visible	默认值。内容不会被修剪，会呈现在元素框之外。
hidden	内容会被修剪，并且其余内容是不可见的。
scroll	内容会被修剪，但是浏览器会显示滚动条以便查看其余的内容。
auto	如果内容被修剪，则浏览器会显示滚动条以便查看其余的内容。
inherit	规定应该从父元素继承 overflow 属性的值。
```