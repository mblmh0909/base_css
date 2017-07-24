## 一、基础
### 1.标记
*  嵌套 > class > id
*  组件化
*  css3语义标签+同名class

### 2.选择器
> ***选择器顺序 内联 > id > 类(伪类、属性) > 类型***

1.  基本选择器
 * **\'#'**_id选择,**'.'** 类选择,**'>'** 直接子选择,**'空格'** 子选择,**'\[ \]'**属性选择
2. 属性选择器
 * **'='**(非必需),**'~='**包含,**'|='**以开始,**'^='**开头,**'$='**结尾,**'\*='**有
3. 点击伪类  
 * (a)**':link'**为访问,**':visited'**已访问,(a,button)**':hover'**悬浮,**':active'**点击,**':focus'**焦点
 * 遁寻LoVe/HAte原则
 * IE6、7不支持 :active 和 :focus
4. input伪类
 * **':disabled'**,**':enabled'**,**':checked'**
 * IE6-IE8不支持
5. 选择子伪类
 * **':first-child'**，**':last-child'**，**':nth-child()'**，**':nth-last-child()'**
 * **':first-of-type'**，**':last-of-type'**，**':nth-of-type()'**，**':nth-last-of-type()'**
 * **'only-child'**,**'only-of-type'** 只存在唯一
 * **'empty'** 完全连空格都没有
 * nth可接收数字参数,即第几个
 * nth可接收n参数,注意只能是n,如2n、2n-1、n+5、n-5等
 * of-type类型限定,last倒数计数
 * 参数可接收even代表偶数
 * IE6-8不支持
6. 否定选择器
 * **':not()'**
7. 伪元素
 * **':first-letter'**，**':first-line()'**
 * **':before'**,**':after'**
 * beore after 常配合css属性 **content** 使用

### 3.文档顺序
* 一般 > 辅助 > 页面结构 > 组件 > 覆盖
* 一般包括reset、链接、按钮、列表等的一般显示样式
* 辅助包括表单、表格、通知、提示等通用样式
* 页面结构包含页头、页脚、导航等页面结构相关
* 组件包括，弹出框、提示框、加载、日历等组件样式
- - -
## 二、display
### 1.block和inline
 * inline从左到右,block从上到下
 * margin-top、bottom不作用行内元素
 * padding-top、bottom虽然作用于元素，但是不能排挤其它元素
 * 默认block div p form等
 * 默认inline span label a等

### 2.box-sizing
 * content-box 内容为设置宽度
 * border-box 包含padding border margin的总宽度为设置宽度

### 3.左右居中
 * margin: 0 auto
- - -
## 三、position
### 1.static
 * 默认设置，元素按display设置从左到右、从上到下依次排列
 * 浏览器计算元素占位

### 2.relative
 * 在不设置上下左右时按static显示。
 * 当设置上下左右后按默认位置和上下左右值计算位置。
 * 占位按原static默认占位。不脱离文档流

### 3.absolute
 * 元素按最近的posotion为relative的父元素计算位置。
 * 以该父元素左上角为0,0。
 * 无占位。脱离文档流。

### 4.fixed
 * 按所在窗口左上角为0,0计算位置
 * 无占位。脱离文档流。
- - -
## 四、float
### 1.意义及缺陷
 * 相当于inline-block+排列顺序
 * 与absolute相比存在占位
 * 破坏了本身的高度即高度为0
 * 垂直margin不折叠

### 2.清除浮动
 * 增加clear div
 * overflow+zoom
 * after+zoom

## 五、inline-block
### 1.显示排列
 * 以inline方式排列，以block形式展现。

### 2.元素间隙
 * 吃胶囊
 * 闭合标签换行