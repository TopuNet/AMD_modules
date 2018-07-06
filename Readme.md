# AMD_modules
### 符合AMD规范的模块集 
### 安装：npm instll TopuNet-AMD-modules

项目索引：
-------------

[debug](#debug)：debug模块

[goto_top](#goto_top)：监听窗口滚动位置 → 决定是否显示“返回顶部按钮”；并监听按钮的点击事件 → 返回窗口到顶部。（不含样式）

[window_resize](#window_resize)：监听窗口的resize事件

[background_change](#background_change)：切换body大背景

<a name="debug"></a>
#### debug：

```javascript
require(['debug'],function($debug){
	$debug.debug(msg);
	$debug.log(msg);
	$debug.warn(msg);
	$debug.error(msg);
});
```

<a name="goto_top"></a> 
#### goto_top：

```javascript
require(['jquery/zepto','goto_top'],function($,$goto_top){
	$goto_top({
		button_selector: "body", // 按钮元素选择器，建议在样式表中默认设为隐藏。默认"body"
	    panel_selector: "div.box", // 外盒元素选择器（根据此元素滚动距离决定按钮是否显示(当滚动距离大于等于窗口的1/3时显示)；点击按钮后此元素的scrollTop滚至0）。默认window
	    durTime_ms: 200, // 点击按钮后，外盒scrollTop滚至0的时间，毫秒。默认200
	    callback_success: function(){} // 滚动完成后的回调方法
	});
});
```

<a name="window_resize"></a>
#### window_resize：

```javascript
require(['jquery/zepto','window_resize'],function($,$window_resize){
	$window_resize(function(){
		// resize后的回调
	});
});
```

<a name="background_change"></a>
#### background_change：

```javascript
// 盒子的数量不能多于图片的数量
require(['jquery/zepto','background_change'],function($,$background_change){
	$background_change({
		obj_arr : [],		//判定变换背景的盒子名称的数组，
		src_arr : []		//背景路径数组
	})
});
```
		
		
