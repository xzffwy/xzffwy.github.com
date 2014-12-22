---
layout: blog
date:  2014/12/15 20:37:51
title: about jekyll
categories: jekyll
tags: jekyll博客中的中文问题
---
# 博客名中文的解决方法
Jekyll中提供的所有连接包括我们要访问的博客页面都是包含博客名字的，博客的名字是由本地的文件名字决定的，而互联网中的url是不能包含中文的，那我们如何解决这个问题呢？
	
研究了一下午，发现也只能取一个英文的名字了，但是我们在网页中怎样显示中文名呢？我提供了一个最笨的方法。

我们可以利用`Front Mart`中的标签，在tags中写入我们需要的中文名字：
{% highlight ruby %}
---
layout: blog
date:  2014/12/15 20:37:51
title: about jekyll
categories: jekyll
tags: jekyll博客中的中文问题
---
{% endhighlight %}
然后再网页中本来用post.title换位post.tags既可以了！

# 博客内容包含中文不能正确显示(invalid byte sequence in UTF-8)
网上也说了很多的关于这个问题的解决方法，但是我发现针对我的都没有什么用，后来我将所有的文件编码格式变为utf-8，问题迎刃而解了。

