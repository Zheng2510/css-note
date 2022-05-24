## css盒模型
* 一种是content-box内容盒-内容就是盒子的边界
* 一种是border-box边框盒-边框才是盒子的边界
* 二者区别是-content-box的宽度是只包含content  ,而border-box的宽度包含到border(border,内边距,内容)
### 公式
* content-box width=内容宽度
* border-box width=内容宽度+padding+border

### 哪个好用
* border-box好用
* 同时指padding,width,border就知道为什么了
## margin合并
### 外边距合并的情况只在上下方向存在,左右方向不存在
### 如何让父元素和第一个孩子或者最后一个儿子的外边距不合并,加个padding,overflow,border
### 哪些情况合并
* 父子margin合并
* 兄弟margin合并
### 如何阻止合并
* 父子合并用padding/border挡住
* 父子合并用overflow:hidden挡住
* 父子合并用display:flex,
* 兄弟合并符合预期的
* 兄弟合并可以用inline-block消除
* 总之要一条一条死记
* css属性逐年增多,每年都有可能有新的

### 基本单位
* 长度单位
* px像素
* em相对于自身font-size的倍数
* 百分数
* 整数
* rem
* vw和vh
* 其他单位相对用的少

### 颜色
* 十六进制#ff6600或者#f60
* RGBA颜色fgb(0,0,)或者rgba(0,0,0,1)
* hsl颜色hsl(360,100%,100%)
