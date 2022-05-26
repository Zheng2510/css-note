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


