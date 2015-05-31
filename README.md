# js-selector
基于原生js封装的一些简单选择器

----------
####大致可以分下面几种情况讨论
	- 简单的id/class/tagName选择器，并且参数中不含特殊字符(" ",">")，
	  就是平常的document.getElement....
	- 匿名方法function(){},就丢给window.onload = function(){}处理
	- 含有" "的，就是下代选择器，先把当前元素取出来，再取出它的子集元素
	- 含有">"的，就是亲子代选择器，同样先把当前元素取出来，再取出它的子
	  集元素，同时要保证它的子集元素的父节点就是当前节点才能通过


----------
####API
	我们可以使用下面几种选择器
	$s("#test-id")
	$s(".test-class")
	$s("p")
	$s(".test-children #children2 .children2-1")
	$s(".test-children #children2 p")
	$s(".test-first-child>.first-child2")
	$s(".test-first-child>div p")	

会返回一个对象,取出具体元素集合需用$("p").elements来取。