一、任何容器都可以指定flex布局<br>
  .box{<br>
    display:flex<br>
  }<br>
  Webkit内核的浏览器，必须加上-webkit前缀<br>
  .box{<br>
    display:flex;<br>
    display:-weblit-flex<br>
  }<br>
  注意：使用flex布局后，子元素的flaot、clear、vertical-align将失效<br>
二、flex布局的属性<br>
  1.flex-direction<br>
  2.flex-wrap<br>
  3.flex-flow<br>
  4.justify-content<br>
  5.aling-items<br>
  6.align-content<br>
三、属性介绍<br>
  1.flex-dirextion:决定项目的排列方向<br>
    .box{<br>
      flex-direction:row|row-reverse|column|column-reverse;<br>
    }<br>

    row(默认值):排列方向是水平方向，起点在左端<br>
    row-reverse:排列方向是水平方向，起点在右端<br>
    column:排列方向是竖直方向，起点在上沿<br>
    column-reverse:排列方向是竖直方向，起点在下沿<br>

  2.flex-wrap:决定是否换行以及如何换行<br>
    .box{<br>
      flex-wrap:nowrap|wrap|wrap-reverse;<br>
    }<br>

    nowrap(默认)：不换行<br>
    wrap:换行，第一行在上面<br>
    wrap-reverse:换行，第一行在下面<br>

  3.flex-flow:是flex-direction和flex-wrap属性的简写形式，默认是row和nowrap<br>

  4.justify-content:决定项目在主轴上的对齐方式<br>
    .box{<br>
      justify-content:flex-start|flex-end|center|space-between|space-around;<br>
    }<br>

    假设主轴是从左到右<br>

    flex-start(默认):左对齐<br>
    flext-end:右对齐<br>
    center:居中<br>
    space-between:两端对齐，项目之间的间隔都相等<br>
    space-around:每个项目的两侧相等<br>

  5.align-items:定义项目在交叉轴上如何对齐<br>
    .box{<br>
      align-items:flex-start|flex-end|center|baseline|stretch;<br>
    }<br>

    假设交叉轴从上到下<br>

    flex-start:交叉轴的起点对齐<br>
    flex-end:交叉轴的终点对齐<br>
    center:交叉轴的中点对齐<br>
    baseline:第一行文字的基线对齐<br>
    stretch(默认):如果项目没有设置height或设置成auto,将占满整个容器的高度<br>

  6.aling-content:定义多根轴线的对齐方式。如果只有一根轴线，则属性不起作用<br>
    .box{
      align-content:flex-start|flex-end|center|space-between|space-around|stretch;<br>
    }<br>

    flex-start:与交叉轴的起点对齐
    flex-end：与交叉轴的终点对齐
    center:与交叉轴的中点对齐
    space-between:与交叉轴的两端对齐，轴线之间的间隔平均分布
    space-around:每根轴线两侧的间隔相等
    stretch(默认):轴线占满整个交叉轴

  7.项目的属性<br>
    order：属性定义项目的排列顺序。数值越小，排列越靠前，默认为0。<br>
    flex-grow：属性定义项目的放大比例，默认为0，即如果存在剩余空间，也不放大。<br>
    flex-shrink：属性定义了项目的缩小比例，默认为1，即如果空间不足，该项目将缩小。<br>
    flex-basis：属性定义了在分配多余空间之前，项目占据的主轴空间（main size）。浏览器根据这个属性，计算主轴是否有多余空间。它的默认值为auto，即项目的本来大小.<br>
    flex:属性是flex-grow, flex-shrink 和 flex-basis的简写，默认值为0 1 auto。后两个属性可选。<br>
    align-self:属性允许单个项目有与其他项目不一样的对齐方式，可覆盖align-items属性。默认值为auto，表示继承父元素的align-items属性，如果没有父元素，则等同于stretch。<br>
