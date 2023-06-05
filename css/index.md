### 问题：BFC

!> 答案：<br>
块级格式化上下文。是一个隔离的独立容器，其内部子元素和外部元素相互不影响；<br><br>
形成条件：<br>
1.浮动元素；<br>
2.定位元素；<br>
3.display:inline-block,table-cells......；<br>
4.overflow:hidden,auto,scroll；<br><br>
常见作用：<br>
1.浮动元素无法撑起父类（父类高度不一致）；<br>
2.不被兄弟浮动元素覆盖；<br>
3.解决margin塌陷（子元素display:inline-block）；<br>