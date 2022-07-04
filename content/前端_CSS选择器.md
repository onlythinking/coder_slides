---
title: Css 选择器
theme: solarized
highlightTheme: github
revealOptions:
  transition: 'convex'
  loop: false
  slideNumber: true
---



### 什么是CSS样式表

CSS 叫做层叠样式表，可以用来设置网页的样式及布局——比如，可以更改内容的字体、颜色、大小以及间距，或是将其分列，或是添加动画及赋予内容其它装饰性的特征。<!-- .element: style="font-size: 24px;" -->

<ul style="font-size: 24px;">
	  <li><a href="#/css_unit">CSS 单位</a></li>
    <li><a href="#/css_selector_priority">选择器优先级</a></li>
    <li><a href="#/css_selector_category">选择器分类</a></li>
</ul>



---

### CSS 单位

<!-- .slide: id="css_unit" -->

- em：font-size中相对于父元素的字体大小，在元素属性中使用是相对于自身字体大小 <!-- .element: style="font-size: 24px;" -->
- rem：根元素的字体大小，在元素属性中使用是相对于根元素字体大小 <!-- .element: style="font-size: 24px;" -->
- 1h：元素的 line-height <!-- .element: style="font-size: 24px;" -->
- vw：视窗宽度的1% <!-- .element: style="font-size: 24px;" -->
- vh：视窗高度的1% <!-- .element: style="font-size: 24px;" -->
- vmin：视窗较小尺寸的1% <!-- .element: style="font-size: 24px;" -->
- vmax：视图大尺寸的1% <!-- .element: style="font-size: 24px;" -->



---

### 选择器优先级

<!-- .slide: id="css_selector_priority" -->

如何判断出选择器的优先级？  <!-- .element: style="font-size: 24px;" -->

