DomEvent
===================
### 一、描述   
工具方法，主要用于Dom的事件操作，被用于Leaflet内部。  
### 二、方法  
(1)增加事件监听：  	
`addListener(el, type, fn, context)`    
  
	el：增加事件监听的元素，即HTML Element  
	type：事件的类型，如click 
	fn:事件处理函数  
	context: 上下文环境   
(2)移除事件监听：
`removeListener(el, type, fn)`  

	el: 需要移除事件监听的元素
	type: 需要移除的事件类型
	fn: 引用的事件处理函数 
（3）阻止事件冒泡：
`stopPropagation(e)`

	e: DomEvent 
	阻止事件冒泡到父元素，例如：
	L.DomEvent.addListener(div, 'click', function (e) {
	    L.DomEvent.stopPropagation(e);
	});
（4）阻止默认事件：
`preventDefault(e)`

	阻止默认的事件触发，如a href、input submit的触发，这个函数主要内部使用。

（5）同时阻止冒泡 & 默认事件：
`stop（e）`    
`同时调用stopPropagation和preventDefault。`    
（6）阻止Click的事件冒泡：
`disableClickPropagation(el)`

	el: HTML Element
	主要用于的事件类型是：'click'， 'doubleclick'， 'mousedown'，'touchstart'
（7）获取鼠标的位置：
`getMousePosition(e, container)`

	e: Dom Event
	container:设置的容器
	获取，当前容器内鼠标的位置，如果不是给定了container，默认就是整个页面。
（8）获取滚轮的角度：
`getWheelDelta(e)`

	e: Dom Event
	当发生鼠标滚轮事件时，获取角度。