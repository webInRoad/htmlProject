# 说明
这个项目是根据51CTO上的[HTML5和CSS3新特性视频教程](http://edu.51cto.com/course/3282.html?source=so)视频做的  
主要是采用html5结合css实现的星巴克首页(home.html)以及订购页面(form.html) 
## html相关技术点
	*video实现页面插入视频文件
		 
		```
		<video controls width="520" height="294">
            <source src="video/tweetsip.mp4">
            <source src="video/tweetsip.webm">
            <source src="video/tweetsip.ogv">
            <p>对不起，您的浏览器不支持video标签</p>
        </video>
		```
## CSS相关技术点
* 元素放置在页面正中央  

	```
	.wrap{
		width: 960px;	
    	margin: 0 auto;		
	}
	```
* 列表项水平显示
	*. 法1采用浮动
	
		```
		.top-menu ul li{
			float:left;
		}
		```
	*. 法2采用display:inline
		
		```
		.top-menu ul li{
			display:inline;
		}
		```
* 列表项有补白  
	![](images/nav.jpg 导航列表)
	
	```
	/*导航*/
	.top-menu{
	    float: left;
	    margin-top: 83px;
	    margin-left: 30px;
	}
	
	.top-menu ul li{
	    display: inline;
	    background-color: #efe5d0;
	    padding: 5px 10px;
	    margin: 0 5px;
	}
	
	.top-menu ul li.selected{
	    background-color: #c8b99c;
	}
	
	.top-menu ul li a:link, .top-menu ul li a:visited{
	    color: #006f47;
	    text-decoration: none;
	    font-weight: bold;
	}
	```

	
	
	


