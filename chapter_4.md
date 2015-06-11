# JavaScript DOM 编程艺术
## 第四章

```
setAttribute("string name", string value);
```
- 使用 setAttribute 方法来刷新元素的属性。

```
getElementById("ID");
getElementsByTagName("Tag name");
```
- getElementsByTagName() 方法返回元素的顺序是它们在文档中的顺序。

```
onclick = "showPic(this); return false;"
```
- this 关键字在这的含义“这个对象”。
- onclick 事件处理函数；事件处理函数的作用是，在特定事件发生时调用特定的JavaScript代码。
- 事件处理函数的工作机制：在给某个元素添加了事件处理函数后，一旦事件发生，相应的JavaScript代码就会执行。被调用的代码可以返回一个值，这个值将被传递给那个事件处理函数。这个示例中添加了一个 onclick 事件处理函数，并让这个处理函数所触发的代码返回布尔值 true 或 false 。这样的话，根据返回的值， onclick 处理函数就知道链接有没有被点击。而强制设置了 return false 之后，每次 onclick 处理函数都会认为链接并没有被打开，就不会有默认的在新标签打开链接的行为了。