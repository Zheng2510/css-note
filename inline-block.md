# 基本概念
## 要理解几个重要的概念
* 文档流 Normal Flow
* 块 ,内联,内联块
* margin合并
* 两种盒模型 (border-box更符合人类思维)

### 文档流(指文档流动方向)-从左到右从上到下
1. 流动方向
* inline元素从左到右,到达最右边才换行
* block元素从上到下,每一个都另起一行
* inline-block也是从左到右(但不会处于两行中间,和inline相似但又不同的一点)

2. 宽度
* inline宽度为内部inline元素的和,不能用width指定
* block默认自动计算宽度,可用width指定
* inline-block结合前两者特点

3. 高度
* inline高度由line-height间接确定,和height无关
* block高度由内部文档流元素决定,可以设height
* inline-block跟block类似,可以设置height
### 元素不分内联还是外联元素
### 不要在inline元素写block元素
### block默认宽度不是100%而是auto-能有多宽就有多宽,可以指定宽度
### 永远不要写宽度百分之百
### inline不接受宽度,是由内联元素的总和决定
### div里什么都没有,那么高度为0
### 如果有滚动条,默认只在第一屏显示

## overflow 溢出
### 当内容大于容器
* 等内容的宽度或高度大于容器的,会溢出
* 可用overflow来设置是否显示滚动条
* auto是灵活设置(当需要有滚动条的时候会显示)
* scroll是永远显示
* hidden是直接隐藏溢出部分
* visible是直接显示溢出部分
* overflow可以分为overflow-x和overflow-y

### 脱离文档流
1. 回忆
* block高度是由内部文档流元素决定,可以设置height
* 这句话的意思是不是,有些元素可以不在文档流里

2. 哪些元素脱离文档流
* float
* position:absolute/fixed

3. 怎么让元素不脱离文档流
* 不要用上面那些属性就可以