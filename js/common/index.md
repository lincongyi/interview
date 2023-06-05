### 问题：javascript的数据类型

!> 答案：<br>
```null、undefined、 number、 string、 boolean、 bigInt(最大安全整数)、 symbol、 object(七种)```

### 问题：判断javascript数据类型的方式

!> 答案：<br>
1.typeof<br>
可以判断出primitve类型：```string、 number、 boolean、 bigInt、 symbol、 undefined```<br>
但判断null为object，判断数组和对象时，值均为object<br>
2.instanceof<br>
用于检测构造函数的prototype属性是否出现在某个实例对象的原型链上。<br>
3.Object.prototype.toString.call() // ["Object" "Object"]<br>
常用于判断浏览器内置对象，对于所有数据类型都能判断<br>
4.```Object(value) === value```// true为对象，false为基本类型

### 问题：判断是否数组

!> 答案：<br>
1.```arr instanceof Array```<br>
2.```Array.isArray(arr)```<br>
3.```Object.prototype.toString.call(arr).slice(8,-1)```// Array

### 问题：javascript预编译的4个步骤
!> 答案：<br>
1.创建ao（活跃）对象<br>
2.找到形参和变量声明<br>
3.实参和形参像统一<br>
4.找到函数声明

### 问题：操作dom元素有哪些方法

!> 答案：<br>
1.```createElement```:创建一个标签节点<br>
2.```createTextNode```:创建一个文本节点<br>
3.```cloneNode(deep)```:复制一个节点，连同属性值一起复制。当deep为true时，连同后代节点属性事件等一起复制，默认为false，只复制当前节点<br>
4.```createDocumentFragment```:创建一个文档碎片<br>
5.```appendChild```:追加子元素<br>
6.```insertBefore```:将子元素插入到前面<br>
7.```removeChild```:删除子元素<br>
8.```replaceChild```:替换子元素<br>
9.```getAttribute```:获取节点属性<br>
10.```createAttribute```:创建节点属性<br>
11.```setAttribute```:设置节点属性<br>
12.```removeAttribute```:删除节点属性<br>
13.```var attr = [element].attributes```:将属性转换成类数组对象

### 问题：toLocaleString()的使用

```js
let num1 = 12345678
num1.toLocaleString() // 12,345,678

let num2 = 0.23
num2.toLocaleString('zh',{style:'percent'}) // 23%

let num3 = 98765
num3.toLocaleString('zh',{style:'currency',currency:'cny'}) // ¥98,765.00
```

### 问题：onmouseover和onmouseenter的区别

!> 答案：<br>
不论鼠标指针穿过被选元素或其子元素，都会触发mouseover事件，对应mouseout事件；<br>
只有再鼠标穿过被选元素时，才会触发mouseenter事件，对应mouseleave