# AMD_modules
### 符合AMD规范的模块集 
### 安装：npm instll TopuNet-AMD-modules

项目索引：
-------------

[goto_top](#goto_top)：监听窗口滚动位置 → 决定是否显示“返回顶部按钮”；并监听按钮的点击事件 → 返回窗口到顶部。（不含样式）

[window_resize](#window_resize)：监听窗口的resize事件

[background_change](#background_change)：切换body大背景

[judgeBrowserEdition](#judgeBrowserEdition)：判断ie低版本浏览器版本

<a name="goto_top"></a> 
###goto_top：
		/* 
			opt: {
				button_selector: "body", // 按钮元素选择器，建议在样式表中默认设为隐藏。默认"body"
		        panel_selector: "div.box", // 外盒元素选择器（根据此元素滚动距离决定按钮是否显示(当滚动距离大于等于窗口的1/3时显示)；点击按钮后此元素的scrollTop滚至0）。默认window
		        durTime_ms: 200, // 点击按钮后，外盒scrollTop滚至0的时间，毫秒。默认200
		        callback_success: function(){} // 滚动完成后的回调方法
			}
			依赖jquery@1.x 或 zepto
		*/
		return function(opt) {};

<a name="window_resize"></a>
###window_resize：
		// callback: 回调方法
		// 依赖jquery@1.x 或 zepto
		return function(callback) {};

<a name="background_change"></a>
###background_change：
		var _opt = {
			obj_arr : [],		//判定变换背景的盒子名称的数组，
			src_arr : []		//背景路径数组
		};
		依赖jquery@1.x 或 zepto 
		
		return background_change;
		注意：盒子的数量不能多于图片的数量

<a name="judgeBrowserEdition"></a>
###judgeBrowserEdition：
		//判断浏览器的版本
		//根据所船参数判断浏览器版本，参数值为0，IE7浏览器返回true，参数值为1，IE7,8,浏览器返回true，参数为其他值时，IE7,8,9,浏览器返回true
		//返回值 judgeBrowserEdition;
		//调用方法  judgeBrowserEdition({num:0});
		
		
