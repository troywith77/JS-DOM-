# JavaScript DOM 编程艺术
## 第四章
### setAttribute 方法
```
setAttribute("string name", string value);
```
- 使用 setAttribute 方法来刷新元素的属性。

### 获取属性
```
getElementById("ID");
getElementsByTagName("Tag name");
```
- getElementsByTagName() 方法返回元素的顺序是它们在文档中的顺序。取得的是一个数组，需要索引。

### onclick 事件处理函数
```
onclick = "showPic(this); return false;"
```
- this 关键字在这的含义“这个对象”。
- onclick 事件处理函数；事件处理函数的作用是，在特定事件发生时调用特定的JavaScript代码。
- 事件处理函数的工作机制：在给某个元素添加了事件处理函数后，一旦事件发生，相应的JavaScript代码就会执行。被调用的代码可以返回一个值，这个值将被传递给那个事件处理函数。这个示例中添加了一个 onclick 事件处理函数，并让这个处理函数所触发的代码返回布尔值 true 或 false 。这样的话，根据返回的值， onclick 处理函数就知道链接有没有被点击。而强制设置了 return false 之后，每次 onclick 处理函数都会认为链接并没有被打开，就不会有默认的在新标签打开链接的行为了。

### childNodes 属性
```
function countBodyChildren(){
    var body_element = document.getElementsByTagName("body")[0];
    alert (body_element.childNodes.length);
}
window.onload = countBodyChildren;
```
- childNodes 属性可以用来获取任何一个元素的所有子元素，它是一个包含这个元素全部子元素的数组。
- 因为文档只有一个 body 元素，所以索引取第一个元素。
- 使用 onload 事件处理函数，让这个函数在页面加载时执行。
- 由 childNodes 属性返回的数组包含所有类型的借点，而不仅仅是元素节点。

### nodeType 属性
```
node.nodeType
alert (body_element.nodeType);
```
- nodeType 的值是一个数字。
- 元素节点的 nodeType 属性值是 1。
- 属性节点的 nodeType 属性值是 2。
- 文本节点的 nodeType 属性值是 3。
- 可以根据 nodeType 的值对特定类型的节点进行处理（if）。