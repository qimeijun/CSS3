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

###十、服务商前缀
```
-webkit  webkit核心浏览器， 包括Chrome, Safari等
-ms      IE浏览器
-o       Opera浏览器
-moz     火狐浏览器
```

通常在解决兼容性的时候，一般把服务商前缀的属性放在前面，W3C的标准属性放在最后面，这样即使出现不一致的情况，后书写的符合W3C标准的属性，会覆盖前面带有属性前缀的定义。


###十一、弹性盒子布局
弹性盒子布局相对于传统的div float 布局方式要简单很多。目前支持的浏览器webkit核心、火狐、IE10<br/>

1、布局方式
```
.father {display: box;}
.son1{box-flex: 1}
.son2{box-flex: 3}
.son3{box-flex: 1}

<div class="father">
    <div class="son1"></div>
    <div class="son2"></div>
    <div class="son3"></div>
</div>
```
2、控制布局方向<br/>
在父元素中定义`box-orient:horizontal` ,来控制布局方向<br/>
horizontal、vertical、inline-axis、block-axis、inherit。<br/>

3、控制元素对齐方式<br/>
`box-align: start`<br/>
参数： start、end、center、baseline、stretch<br/>

4、控制元素顺序<br/>
`box-direction: reverse`<br/>
参数：normal、reverse、inherit<br/>

###十二、三种布局方式
1、最传统的布局方式---固定式布局<br/>
固定页面的宽度，一般在950/960像素，为了效果，通常使用栅格化系统，把页面分成N列，N 越多，页越灵活<br/>
```
.contianer {
    width: 960px;
}
```
2、流式布局<br/>
流式布局相对固定式布局而言要灵活许多，不会因为页面缩小而显示不全。<br/>
流式布局最大的特点：计算列百分比，在栅格化列宽是我们可以使用百分比来设置，而不是固定的像素了<br/>
```
.contianer {
    width: 100%
}
```
3、最流行的布局----响应式布局<br/>
不同的终端分辨率不一样，如何让页面在每个终端都能完美的展示，那就是使用响应式布局<br/>
特点：通过媒介查询<br/>
与流式布局唯一不同的就是通过媒介查询，根据不同的媒介，显示不同的效果<br/>
```
@media only screen {
    .contianer {
        width: 100%;
    }
}

@media only screen and (min-width: 40%) {
    .contianer {
        width: 90%;
    }
}
```
