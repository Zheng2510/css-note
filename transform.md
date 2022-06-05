# transform
### 详细内容在-[mdn](https://developer.mozilla.org/zh-CN/docs/Web/CSS/transform)
* 四个常用功能
1. translate 位移 支持xyz
2. scale 缩放
3. rotate 旋转
4. skew 倾斜

* 经验
* 一般都需要配合transition过度
* inline元素不支持transform,需要先变成block

### 居中显示
* ![图片](images/剧中显示.jpg)

### translate用法(位移)
* translateX(<length-percentage>)
* translateY(<length-percentage>)
* translate(<length-percentage>,<length-percentage>)
* translateZ(<length>)且父容器perspective
* translate3d(x,y,z)
* ![代码演示](images/代码演示1.jpg)
### 经验
* 要学会看mdn语法示例
* translate(-50%,-50%)可做绝对定位元素居中
### scale用法(缩放)
* 常用写法
1. scaleX(<number>)
2. scaleY(<number>)
3. scale(<number>,<number>?)
4. ![代码示例](images/5.jpg)
* 注意:用的少,因为容易出现模糊

### rotate常用写法(旋转)
* rotate([<angle> | <zero>])
*  rotateZ([<angle> | <zero>])
*   rotateY([<angle> | <zero>])
*    rotateX([<angle> | <zero>])
*   rotate3d复杂具体看文章[文章地址](https://developer.mozilla.org/zh-CN/docs/Web/CSS/transform-function/rotate3d)
* ![演示代码](images/6.jpg)
* 经验-一般用于制作360°旋转制作loading
* 用到时搜索rotate mdn文档

### skew(倾斜)常用写法
* skewX([<angle>] | [<zero>])
* skewY([<angle>] | [<zero>])
* skew([<angle>] | [<zero>],[<angle>] | [<zero>])
* ![代码演示](images/7.jpg)
* 经验-用的少,用到时搜索skew mdn

### transform多重效果
1. transform:scale(0.5) translate(-100%,-100%);
2. transform:none;取消所有



## transition过渡
* 作用-补充关键帧
* 语法

1. transition:属性名 时长 过渡方式 延迟
2. transition: left 200ms linear
3. 可以用逗号分隔两个个不同的属性;
4. transition:left 200ms,top 400ms;
5. 可以用all代表所有属性
6. transition:all 200ms;
7. 过渡方式有: linear |ease|ease-in|ease-out|ease-in-out|cubic-bezier|step-start|step-end|steps  [具体网址](https://developer.mozilla.org/en-US/docs/Web/CSS/easing-function)

### 并不是所有属性都能过度
1. display:none =>block无法过渡
2. 一般改成 visibility:hidden => visible
3. display和visibility的区别
4. background

### 动画两次效果
* 两种方法
1. 使用两次transform
* a===transform===b
* b===transform===c
* 如何知道中间点
* 用set time out或者监听transtitionend事件
* [示例](http://js.jirengu.com/buwah/1/edit?html,css,js,output)
2. 使用animation
* 声明关键帧
* 添加动画
* [示例](http://js.jirengu.com/peran/1/edit?html,css,output)

### animation
* 缩写语法
* animation:时长|过渡方式|延迟|次数|方向|填充模式|是否暂停|动画名;
* 时长:1s或者1000ms;
* 过渡方式:跟transition取值一样,例如linear
* 次数:3 或者2.4或者infinite
* 方向:reverse(反过来-从最后往前)|alternate(先进去再回来)|alternate-reverse(先回来再进去)
* 填充模式:none|forwards|backwards|both
* 是否暂停:paused|running
* 以上所有属性都有对应的单独属性
### [红心动画](http://js.jirengu.com/hosug/1/edit?html,css,output)