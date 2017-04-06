update--20151208


@charset "utf-8";
/*reset*/
/*body,ol,ul,h1,h2,h3,h4,h5,h6,p,th,td,dl,dd,form,input,textarea,select,p,iframe{margin:0;padding:0;}*/
body, dl, dd, h1, h2, h3, h4, h5, h6, p, form{margin:0;padding:0;} 
ol,ul{margin:0; padding:0;}
label,input {display: inline-block;vertical-align: middle;}
li{list-style: none;}
a{text-decoration: none;/*display:inline-block;*/ color: #000;}
p.text{text-indent:2em;}
body{background: #fff;font-family:"Open Sans Light","Helvetica","Microsoft Yahei","Arial","Microsoft Jhenghei","sans-serif","Tahoma","宋体","SourceHanSerifSC“;} //增加思源宋体


"Open Sans Light","Microsoft Jhenghei","Helvetica","Microsoft Yahei","Arial","sans-serif","Tahoma"


英文字体
        'Open Sans Light',Helvetica,Arial,sans-serif,Cambria

数字Lucida Sans


字体   
webkit私有属性高级修饰
-webkit-font-smoothing:antialiased;（貌似没区别）-webkit-text-stroke: 2px #fff

'Helvetica Neue', Arial, 'Hiragino Sans GB'


font-family:'Microsoft Jhenghei','Microsoft Yahei','Helvetica Neue','Consolas','arial','Michroma','Segoe UI Light','Segoe UI','sans-serif','Times';




a:link,a:visited{}
a:hover,a:active{}
.clearfix:after { 
  content:"\200B"; 
  display:block; 
  height:0; 
  clear:both; 
} 
.clearfix {*zoom:1;}/*IE/7/6*/


 /*处理li边框重叠问题*/
li{border:1px solid #ccc;
    margin-top: -1px;
    margin-left: -1px;
}

div {
width:-webkit-calc(100%-100px);
width:-moz-calc(100%-100px);
width:calc(100%-100px);
}
div {
    width:100%;
    box-sizing:border-box;
    border-left:100px solid transparent;
}


/*移动端*/

控制用户能不能选择页面中的文本，能否对页面文本进行编辑
/*只能读*/
.read-only {
  -webkit-user-modify:read-only;
  -moz-user-modify:read-only;
  user-modify:read-only;
}
/*可读可写*/
.read-write {
  -webkit-user-modify: read-write;
  -moz-user-modify: read-write;
  user-modify: read-write;
}

覆盖层介绍层透明
滑过时 覆盖层显示，背景层被遮挡
a.cover{opacity: 0;}

a.cover:hover{    opacity: 1;
    transition: all 0.5s ease-out;
    -webkit-transition: all 0.5s ease-out;
    -moz-transition: all 0.5s ease-out;
    -o-transition: all 0.5s ease-out;}

css3子选择器表格第一列
.tab4 tr td:nth-child(1){text-align:left;padding-left:2em;}
  
/************* 展示位置    *****************/

长英文或者长字段换行写法总结如下:

需要了解的3个属性
1.word-wrap:break-word 词内换行 只支持连续的英文和数字，在表格中失效
2.word-break:break-all 边界内换行 支持包括英文和数字的词句短，在火狐中失效
3.table-layout:fixed 固定表格 启动该属性可在表格中支持word-wrap:break-word;overflow:hidden

普通容器中（Div）的用法建议
word-wrap:break-word;

容器中（Div）中的表格的用法建议
table-layout:fixed;word-wrap:break-word;

table{table-layout: fixed;word-wrap:break-word;}


固定比例或具体值大小的用
box-sizing: border-box; 来限制容器大小


.p-a { position: absolute;}
.p-r { position: relative;}
.over { overflow: hidden;}
.t-over { text-overflow: ellipsis; white-space: nowrap;overflow: hidden;}   /*****  不允许断行  ，超出用  ......  代替   *****/
.t-ovr { white-space: nowrap;}  /** 不允许断行   */
.t-num{text-wrap: none; word-break: normal; }/* 数字不断行 */
.t-letter{word-break: normal;}/* 单词不断行 */
.box-justify { -webkit-box-pack:justify; }

垂直居中
display: table-cell;vertical-align: middle;
  vertical-align: baseline;



文字换行
word-wrap:break-word;word-break:break-all;
text-overflow:clip | ellipsis;超出容器部分裁剪/用省略号显示


/*多行超出固定高度！！！！！部分。。。显示*/
text-overflow: -o-ellipsis-lastline;overflow: hidden;
text-overflow: ellipsis;display: -webkit-box;-webkit-line-clamp: 2;-webkit-box-orient: vertical;




首字突出显示
p:first-letter {float:left;font-size:40px;font-weight:bold;}
p:first-line {color:#090;}

让html里的<script>标签内脚本显示
script{display:block;margin:5px ;padding:5px;box-shadow:0px 0px 9px 3px #111;background:#111;color:#fff;padding-left:2em}

表单标签垂直对齐
label,input {
    display: inline-block;
    vertical-align: middle;
    /**display:inline;   兼容低版本ie
    *zoom: 1;
    *vertical-align: auto;*/
}

/*蒙版*/
.mengban{display:none;position:fixed;z-index:3000;top:0;left:0;width:100%;height:100%;background: rgb( 0, 0,0);background-color:rgba(0,0,0,0.7);filter:alpha(opacity=70); opacity:0.7;}



/*弹窗*/

    height: 8em;
    width:6em;
    left: 50%;top:50%;
    margin-left: 3em;
    margin-top: -4em;
    position: fixed;
    text-align: center;
    ovfolw:auto;
   



/*--------------清除浮动-------------*/
<style>
.clearfix:before,.clearfix:after { content:""; display:table; }
.clearfix:after {clear: both; }
.clearfix {zoom:1;}
</style>

/*清除浮动代码*/
.clearfloat:after{display:block;clear:both;content:"";visibility:hidden;height:0}
.clearfloat{zoom:1} 

/*清除浮动代码史*/
http://www.admin10000.com/document/6259.html

　终极版一：

.clearfix:after { 
  content:"\200B"; 
  display:block; 
  height:0; 
  clear:both; 
} 
.clearfix {*zoom:1;}/*IE/7/6*/

　　解释下:content:"\200B";这个参数，Unicode字符里有一个“零宽度空格”，即 U+200B，代替原来的“.”，可以缩减代码量。而且不再使用visibility:hidden。

　　终极版二：

.clearfix:before,.clearfix:after{ 
    content:""; 
    display:table; 
} 
.clearfix:after{clear:both;} 
.clearfix{ 
    *zoom:1;/*IE/7/6*/
}
　　这两个终极版代码都很简洁，终极版一和二都可以使用，以上代码都经过测试，大家赶紧用一下吧，如果有什么问题请及时跟我反馈，如果你还停留在clearfix的老代码的时候就赶紧更新一下代码吧。

在浮动的父元素加overflow: auto;父元素高度撑起来

<ul class="clearfix">
<li style="float:left">test float</li>
</ul>
<div>after div</div>
/*------------------------------*/



/*css3动画渐变按钮*/
http://zurb.com/playground/radioactive-buttons

@-webkit-keyframes greenPulse {
  from { background-color: #ccc; -webkit-box-shadow: 0 0 9px #fff;}
  50% { background-color: #c81623; -webkit-box-shadow: 0 0 18px #c81623;}
  to { background-color: #ccc; -webkit-box-shadow: 0 0 9px #fff;}
}
.xy_order_btnpay{width:120px;font-size:16px;font-weight:bold;border:none;color:#fff;background-color: #c81623;
height:35px;line-height:35px;cursor:pointer;border-radius:4px; 
 -webkit-animation-name: greenPulse;
  -webkit-animation-duration: 3s;-webkit-animation-iteration-count: infinite;}



过渡场景
hover滑过

    -webkit-transition: all .1s ease-out;
    -moz-transition: all .1s ease-out;
    -o-transition: all .1s ease-out;
    -ms-transition: all .1s ease-out;
    transition: all .1s ease-out;


蒙版模糊效果
    -webkit-filter: blur(3px);
    -moz-filter: blur(3px);
    -o-filter: blur(3px);
    -ms-filter: blur(3px);
    filter: blur(3px);


@media (min-width: 2012px) and (max-width:2249px) {
    .container-fluid {
        width:2000px
    }
    
    #left-div~#container-div {
        margin-left: 12.5%;
        width: 87.5%
    }
}


动画帧
@keyframes spin {
    0% {
        -webkit-transform: rotate(0);
        transform: rotate(0)
    }
    
    100% {
        -webkit-transform: rotate(360deg);
        transform: rotate(360deg)
    }
}

@-webkit-keyframes spin {
    0% {
        -webkit-transform: rotate(0)
    }
    
    100% {
        -webkit-transform: rotate(360deg)
    }
}

@-moz-keyframes spin {
    0% {
        -webkit-transform: rotate(0);
        transform: rotate(0)
    }
    
    100% {
        -webkit-transform: rotate(360deg);
        transform: rotate(360deg)
    }
}

@-ms-keyframes spin {
    0% {
        -webkit-transform: rotate(0);
        transform: rotate(0)
    }
    
    100% {
        -webkit-transform: rotate(360deg);
        transform: rotate(360deg)
    }
}

@-o-keyframes spin {
    0% {
        -webkit-transform: rotate(0);
        transform: rotate(0)
    }
    
    100% {
        -webkit-transform: rotate(360deg);
        transform: rotate(360deg)
    }
}

动画
.spin {
    animation: spin 1s linear 10ms infinite;
    -webkit-animation: spin 1s linear 10ms infinite;
    -moz-animation: spin 1s linear 10ms infinite;
    -ms-animation: spin 1s linear 10ms infinite;
    -o-animation: spin 1s linear 10ms infinite
}

渐变
.bai-bg a:hover {
    background-image: -webkit-linear-gradient(top,#f7f7f7,#f6f6f6,#f5f5f5);
    background-image: -moz-linear-gradient(top,#f7f7f7,#f6f6f6,#f5f5f5);
    background-image: -ms-linear-gradient(top,#f7f7f7,#f6f6f6,#f5f5f5);
    background-image: -o-linear-gradient(top,#f7f7f7,#f6f6f6,#f5f5f5)
}



表单

<input class="11" type="text" value="256" maxlength="76">
时时改变网页显示
http://jingyan.baidu.com/article/8ebacdf0300f4c49f65cd51f.html
.exp-image-wraper img{position:relative;transform:rotate(90deg) scale(0.8,0.8);}

背景颜色渐变
body{
    font-size: 16px;color: #fff;font-family:'Microsoft Jhenghei','Microsoft YaHei','Arial','sans-serif';text-shadow:1px 1px 1px rgba(0,0,0,1);
    background: #333; /* Old browsers */
    background: -moz-linear-gradient(left, #222 0%, #999 100%); /* FF3.6+ */
    background: -webkit-linear-gradient(left, #222 0%,#999 100%); /* Chrome10+,Safari5.1+ */
    background: -o-linear-gradient(left, #222 0%,#999 100%); /* Opera11.10+ */
    background: -ms-linear-gradient(left, #222 0%,#999 100%); /* IE10+ */
    background: linear-gradient(left, #222 0%,#999 100%); /* W3C */
  background:url("img/bg.png");
    background-attachment: fixed;
    background-size: cover;
}
        background: -webkit-linear-gradient(top, #000 25%,#fff 75%);
        /*top指的是从上向下线性渐变，left即从左到右，25%指的是从自上而下高度的1/4长度开始，75%结束*/

背景图片
background:url(xxx/1.jpg);
background-color:rgba(88,200,100,0.7);
background-repeat: no-repeat;
}

圆角边框和阴影
        border-radius: 3px;
        box-shadow: 0 1px 2px rgba(0,0,0,0.2);

/*模糊*/
-webkit-filter: blur(5px); 
    -moz-filter: blur(5px);
    -mz-filter: blur(5px);
    -o-filter: blur(5px);
opacity:1;
-webkit-transition: opacity 1.5s ease;
transition: opacity 1.5s ease;

/*css3字体光滑*/
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
/*    CSS3中用于webkit引擎(如chrome)中设置字体的抗锯齿或者说光滑度的属性。
有3个属性：none用于小像素的文本、subpixel-antialiased浏览器默认的、antialiased反锯齿。*/

/*设置元素透明度*/
兼容ie
http://blog.csdn.net/jiudihanbing/article/details/8372947

兼容ie8的rgba
http://my.oschina.net/CodingPeasant/blog/515234
/*ie 透明滤镜*/
filter:Alpha(opacity=50)  兼容ie678

filter: progid:DXImageTransform.Microsoft.Alpha(opacity=70);

/*ie 渐变滤镜*/
filter:alpha(opacity=60)progid:DXImageTransform.Microsoft.gradient(startColorstr=#ffffff,endColorstr=#A9A9A9,GradientType:0;);
/* 全站黑白滤镜*/
html { filter:progid:DXImageTransform.Microsoft.BasicImage(grayscale=1); }
background:transparent;
filter: progid:DXImageTransform.Microsoft.gradient(startColorstr=#66ffffff,endColorstr=#66ffffff);

opacity:0.5; 支持ie9及以上 规定不透明度级别。从0完全透明）到 1.0（完全不透明）
filter: progid:DXImageTransform.Microsoft.Alpha(opacity=70);

IE8 以及更早的版本支持替代的 filter 属性。例如：filter:Alpha(opacity=50)
.iefilter{opacity: 0.6;filter:alpha(opacity=60);}
.ao_rightside{filter:progid:DXImageTransform.Microsoft.gradient(startColorstr=#66ffffff,endColorstr=#6687CEEB);}
.ao_items{filter:progid:DXImageTransform.Microsoft.gradient(startColorstr=#7fffffff,endColorstr=#7fffffff);}

.mainy{filter:progid:DXImageTransform.Microsoft.gradient(enabled='true',startColorstr='#CC000000', endColorstr='#CC000000');}
/*:root css3选择器，来避免IE9浏览器中的滤镜filter和rgba同时支持时的冲突*/
:root .mainy {filter:none;background-color:rgba(0,0,0,0.8);}




<img src ="planets.gif" alt="Planets" usemap ="#planetmap" />
<map name="planetmap">
  <area shape="rect" coords="0,0,110,260" href="sun.htm" alt="Sun" />
  <area shape="circle" coords="129,161,10" href="mercur.htm" alt="Mercury" />
  <area shape="circle" coords="180,139,14" href="venus.htm" alt="Venus" />
</map>


/*emmet语法*/



.xy_order_btnpay:hover{transition:1s;background-color:red}
 @-webkit-keyframes greenPulse {
  from { background-color: #ccc; -webkit-box-shadow: 0 0 9px #fff;}
  50% { background-color: #c81623; -webkit-box-shadow: 0 0 18px #c81623;}
  to { background-color: #ccc; -webkit-box-shadow: 0 0 9px #fff;}
}
.xy_order_btnpay{width:120px;font-size:16px;font-weight:bold;border:none;color:#fff;background-color: #c81623;
height:35px;line-height:35px;cursor:pointer;border-radius:4px; 
 -webkit-animation-name: greenPulse;
  -webkit-animation-duration: 3s;-webkit-animation-iteration-count: infinite;}

/*css3 animate 属性*/
  -webkit-animation-name:'wobble';/*动画属性名即 keyframes定义的动画名*/
  -webkit-animation-duration: 10s;/*动画持续时间*/
  -webkit-animation-timing-function: ease-in-out; /*动画频率，和transition-timing-function是一样的*/
  -webkit-animation-delay: 2s;/*动画延迟时间*/
  -webkit-animation-iteration-count: 10;/*定义循环资料，infinite为无限次*/
  -webkit-animation-direction: alternate;/*定义动画方式*/

animation:wobble 10s ease-in  2s 10 both;


animation-name
animation-duration
animation-timing-function
animation-delay
animation-iteration-count
animation-direction


css3动画保留最后帧
-webkit-animation-fill-mode: forwards;
animation-fill-mode: forwards;
-webkit-animation-iteration-count: infinite;
animation-iteration-count: infinite
