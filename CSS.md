

# 01-Day

## 1. CSS简介

### 1.1 是什么

- 是层叠样式表的简称
- 也是一种标记语言

### 1.2 语法规范 

- 主要构成：选择器以及一条或多条声明
- `h1 { color: red;  font-size: 25px }`
- 选择器  属性  值

### 1.3 代码风格

- 展开式
- { 前面加个空格    ：后面加个空格

## 2. CSS 基础选择器

### 2.1 选择器作用

- 选择标签

### 2.2 分类

- 基础选择器和复合选择器

- 基础：标签选择器、类选择器、id 选择器、通配符选择器

- <style></style> 写在 <head></head> 里面

  1. 标签选择器：
  
     ```html
     <head>
         <style>
     p {
     	color: red;
     }
     </style>
     </head>
     <body>
         <p>
         </p>
     </body>
     ```
  
     
  
  2. 类选择器：
  
     ```html
     <head>
         <style>
     .box {
     	width: 100px;
     	font-size: 35px;
     }
     </style>
     </head>
     <body>
         <div class="box red">
             
         </div>
     </body>
     ```
  
     
  
  3. id 选择器：样式 # 定义 结构 id 调用，只能调用一次 `#red {color: red;}` `<div id="red"></div>
  
  2. 通配符选择器：* 将所有的标签修改 `* {color: red;}`

### 2.3 类选择器-多类名

- 可以写多个多类名（给某个标签添加了多个类）
- 多类名中间必须用空格隔开

## 3. 字体属性

### 3.1 字体系列 `font-family: 'Microsoft YaHei';`

### 3.2 字体大小`font-size: 16px;`

- 标题标签比较特殊，需要指定文字大小
- 记得加上px（单位）

### 3.3 字体的粗细 

- 无单位
- `font-weight:  400;` -- 正常大小
- `font-weight:  700;` -- 粗一点

### 3.4 文字样式 `font-style: normal;`

- 主要是让倾斜的文字<em></em> (标签)不倾斜
- italic 倾斜的

### 3.5 字体符合属性

- 不能更换顺序，每个属性建议空格隔开

- 必须保留 font-size 和 font-family 属性

- ```
  body {
  	font: font-style font-weight font-size/line-height font-family;
  	font: 700 16px 'Microsoft yahei';
  }
  ```

## 4. 文本属性

![image-20221029172151322](C:\Users\谭佳卉\AppData\Roaming\Typora\typora-user-images\image-20221029172151322.png)

## 5. CSS引入方式

![image-20221029183740399](C:\Users\谭佳卉\AppData\Roaming\Typora\typora-user-images\image-20221029183740399.png)

# 02-Day

## 1. Emmet 语法

 - ### 快速生成 HTML 结构语法

  1. 生成标签：直接输入标签名 + Tab 键
  2. 生成多个相同标签：比如 div*3 + Tab 键
  3. 包含关系的标签：比如 ul>li + Tab 键
  4. 并列关系的标签：比如 div+p + Tab 键
  5. 生成带有类名或者id名字的：.demo 或者 #two + Tab 键
  6. 生成 div 类名是有顺序的，用自增符号 $：比如 div$*5 + Tab 键
  7. 如果想要在生成的标签内部写内容用{}：比如 div{哈哈哈哈} + Tab 键

- ### 快速生成 HTML 结构语法  

## 2. 复合选择器

![image-20221030205138609](C:\Users\谭佳卉\AppData\Roaming\Typora\typora-user-images\image-20221030205138609.png)

## 3. 元素显示模式

- 块元素
  1. 独占一行 比如<h1><p><div>
  2. 高度、宽度、外边距以及内边距都可以控制
  3. 宽度默认是容器的100%
  4. 是一个容器及盒子，里面可以放行内或者块级元素
  5. 注意：文字类的元素不能使用块级元素，比如<p><h1>里面不能放块级元素<div>
- 行内元素
  1. 一行可以显示多个
  2. 高、宽直接设置是无效的
  3. 默认宽度就是它本身内容的宽度
  4. 只能容纳文本或其它行内元素
  5. 注意：链接里面不能再放链接；特殊情况链接<a>里面可以放块级元素，转换一下块级模式最安全
- 行内块元素![image-20221030211334660](C:\Users\谭佳卉\AppData\Roaming\Typora\typora-user-images\image-20221030211334660.png)

## 4.   背景

![image-20221031192526991](C:\Users\谭佳卉\AppData\Roaming\Typora\typora-user-images\image-20221031192526991.png)

# 03-Day

## 1. 三大特性

- 层叠性、继承性、优先级（有权重叠加）

  ![image-20221101114035190](C:\Users\谭佳卉\AppData\Roaming\Typora\typora-user-images\image-20221101114035190.png)

  - 继承的权重是 0

## 2. 盒子模型

### 2.1 边框

- `border-width` -- 边框粗细，单位px
- `border-style` -- 边框的样式
- `border-color` -- 边框的颜色

### 2.2 内边距

![image-20221101124403219](C:\Users\谭佳卉\AppData\Roaming\Typora\typora-user-images\image-20221101124403219.png)

### 2.3 外边距

- margin：0 auto；-- 典型应用
- 盒子必须指定宽度 -- 水平居中
- 行内元素或行内块元素水平居中给其父元素添加 text-align：center；

### 2.4 清除内外边距

- ul 有内外边距   div 没有内外边距

- ```html
  * {
  	padding: 0;
  	margin: 0;
  }
  ```

- 行内元素只设置左右边距

- ul 去掉小圆点

  ```
  li {
  	list-style: none;
  }
  ```

  

## 3. PS 基本操作

![image-20221101194835269](C:\Users\谭佳卉\AppData\Roaming\Typora\typora-user-images\image-20221101194835269.png)

![image-20221101194858789](C:\Users\谭佳卉\AppData\Roaming\Typora\typora-user-images\image-20221101194858789.png)

## 4. 圆角边框（重点） 

- `border-radius:`
- 圆形：设置一个正方形盒子，`border-radius:50%`
- 圆角矩形：设置为高度的一半  

## 5. 盒子阴影（重点）

- `box-shadow: 10px 10px 10px -4px rgb(0, 0, 0, .3);`
- 水平阴影  垂直阴影  模糊距离(虚实)  阴影的尺寸  阴影的颜色  内(inset)外(不用写，默认的)阴影

## 6. 文字阴影

# 04-Day

## 1. 浮动

### 1.1 应用：

- 可以让多个块级元素一行内排列显示

### 1.2 网页布局第一准则：

- 多个块级元素纵向排列找标准流，多个块级元素横向排列找浮动

### 1.3 特性：

    1. 脱离了标准普通流的控制移动到指定位置(俗称脱标)、浮动的盒子不再保留原县的位置
    2. 浮动的盒子一行显示上边对齐
    3. 添加浮动后具有行内块特性

### 1.4 浮动布局注意点

- 浮动和标准流的父盒子搭配：先用标准流的父元素排列上下位置，之后内部子元素采取浮动排列左右位置
- 一个元素浮动了，理乱上其他兄弟元素也要浮动：一浮全浮
- 浮动的盒子只会影响后面的标准流，不会影响前面的标准流

###  1.5  清除浮动

## 2. PS 切图

## 3. CSS 属性书写顺序

1. 布局定位属性：display / position / float .clear / visibility / overflow
2. 自身属性：width / height / margin / padding / border / background
3. 文本属性：color / font / text-decoration / text-align / white-space / break-word
4. 其他属性：content / 

## 4. 定位

### 4.1 分类

- 相对定位：移动位置的参照点是自己原先的位置
- 绝对定位：
  1. 如果没有祖先元素或者祖先元素没有定位则以浏览器为准定位；
  2. 如果祖先有定位，则以最近一级的定位祖先元素为参考点移动位置
  3. 不再占有原先的位置（脱标）

### 4.2 应用：（子绝父相）

1. 子级绝对定位，不会占有位置，可以放到父盒子里面的任何一个地方，不会影响其他的兄弟盒子
2. 父盒子需要加定位限制子盒子，需要占有位置 -- 相对定位

- 固定定位：
  1. 以浏览器的可视窗口最为参照点移动，不随滚动条滚动
  2. 脱标的 -- 一种特殊的绝对定位
  3. 小技巧：固定在版心右侧位置
     - 让固定定位的盒子left：50% 走到浏览器可视区
     - 再让固定定位的盒子贴着版心右侧对齐

### 4.3 总结

| 定位模式          | 是否脱标       | 移动位置           |
| ----------------- | -------------- | ------------------ |
| relative 相对定位 | 否(占有位置)   | 相随与自身位置移动 |
| absolute 绝对定位 | 是(不占有位置) | 带有定位的父级     |
| fixed 固定定位    | 是(不占有位置) | 浏览器可视区       |

- 绝对定位和固定定位不能用margin：auto；相对定位可以

###   4.4 叠放次序

- `选择器{ z-index: 1;}`
- 数值可以是正整数、负数或0，默认是auto，数值越大，盒子越靠上
- 数字后面不能加单位
- 只有定位的盒子才有z-index属性

### 4.5 注意

- 加了绝对定位的盒子不能通过margin：0 auto 水平居中，要写`{left: 50%; margin-left: 50%}`
- 行内元素添加绝对或者固定定位，可以设置高度和宽度
- 块级元素添加绝对或者固定定位，如果不给宽度或者高度，默认大小是内容的大小
- 绝对定位会完全压住盒子（压住下面标准流的所有内容）
- 而浮动元素不同，不会压住文字，产生目的是为了做文字环绕效果

## 5. 元素的显示与隐藏

### 5.1 display 属性

- 不保留原来位置
- display：none；隐藏对象
- display：block；转换为块级元素，显示元素

# 05-Day

## 1. 精灵图

- 一般精灵图都是负值  

## 2. 字体图标

- 本质上文字：简单的小图标![image-20221104214352698](C:\Users\谭佳卉\AppData\Roaming\Typora\typora-user-images\image-20221104214352698.png)

## 3. 三角做法

## 4. 行内块元素和文字垂直居中对齐

- 如果直接插入图片就不用转换为行内块元素，
- 如果插入背景就需要先转换为行内块元素`display: inline-block`
- `vertical-align: middle;`
- 可以解决图片底部默认空白缝隙问题，或将块内元素转换为行内块元素

## 5. 文字溢出省略号显示

- 单行：

  ```
  div {
  	white-space: nowrap;
  	overflow: hidden;
  	text-overflow: ellipsis;
  }
  ```

## 6. 布局技巧

- ```html
  <style>
      ul li {
          float: left; /*将无序列表放到一行显示*/
          list-style: none;
          width: 150px;
          height: 200px;
          border: 1px soloid red;
      }
  </style>
  ```

- margin 负值巧妙运用
