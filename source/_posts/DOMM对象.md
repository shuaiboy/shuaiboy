---
title: DOMM对象
date: 2016-11-29 22:20:56
tags: DOM对象
---

## 获取DOM对象的方法 ##
	# getElementById()
	# getElementsByName()
	# getElementsByTagName()

## 节点属性 ##
	在文档对象模型(DOM)中，每个节点都是一个对象，DOM节点有三个重要的属性。
	1.nodeName: 节点名称
	2.nodeType: 节点类型
	3.nodeValue: 节点的值
### nodeName 属性：节点的名称，是只读的。###
	1.元素节点nodeName与标签名相同
	2.属性节点nodeName是属性的名称
	3.文本节点nodeName永远是#text
	4.文档节点的NodeName永远是#document
### nodeValue属性：节点的值 ###
	1.元素节点nodeValue永远是undefined或null
	2.文本节点的nodeValue永远是文本自身
	3.属性节点的nodeValue是属性的值
### nodeType属性： 节点的类型，是只读的，以下常用的几种节点类型 ###
元素类型  节点类型
 元素		1
 属性		2
 文本		3
 注释		8
 文档		9
 

## 对元素属性进行操作 ##
	# getAttribute(key)
	# setAttribute(key, value)
## 为了兼容，建议： ##
	1.常规属性使用node.xxx 例如： node.title
	2.自定义属性建议使用node.getAttribute("xxx")
	3.当获取的目标是js的关键字时建议使用node.getAttribute('xxx')  例如： label中的for
	4.当获取的目标是保留字， 例如： class 使用className 代替

## 对节点的访问 ##
	# childNodes 返回一个数组， 执行元素的子元素
	# firstChild 返回子节点的字一个节点元素
	# lastChild  返回子节点的最后一个元素
	# nextSibling 下一个节点
	# previousSibling 上一个节点
	# parentNode 父节点

## 对节点的操作 ##
	# createElement()
	# createTextNode()
	# appendChild()
	# insertBefore()
	# removeChild()
	# replaceChild()