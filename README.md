# jQuery-banner使用手册 #

#### 当前版本：v1.2.0 beta ####

### jQuery-banner是什么？###
>jQuery-banner是一款基于jQuery库开发的轻量级轮播插件，方便开发者快速完成针对页面轮播效果的开发，并获得不同的轮播效果。例如，水平滑动或垂直滑动，以及淡出淡入或切换等！（适用于常规banner、照片大图预览幻灯片切换效果、滚屏效果等）此插件的当前版本为 V1.1。本插件由lzmoop（磨盘兄弟）提供的免费开源插件。


### 具体参数列表###
 <div id="csBg">
    <table>
        <thead>
            <tr>
                <th>参数名称</th>
                <th>参数取值</th>
                <th>参数说明</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>动画效果:</td>
                <td>
                    '[left]' / '[right]' / '[up]' / '[down]' / '[fade]' / '[cut]'
                </td>
                <td>
                    本参数为空时：默认值为 left 本参数可省略
                </td>
            </tr>
            <tr >
                <td>间隔时间：</td>
                <td>'[slow]' / '[medium]' / '[fast]' / [number]</td>
                <td>
                    本参数为空时：默认值为 medium 即 3000 本参数可省略
                </td>
            </tr>
            <tr>
                <td>动画速度:</td>
                <td>'[slow]' / '[medium]' / '[fast]' / [number]</td>
                <td>当参数不是自定义数字时应省略</td>
            </tr>
            <tr>
                <td>是否自动：</td>
                <td>[true] / [false]</td>
                <td>本参数为空时：默认自动播放,只能用对象{'auto':true/false}传参</td>
            </tr>
            <tr>
                <td>是否循环:</td>
                <td>[true] / [false]</td>
                <td>本参数为空时：默认循环播放,只能用对象{'cycle':true/false}传参</td>
            </tr>
            <tr>
                <td colspan="3">
                    调用函数：$(selector/object).banner([animation],[interval],[duration]);或以对象的方法传参，示例参考下方代码片段。[] 表示参数可省略
                </td>
            </tr>
        </tbody>
    </table>
</div>

### 引入库文件 ###

 -- 此插件基于jQuery开发

	<script src="js/jquery-11.1.1.min.js"></script>
	<script src="js/jquery-banner.1.2.0.min.js"></script>
	<link href="css/jquery-banner.css" rel="stylesheet" type="text/css">


### HTML代码片段 ###

 -- 页面上必须的html代码，保证外层框架结构相同，标记不限，内层结构不限
	
	<div id='selector'>
		<ul>
			<li><a href="#"><img src="images/01.png"></a></li>
			<li><a href="#"><img src="images/02.png"></a></li>
			<li><a href="#"><img src="images/03.png"></a></li>
		</ul>
	</div>

### 调用插件 ###

-- 参数可为空，全部参数请参考列表；可多次调用

	<script type="javascript">
	<!--
		$('#banner').banner('fade',3000,600) //效果 间隔时间 运行速度 

		/* 或使用对象传参 */

		$('#banner').banner({
			effect : 'down' ,
			intervalue : 3000 ,
			speed : 600 ,
			auto : true ,//默认自动
			cycle : true//默认循环
		})
	-->
	</script>

### 官方提供的选择器 ###

-- 自定义样式时请带上外层父级id，避免同一页面多个组件样式冲突

	.jquery-bannerImg  /* banner外层框架 */
	.jquery-bannerImg-images  /* banner的运动层 */
	.jquery-bannerBtn  /* banner左右控件的盒子 */
	.jquery-bannerBtn-left  /* banner的向左控件 */
	.jquery-bannerBtn-right  /* banner的向右控件 */
	.jquery-bannerPoint  /* banner的焦点按钮盒子 */
	.jquery-bannerPoint-point  /* banner的焦点按钮 */
	.jquery-bannerPoint-hover  /* 控制banner的焦点按钮选中时的样式 */

 - © 本手册由 磨盘兄弟 @lzmoop 官方提供 
