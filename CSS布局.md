# CSS 布局

###display
`display: none | block | inline` <br/>
`none:` 隐藏对象，与visibility属性的hidden值不同，其不为被隐藏的对象保留其物理空间。<br/>
`inline`: 指定对象为内联对象<br/>
`block`: 指定对象为块元素
###float
`float: none| left| right`<br/>
`none`:设置对象不浮动<br/>
`left`:设置对象浮动在左边<br/>
`right`: 设置对象浮动在右边<br/>
说明：当属性不等于none引起对象浮动时，对象将被视为块对象，即display属性等于block，也就是说浮动对象的display特性将被忽略。

###clear
`clear: none | left | right | both`<br/>
`none`: 允许两边都可以有浮动对象<br/>
`left`:不允许左边有浮动对象<br/>
`right`: 不允许右边有浮动对象<br/>
`both`: 不允许有浮动对象
###visibility
`visibility: visible | hidden | collapse`<br/>
`visible`: 设置对象为可见对象<br/>
`hidden`: 设置对象为隐藏<br/>
`collapse`: 主要用来表格的行或列。隐藏的行或列能够被其他内容使用，对于表格外的其他对象，其作用等同于hidden。<br/>
与`display`不同的是，此属性为隐藏的对象保留其占据的物理空间。如果希望对象为可视，其父对象也必须是可视的。
###clip
`clip:auto | rect(<number> | auto <number> | auto <number> | auto <number> | auto)`<br/>
`auto`:对象无剪切<br/>
`rect`: 根据上上-右-下-左的顺序提供子对象左上角为(0,0)坐标计算的四个编译数值，其中任一数值都可以用auto奇幻，即此边不剪切。<br/>
说明：检索或设置对象的可视区域，区域外的部分是透明的。必须将position的值设为absolute此属性方可使用。

###overflow
`overflow: <overflow-style>{1,2}`<br/>
`<overflow-style> = visible | hidden | scroll | auto`<br/>
`visible`: 不剪切内容<br/>
`hidden`: 将超出对象尺寸的内容进行剪裁，将不出现滚动条<br/>
`scroll`: 将超出对象尺寸的内日用进行剪裁，并以滚动条的方式显示出超出的内容<br/>
`auto`: 在需要时剪切内容并添加滚动条，此为body对象和textarea的默认值<br/>
说明：检索或设置当对象的内容超过其指定高度及宽度时如何管理内容。对于table来说，假如table-layout属性设置为fixed，则td对象支持带有默认值为hidden的overflow属性。如果设为hidden，scroll或者auto，那么超出td尺寸的内容将被剪切。如果设为visible，将导致额外的文本溢出到右边或左边（视direction属性设置而定）的单元格。

###overflow-x
`overflow-x: <overflow-style>`<br/>
`<overflow-style> = visible | hidden | scroll | auto`<br/>
说明：设置或检索当对象的内容超过其指定宽度时如何管理内容。

###overflow-y
`overflow-y: <overflow-style>`<br/>
`<overflow-style> = visible | hidden | scroll | auto`<br/>
说明：设置或检索当对象的内容超过其指定高度时如何管理内容。

