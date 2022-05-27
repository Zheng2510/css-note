# flex-item
1. item加order
```
.item:first-child{
    order: 1;
}
.item:nth-child(2){
    order: 3;
}
```
* order改变顺序-数越小往前

2. item加flex-grow(控制如何长胖)
```
.item:first-child{
    flex-grow: 2;
}
.item:nth-child(2){
    flex-grow: 1;
}
```
* 分配第一个孩子两份第二个一份
3. flex-shrink(控制如何变瘦)
* 一般写flex-shrink:0防止变瘦,默认是1;
* 当到达固定宽度时,数值越大瘦的越多
3. flex-basis控制基准宽度-默认auto
4. 让某个item特立独行用align-self: flex-end  |  flex-start ;
### 重点
* display: flex
* flex-direction:row/down (横着还是竖着流动方向)
* flex-wrap:wrap(是否换行)
* just-content:center/space-between
* align-items:center

### 整理知识
* flex-direction和flex-wrap两个属性经常会一起使用，所以有缩写属性flex-flow。这个缩写属性接受两个属性的值，两个值中间以空格隔开。
举个例子，你可以用flex-flow: row wrap去设置行并自动换行。
* 图片溢出来一点用vertical-align:top\middle可以解决
* 要是想让子元素向右顶,把空间放在中间,可以在父元素加justify-content:space-between  | 还发现可以在子元素加 margin-left:auto;
* 平均布局一般加上用上-(负)margin


### 经验
* 永远不要把width和height写死,除非特殊情况;
* 用min-width/max-width/min-height/max-height(min最小,max最大);
* flex可以基本满足需求
* flex和margin-xxx:auto配合有意外效果

### 什么情况是写死
* width: 100px;

* 不写死
* width: 50%;
* max-width:100px;
* width:30vw;
* min-width:80%
* 特点:不使用px,或者加min max前缀; 


