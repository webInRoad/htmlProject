# 说明
## 技术点 
* 列表项前设置图标 
	* 法1:修改list-type-image属性

	```
	.top_content li{
		line-height: 27px;
		list-style-image: url('../images/li_bg.gif');
	}
	```
	* 法2:设置背景图片,并设置左边补白
		
	```
	.news_list li{
		background: url('../images/list.jpg') no-repeat;
		padding-left: 10px;
	}
	```
