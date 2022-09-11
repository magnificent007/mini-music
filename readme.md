### 初步猜测 u-cell 标签的url不能跳转到pages.json中已经设定的tabbar栏的vue组件
### 弹框登录可以不用popup组件，z-index和位置样式难以控制，可以用view包裹u-input和button，再放到遮罩层u-overlay标签里进行绝对定位，绝对定位的根据是父组件遮罩层，注意遮罩层组件的z-index：10070
### 对象判空的几种方法：1、.Object.getOwnPropertyNames()获取属性名返回一个数组；2、Object.keys()获取键值名返回一个数组
### uni开发过程中，uview的图片组件使用相对路径也就是 ../../../xxx的时候在hbuilder里可能就正常显示，但微信里显示不了 这时候就得使用觉得路径，也就是如果图片资源在你的根目录static文件夹下就直接 /static/xxx
### uview阻止默认点击事件 <view @tap.stop.prevent> 中间是点击事件 </view>
### uview路由接参两种方式：1、onLoad钩子默认参数option里直接点出传参 option.id；2、this.$route.query.id(亲测第二种手机报错)
### layout布局最好设置width：100%，否则页面左滑动右边出现留白
```
设置对象存键值
let obj = {};
this.$zaudio.audiolist = this.$zaudio.audiolist.reduce((item, next) => {
	// 判断下一个对象中的src路径是否在obj对象中是真值，是真值存在则为空并不给item数组 push对象
	// 为假不存在则设置该对象的src为obj的键值并设为真值，追加该对象到item中
	obj[next.src] ? '' : obj[next.src] = true && item.push(next);
	return item;
}, []);
```
