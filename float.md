# float布局
### 步骤
* 子元素上加float:left和width
* 在父元素上加 .clearfix (不要忘了)
### 经验
* 有经验者会留一些空间或者最后一个不设 width
* 不需要做响应式，因为手机上没有 IE，而这个布局是专门为 IE 准备的
IE 6/7 存在双倍 margin bug，解决办法有两个
1.  一是将错就错，针对 IE 6/7 把 margin 减半
2.  二是神来一笔，再加一个 display: inline-block

### clearfix必须加三句话下面是代码
```javascript
*{
    margin:0;
    padding:0;
    box-sizing: border-box;
}
.clearfix:after{
    content: '';
    display: block;
    clear: both;
}
```
### 如果在图片下面有多余的东西就在 图片加上
```
vertical-align:middle;
```

### border换成outline(有时border会占用)
### 对于块元素并且宽度是固定的,那么左边auto外边距和右边auto外边距就会直接居中
```
margin-left:auto;
margin-right:auto;
```
### 经验
* 加上头尾,即可满足所有pc页面 需求
* 手机页面不用float
* float要程序员自己计算宽度,不灵活
* float用来应付 ie足以