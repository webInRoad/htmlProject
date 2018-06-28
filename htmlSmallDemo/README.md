# 说明
通过实例说明一些css特性  
- border实现小箭头，border设置的其实默认就是**三角形**，平日是由于1像素所以看起来是直线
	
	```
		.container:before{
			content: '';
			border: 10px solid transparent;
			border-right-color:#B03C7C;
		}
	```
- li实现导航(li.html与固定位置的导航条.html)
	
	- 如果不实现a:hover效果，而让内容填充的话，就在li上设置padding
	
	```
	.top-menu ul li{
	    background-color: #efe5d0;
	    padding: 5px 10px;
	    margin: 0 5px;
	}
	```
	- 如果要实现a:hover效果，则只能将a设置为块状元素
	
	```
	li{
		list-style-type: none;
		float: left;
		width: 50px;
		height: 30px;
		line-height:30px;
		text-align: center;
	}
	a{
		display:block;
		/* 由于a标签属于内联元素，无高度和宽度属性，因此控制鼠标经过状态改变背景颜色时，仅在有文字的地方显示背景颜色。解决的办法是把a标签变为块级元素，display:block */
	}
	a:link,a:visited{
		text-decoration: none;
		color:black;
	}
	a:hover,a:active{
		text-decoration: none;
		color: white;
		background: #BE3948;
		/*display: block;*/
	}
	```
- overflow:hidden
	隐藏border边框外面的部分(截取的长度是内容长度加上padding长度)
- background
	背景颜色不包含border区域，即是border以内(与overflow范围一致)
- float
	如果前一个盒子剩余的宽度不够，会***再***前一个贴边
- 清除浮动
	[总共6种法子](清除浮动.html "清除浮动的方法")
	最常用的(设置:after伪类)
		
		```
		.box1:after{
			display: block;
			content: '';
			clear: both;
		}
		```
- text-align 与 align="center"的区别
	text-align是指元素里的**内容**居中
	align="center"是指元素里的**元素**(像图片等)居中
- 子元素定位到父元素正中央(子相父绝，并设置left为50%,以及margin-left为子元素(width+padding\*2+border\*2)/2)
	
```
.parent{
	width: 300px;
	height: 200px;
	background-color: #ADD8E5;
	border:20px solid #ccc;
	padding:20px;
	position: relative;
}
.son{
	width: 200px;
	height: 40px;
	padding: 0 20px;
	border:1px solid #ddd;
	background-color: pink;
	position: absolute;
	bottom: 100px;
	left:50%;
	margin-left: -121px;/*(200+20*2+1*2)/2*/
}
```