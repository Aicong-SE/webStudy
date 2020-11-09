[TOC]



### 边框border

border: width  style  color;

#### border-style

| 类型   | 说明                                                 |
| ------ | ---------------------------------------------------- |
| dotted | 定义一个点线边框                                     |
| dashed | 定义一个虚线边框                                     |
| solid  | 定义实线边框                                         |
| double | 定义两个边框。两个边框的宽度和 border-width 的值相同 |
| groove | 定义3D沟槽边框。效果取决于边框的颜色值               |
| ridge  | 定义3D脊边框。效果取决于边框的颜色值                 |
| inset  | 定义一个3D的嵌入边框。效果取决于边框的颜色值         |
| outset | 定义一个3D突出边框。 效果取决于边框的颜色值          |

**宽度** border-width: 5px; 

**颜色** border-color: red|rgb(255,0,0)|#ff0000; 

**单独设置各边**

border-top-style: dotted;

border-right-style: solid;

border-bottom-style: dotted;

border-left-style: solid;

### 渐变色

#### 线性渐变

```css
background-image: linear-gradient(direction, color-stop1, color-stop2, ...);
```

```css
# 从上到下
background-image: linear-gradient(#e66465, #9198e5);
# 从左到右
background-image: linear-gradient(to right, red , yellow);
# 对角
background-image: linear-gradient(to bottom right, red, yellow);
# 角度
background-image: linear-gradient(90deg, color-stop1, color-stop2);
# 使用多个颜色节点
background-image: linear-gradient(red, yellow, green);
# 重复的线性渐变
background-image: repeating-linear-gradient(red, yellow 10%, green 20%);
```

#### 径向渐变

```css
background-image: radial-gradient(shape size at position, start-color, ..., last-color);
```

