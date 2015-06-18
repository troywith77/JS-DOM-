# JavaScript DOM 编程艺术
## 第三章
###DOM
DOM（Document Object Model）
###节点
节点表示网络中的一个连接点。
####元素节点
标签的名字就是元素的名字，元素可以包含其他的元素。唯一不被包含在其他元素内的元素是<br>< html >元素，它是我们节点树的根元素。
####文本节点
元素节点是节点类型的一种。如果一份文档完全由空白元素组成，它将只有一个结构，而不会包含什么内容。
####属性节点
属性节点可以对元素做出更具体的描述，如< title >、< href >。因为属性总是被放在起始标签里，所以属性节点总是被包含在元素节点中。并非所有的元素都包含着属性，但所有的属性都被元素包含。
####获取元素
1. getElementById方法。这个方法将返回一个与给定id属性值的元素节点对应的对象。它是document对象特有的函数，在脚本代码中，函数名的后面必须跟有一对圆括号，这对圆括号包含着函数的参数。
```
getElementById("id");
```
2. getElementsByTagName方法。这个方法返回一个对象数组，每个对象分别对应着给定标签的一个元素。这个方法也只有一个参数，就是标签的名字。这个调用返回一个对象数组，我们可以利用length属性查出这个数组里的元素个数。注意：即使在整个文档里这个标签只有一个元素，此方法仍然返回一个数组，如< body >,此时，该数组的长度为1.

3. HTML5 DOM 中新增了一个方法：getElementsByClassName方法。由于这个方法还比较新，某些DOM实现里可能还没有，因此使用时要注意。使用此方法时将类名传入参数，要指定多个类名时，只需用空格隔开。

####知识点
- 一份文档就是一颗节点树
- 节点分为不同的类型：元素节点、文本节点、属性节点
- getElementById将返回一个对象，该对象对应着文档里的一个特定的元素节点
- getElementsByTagName 和 getElementsByClassName 将返回一个对象数组，它们分别对应着文档里的一组特定的元素节点
- 每个节点都是一个对象

###获取和设置属性
1. getAttribute<br>
getAttribute 是一个函数。它只有一个参数——打算查询的属性的名字。
```
object.getAttribute("attribute");
```
与之前的方法不同，getAttribute 方法不属于 document 对象，所以不能通过 document 对象调用。它只能通过元素节点对象调用

2. setAttribute<br>
此方法允许我们对属性节点的值做出修改，只能用于元素节点。
```
object.setAttribute("attribute",value);
```