![priority](https://blogs-on.oss-cn-beijing.aliyuncs.com/imgs/album_temp_1631516058.PNG)

----

**两条经验法则**  <!-- .element: style="font-size: 24px;" -->

1. 尽量不要使用ID选择器，因为它会大幅提升优先级。当需要覆盖这个选择器时，通常找不到另一个有意义的ID，于是就需要复制原来的选择器加上另一个类来让它区别于想要覆盖的选择器。  <!-- .element: style="font-size: 20px;" -->
2. 不要使用！important。它比ID更难覆盖，一旦用了它，想要覆盖原先的声明，就需要再加上一个！important，而且依然要处理优先级的问题。  <!-- .element: style="font-size: 20px;" -->



---

### 选择器分类

<!-- .slide: id="css_selector_category" -->

- [基础选择器](https://www.onlythinking.com/post/前端_html和css基础/#基础选择器)
- [组合选择器](https://www.onlythinking.com/post/前端_html和css基础/#组合选择器)
- [复合选择器](https://www.onlythinking.com/post/前端_html和css基础/#复合选择器)
- [伪类选择器](https://www.onlythinking.com/post/前端_html和css基础/#伪类选择器)
- [伪元素选择器](https://www.onlythinking.com/post/前端_html和css基础/#伪元素选择器)
- [属性选择器](https://www.onlythinking.com/post/前端_html和css基础/#属性选择器)



----

基础选择器

- 类型或标签选择器，匹配目标元素的标签名，如 ：p，input[type=text]，优先级（0，0，1）。 <!-- .element: style="font-size: 20px;" -->
- 类选择器，匹配class属性中有指定类名的元素，如：.box，优先级（0，1，0）。 <!-- .element: style="font-size: 20px;" -->
- ID选择器，匹配拥有指定ID属性的元素，如：#id， 优先级（1，0，0）。 <!-- .element: style="font-size: 20px;" -->
- 通用选择器（*），匹配所有元素 ，优先级（0，0，0）。 <!-- .element: style="font-size: 20px;" -->



----

组合选择器

- 后代组合器（单个空格（）表示），比如 .nav li，表示li是一个拥有nav类的元素的后代。  <!-- .element: style="font-size: 20px;" -->
- 子组合器（>），匹配的元素是直接后代，.parent > .child。  <!-- .element: style="font-size: 20px;" -->
- 相邻兄弟组合器（+），匹配的元素紧跟在后面其它元素后面，div + p。  <!-- .element: style="font-size: 20px;" -->
- 通用兄弟组合器（~），匹配所有跟随在指定元素之后的兄弟元素，它不会选中目标元素之前的兄弟元素，li.active ~ li。 <!-- .element: style="font-size: 20px;" -->



----

复合选择器

多个基础选择器连起来（中间没有空格）组成一个复合选择器（如：ul.nav）。复合选择器选中的元素将匹配其全部基础选择器，.box.nav 可以选中 class=“box nav” ，但是不能选中 class=“box”。 <!-- .element: style="font-size: 20px;" -->

----

伪类选择器

用于选中某种特定状态的元素，优先级（0，1，0）。  <!-- .element: style="font-size: 20px;" -->

- :first-child——匹配的元素是其父元素的第一个子元素。 <!-- .element: style="font-size: 20px;" -->

- :last-child——匹配的元素是其父元素的最后一个子元素。 <!-- .element: style="font-size: 20px;" -->

- :only-child——匹配的元素是其父元素的唯一一个子元素（没有兄弟元素）。 <!-- .element: style="font-size: 20px;" -->

- :nth-child(an+b)——匹配的元素在兄弟元素中间有特定的位置。公式an+b里面的a和b是整数，该公式指定要选中哪个元素。要了解一个公式的工作原理，请从0开始代入n的所有整数值。公式的计算结果指定了目标元素的位置。下表给出了一些例子。 <!-- .element: style="font-size: 20px;" -->

  

----

伪元素选择器

伪元素选择器可以向HTML标记中未定义的地方插入内容，优先级（0，0，1）。 <!-- .element: style="font-size: 20px;" -->

- ::before——创建一个伪元素，使其成为匹配元素的第一个子元素。该元素默认是行内元素，可用于插入文字、图片或其他形状。必须指定content属性才能让元素出现，如：.nav::before。 <!-- .element: style="font-size: 20px;" -->
- ::after——创建一个伪元素，使其成为匹配元素的最后一个子元素。该元素默认是行内元素，可用于插入文字、图片或其他形状。必须指定content属性才能让元素出现，如：.nav::after。 <!-- .element: style="font-size: 20px;" -->
- ::first-letter——用于指定匹配元素的第一个文本字符的样式，如：h1::first-letter。 <!-- .element: style="font-size: 20px;" -->
- ::first-line——用于指定匹配元素的第一行文本的样式。 <!-- .element: style="font-size: 20px;" -->
- ::selection——用于指定用户使用鼠标高亮选择的任意文本的样式。通常用于改变选中文本的background-color。只有少数属性可以使用，包括color、background-color、cursor、text-decoration。 <!-- .element: style="font-size: 20px;" -->

----

属性选择器

属性选择器用于根据HTML属性进行匹配元素，优先级（0，1，0）。<!-- .element: style="font-size: 20px;" -->

- [attr]——匹配的元素拥有指定属性attr，无论属性值是什么，如：input[disabled]。<!-- .element: style="font-size: 20px;" -->
- [attr=“value”]——匹配的元素拥有指定属性attr，且属性值等于指定的字符串值，如：input[type=“radio”]。<!-- .element: style="font-size: 20px;" -->
- [attr^=“value”]——“开头”属性选择器。该选择器匹配的元素拥有指定属性attr，且属性值的开头是指定的字符串值，例如：a[href^=“https”]。<!-- .element: style="font-size: 20px;" -->
- [attr＊=“value”]——“包含”属性选择器。该选择器匹配的元素拥有指定属性attr，且属性值包含指定的字符串值，如：[class＊=“sprite-"]。<!-- .element: style="font-size: 20px;" -->
- [attr~=“value”]——“空格分隔的列表”属性选择器。该选择器匹配的元素拥有指定属性attr，且属性值是一个空格分隔的值列表，列表中的某个值等于指定的字符串值，如：a[rel=“author”]。<!-- .element: style="font-size: 20px;" -->
- [attr|=“value”]——匹配的元素拥有指定属性attr，且属性值要么等于指定的字符串值，要么以该字符串开头且紧跟着一个连字符（-）。<!-- .element: style="font-size: 20px;" -->
