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

##动画
+ 动画属性

```css
@keyframes 规定动画。
from等价于 0%。
to等价于 100%。
```

```css
animation 所有动画属性的简写属性，除了 animation-play-state 属性。
CSS animation 属性是 animation-name，animation-duration, animation-timing-function，animation-delay，animation-iteration-count，animation-direction，animation-fill-mode 和 animation-play-state 属性的一个简写属性形式。
```

```css
animation-name 规定 @keyframes 动画的名称。

值：

none
特殊关键字，表示无关键帧。可以不改变其他标识符的顺序而使动画失效，或者使层叠的动画样式失效。

IDENT
标识动画的字符串，由大小写敏感的字母a-z、数字0-9、下划线(_)和/或横线(-)组成。第一个非横线字符必须是字母，数字不能在字母前面，不允许两个横线出现在开始位置。
```

```css
animation-duration 规定动画完成一个周期所花费的秒或毫秒。

值

<time>
一个动画周期的时长，单位为秒(s)或者毫秒(ms)，无单位值无效。
```

```css
animation-timing-function CSS animation-timing-function属性定义CSS动画在每一动画周期中执行的节奏。可能值为一或多个 <timing-function>。对于关键帧动画来说，timing function作用于一个关键帧周期而非整个动画周期，即从关键帧开始开始，到关键帧结束结束。

值

<timingfunction>
每个 <timing-function>代表了应用于动画的timing function，定义于animation-property.
```

```css
animation-delay CSS属性定义动画于何时开始，即从动画应用在元素上到动画开始的这段时间的长度。0s是该属性的默认值，代表动画在应用到元素上后立即开始执行。否则，该属性的值代表动画样式应用到元素上后到开始执行前的时间长度；定义一个负值会让动画立即开始。但是动画会从它的动画序列中某位置开始。例如，如果设定值为-1s，动画会从它的动画序列的第1秒位置处立即开始。
如果为动画延迟指定了一个负值，但起始值是隐藏的，则从动画应用于元素的那一刻起就获取起始值。

值

<time>
从动画样式应用到元素上到元素开始执行动画的时间差。该值可用单位为秒(s)和毫秒(ms)。如果未设置单位，定义无效。
```

```css
animation-iteration-count  CSS 属性   定义动画在结束前运行的次数 可以是1次 无限循环，如果指定了多个值，每次播放动画时，将使用列表中的下一个值，在使用最后一个值后循环回第一个值。

值

infinite
无限循环播放动画.

<number>
动画播放的次数；默认值为1。可以用小数定义循环，来播放动画周期的一部分：例如，0.5 将播放到动画周期的一半。不可为负值。
```

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

```css
animation-play-state 属性定义一个动画是否运行或者暂停。可以通过查询它来确定动画是否正在运行。另外，它的值可以被设置为暂停和恢复的动画的重放。恢复一个已暂停的动画，将从它开始暂停的时候，而不是从动画序列的起点开始在动画。

值

running
当前动画正在运行。

paused
当前动画已被停止。
```