# html标签

+ lang=“en”

告诉搜索引擎爬虫，我们的网站是关于什么内容

+ p标签 

```html
<p></p>段落标签
```

+ h标签

```html
<h1></h1> h1-h6 标题标签 一级到六级标签大小逐次减小
```

+ strong标签

```html
<strong></strong>能把标签内的内容加粗
```

+ em标签

```html
<em></em>将标签内的内容斜体
```

+ 既加粗又斜体

```html
strong 和 em 标签嵌套 <strong><em></em></strong> or <em><strong></strong></em>都可以
```

+ del标签

```html
<del></del>中划线标签
```

+ address标签

```html
斜体 用处不大 了解
```

+ div标签

```html
充当容器 分块 让页面更加结构化
```

+ span标签

```html
容器
```

+ html编码

```html
&nbsp; 文本分割符 空格，&lt; < 小于号 &gt; > 大于号
```

+ 回车

```html
<br>
```

+ 有序列表（用处不大）

```html
<ol><li></li></ol> <ol type="a"> 内容将按abcd来排序 五种排序方式1 a A i I  倒序加属性reversed="reversed"  从第2个开始排 start="2"
```

+ 无序列表

```html
<ul><li></li></ul> type="disc"实心圆 "circle"空心圆 "square"方块 导航栏最好的骨架
```

+ img标签

```html
<img src=""> 1.网上url 2.本地绝对路径 3.本地相对路径 alt="" 图片占位符 当图片地址发生错误 展示alt里的内容 title=""图片提示符 
```

+ a标签

```html
<a href=""></a> href超文本引用 
1.超链接
2.锚点<div id="ab">你好</div> <a href="#ab">谢谢</a>点击 谢谢 跳转到 你好
3.打电话 href="tel:1588......."
```

+ form表单标签

```html
 <form mothod="get/post" action="">action 接收地址
      <p>
          username:<input type="text" name="username"> name为数据名
      </p>
      <p>
          password:<input type="password" name="password"> 
      </p>
      <input type="submit">
      type="radio"单选框 要想做成选择题 name属性要一样 value=""数据值 
      checked="checked"默认选中
 </form>
```

+ select标签

```html
<select><option></option></select>下拉菜单
```

+ 注释 调试

```html
<!--  --> ctrl+?快捷键 
```