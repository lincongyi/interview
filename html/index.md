> 考点1：语义化

### 问题：说说你对html语义化的理解

!> 答案：根据内容的结构，选择合适的标签，便于开发者阅读和写出优雅的代码，让浏览器的爬虫和机器更好地解析。

### 问题：为什么要语义化

!> 答案：<br>
1.为了再没有css的情况下，页面也能呈现出很好的内容结构；<br>
2.为了优化用户体验，例如img的title、alt等<br>
3.有利于seo<br>
4.方便其他及其解析（如屏幕阅读器、盲人阅读器）<br>
5.便于团队开发和维护

### 问题：html语义化标签有哪些

!> 答案：常用的语义化标签有：```header、footer、hgroup、nav、section、article```等

### 问题：strong和b标签的区别

!> 答案：strong和b标签都可以为字体加上加粗效果，但是b标签仅仅为字体加粗，而strong标签有语义化作用，搜索引擎更关注strong标签下的关键字。


### 问题：i和em标签的区别

!> 答案：i和em标签都可以为字体加上斜体效果，但是em标签仅仅为斜体，而i标签有语义化作用，搜索引擎更关注i标签下的关键字。

### 问题：使用iframe的优缺点，为什么要少用iframe

!> 答案：<br>
优点：<br>
1.程序调入静态页面比较方便<br>
2.页面和程序分离<br>
缺点：<br>
1.样式/脚本需要额外链入，会增加请求<br>
2.iframe的创建比其它包括scripts和css的 DOM 元素的创建慢了 1-2 个数量级，阻塞页面加载<br>

### 问题：label标签的作用

!> 答案：label标签有两个属性:一个是for、另外一个就是accesskey<br>
for属性表示label要绑定的html元素，你点击这个标签的时候，所绑定的元素将获取焦点<br>
accesskey属性表示所绑定的元素的热键，当您按下热键，所绑定的元素将获取焦点

### 问题：meta标签，viewport理解
```html
<meta name="viewport" content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
```
!> 答案：<br>
meta标签中viewport通常是为了做到移动端的兼容和适配<br>
属性：<br>
width:设置viewport的宽度 device-width:获取当前设备的宽度<br>
initial-scale=1:设置初始缩放比例<br>
minimum-scale=1:最小缩放值<br>
user-scalable=no:不允许用户进行缩放

### 问题：html5新特性

!> 答案：<br>1.语义化标签<br>2.增强型表单<br>3.视频和音频<br>4.canvas绘图<br>5.svg绘图<br>6.地理定位```getCurrentPosition()```<br>7.拖放api```draggable="true"```<br>8.WebWorker<br>9.WebStorage```localStorage```和```sessionStorage```<br>10.WebSocket

### 问题：```cookie/localStorage/sessionStorage```的区别

!> 答案：<br>
1.```cookie```<br>
cookie是服务器发给客户端的特殊信息，cookie是以文本的方式保存在客户端，每次请求时都带上它<br>
一般由服务器生成，如果不设置过期时间，cookie被保存在内存中，生命周期随浏览器的关闭而结束；如果设置了cookie的过期时间，cookie被保存在硬盘中，关闭浏览器后，cookie数据仍然存在，直到过期时间结束才消失。<br>
单个cookie保存的数据不能超过4kb（有大小限制）<br>
2.```localStorage/sessionStorage```<br>
仅在客户端中保存，不参与和服务器的通信<br>
存放数据一般5mb<br>
```sessionStorage```仅在当前会话有效，关闭页面后被清除<br>
```localStorage```即使浏览器被关闭了，该数据仍然存在，下次打开浏览器访问网站时仍然可以继续使用

### 问题：前端需要注意哪些SEO

!> 答案：<br>
1.合理的title，description，keyswords 搜索引擎对这三项的权重逐个减小，title 值强调重点即可，重要的关键词出现不要超过两次，而且要靠前<br>
2.不同页面的tilte要有所不同；description把页面的内容高度概括，长度合适，不可过分堆叠关键词，不同页面description有所不同。keyswords列举出重要的关键词即可<br>
3.语义化的HTML代码，符合W3C 规范：语义化代码有利于搜索引擎理解网页<br>
4.重要的内容不要用js输出，爬虫不会执行js获取内容<br>
5.非装饰的图片必须加alt<br>
6.尽量少用iframe ，搜索引擎不会抓取iframe中的内容

### 问题：link和import的区别

!> 答案：<br>
1.@import是 CSS 提供的语法规则，只有导入样式表的作用；link是HTML提供的标签，不仅可以加载 CSS 文件，还可以定义 RSS、rel 连接属性等<br>
2.加载页面时，link标签引入的 CSS 被同时加载；@import引入的 CSS 将在页面加载完毕后被加载<br>
3.可以通过 JS 操作 DOM ，插入link标签来改变样式；无法使用@import的方式插入样式<br>

### 问题：async和defer的作用和区别

!> 答案：<br>
```async```:用于异步下载脚本文件，下载完毕立即解释执行代码<br>
```defer```:用于开启新的线程下载脚本文件，所有元素解析完成之后，DOMContentLoaded 事件触发之前完成

### 问题：重绘和重排

!> 答案：<br>
```reflow（重排）```:当涉及到dom节点的布局属性发生变化时，就会重新计算该属性，浏览器重新绘制响应的元素。<br>
```replaint（重绘）```:当影响到dom元素可见性的属性发生变化时（如color，border-color），浏览器会重新绘制响应的元素。<br>
重排必然会引起重绘<br><br>
重排触发机制：<br>
1.添加或删除可见的DOM元素<br>
2.元素位置改变<br>
3.元素本身的尺寸发生改变(外边距、内边距、边框厚度、宽高、等几何属性)<br>
4.内容改变<br>
5.页面渲染器初始化<br>
6.浏览器窗口大小发生改变<br>
7.获取某些属性。当获取一些属性时，浏览器为取得正确的值也会触发重排，它会导致队列刷新，这些属性包括：offsetTop、offsetLeft、 offsetWidth、offsetHeight、scrollTop、scrollLeft、scrollWidth、scrollHeight、clientTop、clientLeft、clientWidth、clientHeight、getComputedStyle()。所以，在多次使用这些值时应进行缓存。<br><br>
减少重排：<br>
1.避免逐条修改样式，建议集中修改或者切换类名；<br>
2.减少dom操作；<br>
3.使用文档片段创建一个子树，然后再拷贝到文档中(```document.createDocumentFragment()```)；<br>
4.定位(```fixed||absolute```)，使其脱离文档流，修改他们的 CSS 是不会 reflow 的；<br>
5.开启硬件加速；<br>