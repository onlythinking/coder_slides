---
title: 响应式设计-视口（Viewport）
theme: solarized
highlightTheme: github
revealOptions:
  transition: 'convex'
  loop: false
  slideNumber: true
---

### 认识视口

视口分为布局视口（layout viewport），视觉视口（visual viewport）和理想视口（ideal viewport）<!-- .element: style="font-size: 24px;" -->

- 布局视口可以看作是CSS布局时的画布。<!-- .element: style="font-size: 24px;" -->
- 视觉视口是当前显示的页面区域。<!-- .element: style="font-size: 24px;" -->
- 理想视口是页面在设备最佳的呈现。<!-- .element: style="font-size: 24px;" -->



> 视口 (viewport) 代表当前可见的计算机图形区域。浏览器中的viewport和 html 区域相同。在大多数移动设备中，浏览器是全屏的，所以 viewport 是整个屏幕的大小<!-- .element: style="font-size: 16px;color: #909399;" -->



Web 浏览器视口会动态调整<!-- .element: class="fragment" style="font-size: 24px;" -->

比如：当使用触屏双指缩放，当动态键盘在手机上弹出的时候，或者之前隐藏的地址栏变得可见的时候，视觉视口缩小了，但是布局视口却保持不变。<!-- .element: class="fragment" style="font-size: 20px;" -->



---

### 移动设备的视口

移动设备的视口的默认值为 980px，一般情况下都要比这些设备的屏幕尺寸要大。<!-- .element: style="font-size: 24px;" -->

一个常用的针对移动网页优化过的页面的 viewport meta 标签大致如下：<!-- .element: style="font-size: 24px;color: #909399;" -->

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

- width：控制 viewport 的大小，可以指定的一个值，如 600，或者特殊的值，如 device-width 为设备的宽度（单位为缩放为 100% 时的 CSS 的像素）。<!-- .element: class="fragment fade-down" style="font-size: 20px;" -->
- height：和 width 相对应，指定高度。<!-- .element: class="fragment fade-down" style="font-size: 20px;" -->
- initial-scale：初始缩放比例，也即是当页面第一次 load 的时候缩放比例。<!-- .element: class="fragment fade-down" style="font-size: 20px;" -->
- maximum-scale：允许用户缩放到的最大比例。<!-- .element: class="fragment fade-down" style="font-size: 20px;" -->
- minimum-scale：允许用户缩放到的最小比例。<!-- .element: class="fragment fade-down" style="font-size: 20px;" -->
- user-scalable：用户是否可以手动缩放。<!-- .element: class="fragment fade-down" style="font-size: 20px;" -->



---

### 浏览器中尺寸属性

![docs](https://blogs-on.oss-cn-beijing.aliyuncs.com/imgs/202206231726538.png)

----

Screen 对象<!-- .element: style="font-size: 24px;" -->

![image-20220623172526186](https://blogs-on.oss-cn-beijing.aliyuncs.com/imgs/202206231725708.png)

----

Window 对象<!-- .element: style="font-size: 24px;" -->

![image-20220623172556590](https://blogs-on.oss-cn-beijing.aliyuncs.com/imgs/202206231725982.png)



----

Body 对象<!-- .element: style="font-size: 24px;" -->

![image-20220623172624223](https://blogs-on.oss-cn-beijing.aliyuncs.com/imgs/202206231726293.png)



