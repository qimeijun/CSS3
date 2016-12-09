###一、引入外来字体

```
@font-face{
    font-family: fontname;
    src: url("Sansation_Light.ttf"),url("Sansation_Light.eot")/* IE9+ */
}
```

###二、文字倒影
box-reflect: 方向 间距 渐变效果<br/>
方向：above、below、left、right<br/>
间距：倒影与文件之间的距离<br/>
`box-reflect: below 1px linear-gradient(transparent, transparent 50%, rgba(0,0,0,3));`

###三、文字阴影
`text-shadow: 2px 2px 4px green;`

###四、文字描边
`-webkit-text-stroke: 3px green;
text-stroke: 1px green;`
只支持-webkit 核心


###五、处理字体溢出
```
display: bloack;
width: 200px;
white-space: nowrap; /*不换行*/
text-overflow: ellipsis;/*多余文本换成省略号*/
overflow:hidden; /*多余文字隐藏*/
```


###六、背景大小
`background-size: auto 100%` 表示全屏， 相当于`background-size: cover`

###七、颜色渐变
```
background: -webkit-linear-gradient(left, red, orange, yellow, green, blue, indigo, violet);
background: -o-linear-gradient(left, red, orange, yellow, green, blue, indigo, violet);
background: -moz-linear-gradient(left, red, orange, yellow, green, blue, indigo, violet);
background: linear-gradient(left, red, orange, yellow, green, blue, indigo, violet);
```

```
background: -webkit-radial-gradient(left, red 5%, green 15%, blue 60%);
background: -o-radial-gradient(left, red 5%, green 15%, blue 60%);
background: -moz-radial-gradient(left, red 5%, green 15%, blue 60%);
background: radial-gradient(left, red 5%, green 15%, blue 60%);
```


###八、3D 旋转
rotate3d(x, y, z, 旋转角度)<br/>
```
-webkit-transform: rotate3d(1, -1, 0, 60deg);
-o-transform: rotate3d(1, -1, 0, 60deg);
-moz-transform: rotate3d(1, -1, 0, 60deg);
-ms-transform: rotate3d(1, -1, 0, 60deg);
transform: rotate3d(1, -1, 0, 60deg);
```

###九、清除浮动
1、使用`clear:  left、right、both`<br/>
`clear:left` 表示左边不能出现浮动<br/>
`clear:right`  表示右边不能出现浮动<br/>
`clear:both` 表示两边都不能出现浮动<br/>
2、对父类元素使用`:after`伪类<br/>
```
.clearfix:after {
    content: '020';
    display: black;
    height: 0;
    clear: both;
}
```
