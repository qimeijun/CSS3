#CSS边框
###background
`background: [background-color] || [background-image] || [background-repeat] || [background-attachment] || [background-position]`<br/>
说明：复合属性，设置对象的背景特性。

###background-color
`background-color:<color>`<br/>
说明：设置或检索对象的背景颜色

###background-image
`background-image:<bg-image>[, <bg-image>]`<br/>
`<bg-image> = none | <url> | <linear-gradient> | <radial-gradient> | <repeating-linear-gradient> | <repeating-radial-gradient>`<br/>
`none`: 无背景图<br/>
`<url>`: 使用绝对或相对地址指定背景图像<br/>
`<linear-gradient>:`使用线性渐变创建背景图像<br/>
`<radial-gradient>:`使用径向（放射性）渐变创建背景图像<br/>
`<repeating-linear-gradient>:`使用重复的线性渐变创建背景图像<br/>
`<repeating-radial-gradient>:`使用重复的径向渐变创建背景图片<br/>
说明：设置或检索对象的背景图像
###background-repeat
`background-repeat:<repeat-style> [ , <repeat-style> ]*`<br/>
`<repeat-style> = repeat-x | repeat-y | [repeat | space | round | no-repeat]{1,2}`
`repeat-x`：背景图像在横向上平铺<br/>
`repeat-y`：背景图像在纵向上平铺<br/>
`repeat`：背景图像在横向和纵向平铺<br/>
`no-repeat`：背景图像不平铺<br/>
`round`：背景图像自动缩放直到适应且填充满整个容器。（CSS3）<br/>
`space`：背景图像以相同的间距平铺且填充满整个容器或某个方向。（CSS3）<br/>
说明：设置或检索对象的背景如何铺排填充。必须先指定background-image属性
###background-attachment
`background-attachment:<attachment> [ , <attachment> ]*`<br/>
`<attachment> = fixed | local | scroll`<br/>
`fixed：`背景图像相对于窗体固定。<br/>
`scroll：`背景图像相对于元素固定，也就是说当元素内容滚动时背景图像不会跟着滚动，因为背景图像总是要跟着元素本身。但会随元素的祖先元素或窗体一起滚动。<br/>
`local：`背景图像相对于元素内容固定，也就是说当元素随元素滚动时背景图像也会跟着滚动，因为背景图像总是要跟着内容。（CSS3）<br/>
说明：设置或检索背景图像是随对象内容滚动还是固定，必须先指定background-image属性
###background-position
`background-position:<bg-position> [ , <bg-position> ]*`<br/>
`<bg-position> = [ <percentage> | <length> | left | center① | right ] [ <percentage> | <length> | top | center② | bottom ]?`<br/>
`<percentage>`：用百分比指定背景图像填充的位置。可以为负值。<br/>
`<length>`：。可以为负值。<br/>
`left`：背景图像在横向上填充从左边开始。<br/>
`center①`：背景图像在横向上填充从中间开始。<br/>
`right`：背景图像在横向上填充从右边开始。<br/>
`top`：背景图像在纵向上填充从顶部开始。<br/>
`center`：背景图像在纵向上填充从中间开始。<br/>
`bottom`：背景图像在纵向上填充从底部开始。<br/>
说明：设置或检测对象的背景图像位置。必须先指定background-image
###background-origin
`background-origin:<box> [ , <box> ]*`<br/>
`<box> = border-box | padding-box | content-box`<br/>
`padding-box：`从padding区域（含padding）开始显示背景图像。<br/>
`border-box：`从border区域（含border）开始显示背景图像。<br/>
`content-box：`从content区域开始显示背景图像。<br/>
说明：设置或检测对象的背景图像计算background-position时的参考原点
###background-clip
`background-clip:<box> [ , <box> ]*`<br/>
`<box> = border-box | padding-box | content-box | text`<br/>
`padding-box`：从padding区域（不含padding）开始向外裁剪背景。<br/>
`border-box`：从border区域（不含border）开始向外裁剪背景。<br/>
`content-box`：从content区域开始向外裁剪背景。<br/>
`text`：从前景内容的形状（比如文字）作为裁剪区域向外裁剪，如此即可实现使用背景作为填充色之类的遮罩效果<br/>

###background-size
`background-size:<bg-size> [ , <bg-size> ]*`<br/>
`<bg-size> = [ <length> | <percentage> | auto ]{1,2} | cover | contain`<br/>
`<length>：`用长度值指定背景图像大小。不允许负值。<br/>
`<percentage>：`用百分比指定背景图像大小。不允许负值。<br/>
`auto：`背景图像的真实大小。<br/>
`cover：`将背景图像等比缩放到完全覆盖容器，背景图像有可能超出容器。<br/>
`contain：`将背景图像等比缩放到宽度或高度与容器的宽度或高度相等，背景图像始终被包含在容器内。<br/>
