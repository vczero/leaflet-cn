DomUitl
===================
### 一、描述   
工具方法，主要用于Dom树的操作，被用于leaflet内部。
### 二、方法  
#####(1)get(id):获取一个元素
`id为字符串或者元素，如果是字符串将取得带有此ID的元素，如果是元素则直接返回`

#####(2)getStyle(el, style):获取一个元素的样式，包含通过CSS设置的。
	el:元素
	style：给定的样式名称

#####(3)create(tagName, className, container):创建一个元素
	tagName: 要创建的标签名称
	className: 样式的类名
	container: 父容器，如果存在父容器则存入，否则直接创建返回 
#####(4)disableTextSelection():阻止文字被选择，例如拖动地图的过程中，无法选择

#####(5)enableTextSelection():使文字能够重新被选择

#####(6)hasClass(el, name):元素的样式类中是否存在给定的类名
	el: 元素
	name: class name

#####(7)addClass(el, name):向元素类中增加一个样式类
	el: 元素
	name: 样式类名

#####(8)removeClass(el, name):移除一个元素的（给定）样式类
	el: 元素
	name: 样式类名

#####(9)setOpacity(el, value):设置元素的透明度
	el: 元素
	value: 透明度

#####(10)testProp(el, value):设置元素的透明度