# CSS的盒模型

![box-model-standard-small](https://user-images.githubusercontent.com/34019939/50679860-2ec31900-1040-11e9-87be-bda81d1ceb55.png)

- `width`和`height`
> width 和 height 设置内容框（content box）的宽度和高度。内容框是框内容显示的区域——包括框内的文本内容，以及表示嵌套子元素的其它框。

- `padding`
> padding 表示一个 CSS 框的内边距 ——这一层位于内容框的外边缘与边界的内边缘之间。该层的大小可以通过简写属性padding 一次设置所有四个边，或用 padding-top、padding-right、padding-bottom 和 padding-left 属性一次设置一个边。
`padding:20px`  设置四面均为20px
`padding:20px 100px 0px 20px `  设置上右下左

_当padding增加时，CSS框也会跟着增加。因为padding是内容框和CSS内边框之间的距离_

-  `border`
> CSS 框的边界（border）是一个分隔层，位于内边距的外边缘以及外边距的内边缘之间。边界的默认大小为0——从而让它不可见——不过我们可以设置边界的厚度、风格和颜色让它出现。 border 简写属性可以让我们一次设置所有四个边，例如  border: 1px solid black; 但这个简写可以被各种普通书写的更详细的属性所覆盖：
`border: 1px solid black`  三个参数对应： `border-width, border-style, border-color`

- `margin`
> 外边距（margin）代表 CSS 框周围的外部区域，称为外边距，它在布局中推开其它 CSS 框。其表现与 padding 很相似；简写属性为 margin，单个属性分别为 margin-top、margin-right、margin-bottom 和 margin-left。

**注意**：_外边距有一个特别的行为被称作外边距塌陷（margin collapsing）：当两个框彼此接触时，它们的间距将取两个相邻外边界的最大值，而非两者的总和。_

- `overflow`
> 当你使用绝对的值设置了一个框的大小（如，固定像素的宽/高），允许的大小可能不适合放置内容，这种情况下内容会从盒子溢流。我们使用overflow属性来控制这种情况的发生。它有一些可能的值，但是最常用的是：
1. auto: 当内容过多，溢流的内容被隐藏，然后出现滚动条来让我们滚动查看所有的内容。
2. hidden: 当内容过多，溢流的内容被隐藏。
3. visible: 当内容过多，溢流的内容被显示在盒子的外边（这个是默认的行为）

- 框类型（display)
 1. `display:block`  一个单独的框，可以是嵌套框; 内容独占一行，可以设置width height。
 2. `display:inline`  行内框，将一行里面的某些元素框起来，而且这个框会换行 ; width和height都是自动的，不能设置。
 3. `inline-block` 不会换行，放不下的时候整个跑到下一行; 可以设置width和height。
