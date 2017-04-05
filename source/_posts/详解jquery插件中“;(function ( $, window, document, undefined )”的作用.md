layout: active
title: 详解jquery插件中“;(function ( $, window, document, undefined )”的作用
date: 2016-11-05 18:18:37
tags: ;(function ( $, window, document, undefined )
---

在写jQuery插件的时候我们经常这样写
<pre><code>;(function($, window, document, undefined){
	//插件详细代码
})(jQuery, window, document);
</code></pre>

1. 代码最前边的分号（;）, 为了防止在多文件压缩的时候，其它文件最后一行没有写分号引起错误。
2. (function(){})() 为自执行匿名函数， 它的好处就是可以避免内部变量和外部变量引起冲突。
3. window, document对象都是全局环境下的， 在函数中window, document则是局部变量，不是全局的window, document对象。这样的好处就是可以提交性能， 减少作用域链的查询时间， 如果函数体内多次调用window和document对象，那么这样做非常有必要。
4. undefined是低版本浏览器可以修改的问题。
