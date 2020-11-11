[TOC]



## 事件

### 焦点

#### 获得焦点事件

```javascript
jq_obj.focus(function(){})
```

#### 失去焦点事件

```javascript
jq_obj.bulr(function(){})
```

### 鼠标

#### 按下事件

```javascript
// 鼠标按钮被按下（左键或者右键）时触发。不能通过键盘触发。
jq_obj.mousedown(function(){})
```

#### 释放事件

```javascript
// 鼠标按钮被释放弹起时触发。不能通过键盘触发。
jq_obj.mouseup(function(){})
```

#### 单击事件

```javascript
// 单击鼠标左键或者按下回车键时触发。这点对确保易访问性很重要，意味着onclick事件处理程序既可以通过键盘也可以通过鼠标执行。
jq_obj.click(function(){})
```

#### 双击事件

```javascript
// 双击鼠标左键时触发。
jq_obj.dblclick(function(){})
```

#### 移入事件

```javascript
// 鼠标移入目标元素上方。鼠标移到其后代元素上时会触发。
jq_obj.mouseover(function(){})
```

#### 移出事件

```javascript
// 鼠标移出目标元素上方。
jq_obj.mouseout(function(){})
```

#### 移入事件

```javascript
// 鼠标移入元素范围内触发，该事件不冒泡，即鼠标移到其后代元素上时不会触发。
jq_obj.mouseenter(function(){})
```

#### 移出事件

```javascript
// 鼠标移出元素范围时触发，该事件不冒泡，即鼠标移到其后代元素时不会触发。
jq_obj.mouseleave(function(){})
```

#### 移动事件

```javascript
// 鼠标在元素内部移到时不断触发。不能通过键盘触发。
jq_obj.mousemove(function(){})
```

### 键盘

#### onkeydown

```javascript
// 在用户按下一个按键时执行Javascript代码
<input type="text" onkeydown="myFunction()">
```

#### onkeypress

```javascript
// 在用户按下键盘按钮时执行Javascript代码
<input type="text" onkeypress="myFunction()">
```

#### onkeyup

```javascript
// 当用户释放键盘按钮时执行Javascript代码
<input type="text" onkeyup="myFunction()">
```

