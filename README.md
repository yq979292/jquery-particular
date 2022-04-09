# jquery-particular
jq详解内容。从基础api .到模拟api 实现 模拟 jq库

## 什么是jquery
>jQuery其实就是一堆的js函数(js库)，也是普通的js而已，不是全新
的东西，不要畏惧!

**jQuery官方标语**
- write less ， do more

## 为什么要用jquery(非设计思想上的好处)


- jQuery面向用户良好的设计使得在使用过程中彻底解放了你记忆原
生操作DOM的接口

- jQuery中包含多个可重用的函数，用来辅助我们简化javascript开发
- jQuery在半数以上并没有复杂交互的网站中得以大面积使用，因为它们需要的仅仅是一些兼容低级浏览器而又呈现酷炫效果动画的页面。（jQuery出到3，但大公司pc端依然用1.x版本、移动端2.x版本）
- jQuery改变了数百万人编写JavaScript的方式，当然部分人已经觉得时过境迁，组件化，工程化，大行其道，但请不要忘记他的前端开发者的启蒙意义！且很多公司很多项目依然需要他，所以笔面试必会！
## jQuery学习注意点

- jQuery只是辅助工具，不能完全替代js，二者并存当方式出现在项目中
- jQuery很庞杂，先学使用再学思想
- jQuery方法很多，按需学习，把常用的有价值的学会
- jQuery api 可以现查现用

## jQuery的使用-起步

### 起步
~~~
       引入jQuery工具库

		     cdn：http://www.jq22.com/cdn/#a2

		下载地址：http://www.jq22.com/jquery-info122
		
~~~

### 官方

~~~
官方地址（下载 api查询等）:

	中文：
		https://www.jquery123.com/

	英文原版：
		https://jquery.com/
~~~

### 使用起步
~~~
核心全局函数：
	$ (jQuery)
	一顿操作猛如虎，全从$开始撸

撸代码从选择开始:
	选择元素：
		$(); 此函数可以传递多种参数，返回值是对象（jq对象）
		
	参数规则：
		css selector、 jquery unique selector 
		null、undefined、dom
		$(function(){}) $(document).ready() 

		css selector和context

		http://www.w3school.com.cn/jquery/jquery_ref_selectors.asp

~~~


## jQuery使用-精髓


  - 选择元素
  - 循环操作
  - 链式调用


#### jQuery实例方法-DOM操作
##### 进一步选择元素相关方法
~~~
  .get()
	.eq()
	.find()
	.filter()
	.not()
	.is()
	.has()
	
	.add() 集中操作 .end() 回退操作
~~~


##### 取赋值相关方法：

~~~
	.html()、.text()、.val()、.size()

	.addClass 、.removeClass、.hasClass

	.css 

	.attr()、.prop()	

注意：
	1. 尽量避免直接添加行间样式，因为其权重过高 ，这样不利于响应式设计，
破坏了c3+h5优雅的解决方案

	2.attr和prop的区别：
		jQuery认为：attribute的checked、selected、disabled就是表示该属性初始状态的值，
property的checked、selected、disabled才表示该属性实时状态的值(值为true或false)

~~~
##### 取赋值相关方法：
~~~
 .val()
~~~

##### 基于jQuery对象查改删增相关方法：

~~~
  .next()、.prev()、.preAll()、.nextAll()
	.prevUntil() 、.nextUntil()
	.siblings()
	.parent()、.parents()、.offsetParent()、.closest()
	.slice()

	.insertAfter()、.After()
	.insertBefore()、.before()
	.appendTo()、.append()
	.prependTo()、.prepend()

	.remove()、.detach()

	$() 参数：标签字符串 创建jQuery对象


~~~

##### 基于jQuery对象增删改查相关方法：

~~~
.wrap()、 wrapInner()、wrapAll、unWrap
	.clone()
~~~

#### jQuery实例方法-事件

~~~
事件绑定：
	.on()

	.one()

	.off()

	.trigger()

	.click/keydown/mouseenter…

~~~

~~~
兼容的事件对象：
	e.pageX、e.clienX、e.which、e.button

	e.preventDefault()

	e.stopPropagation()

	return false; 


~~~

####  jQuery实例方法-动画

~~~
动画相关方法：
	.hide()、.show()、.toggle()
		参数：null 或 （duration, easing, callblack）

	.fadeIn、.fadeout 、.fadeToggle、.fadeTo()	
		参数：null或 （duration, [opacity], easing, callblack）

	.slideDown()、.slideUp()、.slideToggle()
		参数：null或 （duration, [opacity], easing, callblack）

	.animate()
		参数：(target duration easing callback）

	.stop() .finish()
		参数：true false
	.delay()

	jQuery.fx.off = true 运动的开关
~~~

#### jQuery实例方法-动画插件
~~~
插件名称：
	jQuery Easing Plugin:

目的:
	用于扩展jQuery动画过渡效果
	
链接地址：
	https://cdnjs.cloudflare.com/ajax/libs/jquery-easing/1.4.1/jquery.easing.min.js
~~~

#### jQuery实例方法-位置图形
~~~
位置坐标图形大小相关方法：
	.offset()
	.position()
	.scrollTop() 、.scrollLeft()
	.width()、.height()
	.innerWidth()、.outerWidth()、.innerHeight()、.outerWidth()



~~~
#### jQuery实例方法-遍历索引

~~~
遍历索引相关方法：

	.each()，补充.children()

	.index()

~~~
#### jQuery工具方法


~~~
$.type() 判断数据类型 $.isArray()  $.isFunction()  $.isWindow…

$.trim() 消除空格

$.proxy() 改变this指向

$.noConflict()防止冲突

$.each() 循环 map...

$.parseJSON() 严格json字符串转换成对象 – 原生JSON.parse();

$.makeArray() 类数组转换成数组


~~~

~~~
$.extend() 插件扩展（工具方法）

$.fn.extend() 插件扩展（实例方法）

~~~


#### jQuery工具方法-高级

~~~
$.ajax() - 基本使用

前提：看一下，《你不知道的js》课程中的UI多线程-深入剖析js执行机制

$.Callbacks() 回调

$.Deferred() 异步

$.when()

~~~
