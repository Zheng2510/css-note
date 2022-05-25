# flex布局  
* container -容器(一般为父元素)
* items-(一般作为子元素)

### container样式有哪些
* 让一个元素变成flex容器
```css
.container {
    display: flex;/* or inline-flex */
}
```
1.  改变items流动方向(主轴)
* 从左往右-
```
.container{
flex-direction: row;
}
```
* 从右往左-
```
.container{
flex-direction:row-reverse;
}
```
* 从上往下-
```
.container{
flex-direction:column;
}
```
* 从下往上-
```
.container{
 flex-direction:column-reverse;
}
```
2. 改变折行
* 不折行
```
.container{
    flex-wrap:nowrap;
}
```
* 折行
```
.container{
    flex-wrap: wrap;
}
```
* 从底下往上折行
```
.container{
    flex-wrap: wrap-reverse;
}
```
### 主轴对齐方式
* 默认主轴是横轴
* 除非改变flex-direction 方向
```
.container{
    justify-content: flex-start |flex-end | center | space-between | space-around | space-evenly ;
}
```
* flex-start-都往前靠
* flex-end-都往后靠
* center-往中间靠
* space-between 把空间放在中间

### 次轴对齐
* 默认次轴是纵轴
```
.container{
    align-items: stretch | flex-start | flex-end | center | baseline
}
```
* stretch -一样高
* flex-start-往上对齐
* flex-end-往下对齐
* center-往中间对齐
### 多行内容
```
.container{
    align-content: flex-start | flex-end | center | stretch | space-between | space-around ;
}
```
* flex-start-往上顶
* flex-end-往下顶
* center-中间
* stretch-空间平均分
* space-between-把空间放在中间,上下顶着
* space-around-空间围绕
