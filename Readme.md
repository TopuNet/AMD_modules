# AMD_modules
###符合AMD规范的模块集

项目索引：
-------------

[goto_top](#goto_top)：监听窗口滚动位置 → 决定是否显示“返回顶部按钮”；并监听按钮的点击事件 → 返回窗口到顶部。（不含样式）

[window_resize](#window_resize)：监听窗口的resize事件

<a name="goto_top"></a> 
###goto_top：
		// button_selector: 按钮选择器
		return function(button_selector) {};

<a name="window_resize"></a>
###window_resize：
		// callback: 回调函数
		return function(callback) {};
