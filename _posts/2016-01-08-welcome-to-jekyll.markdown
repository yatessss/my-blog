---
layout: post
title:  "markdown语法简介"
date:   2016-01-08 20:46:12
categories: jekyll update
---

在我看来markdown语法就是可以不需要了解html,来编写博客网页.
总结这个也是为了将来自己有不会的地方可以很快的查看一下.

###1. 标题标签<h1>写法

* ***markdown中的写法:***
{% highlight shell-session %}
一级标题
=======

二级标题
-----------

### 其他级别标题
{% endhighlight %}

* ***对应的html结构:***
{% highlight html %}
<h1>一级标题</h1>

<h2>二级标题</h2>

<h3>其他级别标题</h3>
{% endhighlight %}

* ***在页面中显示的效果:***

一级标题
=======

二级标题
-----------

### 其他级别标题

---

###2. 段落标签<p>写法

* ***markdown中的写法:***
{% highlight shell-session %}
这是一个段落,段落分隔用一个空白行
{% endhighlight %}

* ***对应的html结构:***
{% highlight html %}
<p>这是一个段落,段落分隔用一个空白行</p>
{% endhighlight %}

* ***在页面中显示的效果:***

这是一个段落,段落分隔用一个空白行

---

###3. 强调< em >,粗体< strong >,代码< code >,删除< s >写法
* ***markdown中的写法:***
{% highlight shell-session %}
各类标签:*强调标签em*,**加粗标签strong**,`代码标签code`
{% endhighlight %}

* ***对应的html结构:***
{% highlight html %}
<p>Text attributes <em>italic</em>, <strong>bold</strong>,<code>monospace</code></p>
{% endhighlight %}

* ***在页面中显示的效果:***

各类标签:
*强调标签em*,
**加粗标签strong**,
`代码标签code`

---

###4. 有序列表<ol>和无序列表<ul>写法
* ***markdown中的写法:***
{% highlight shell-session %}
有序列表:

1. 列表1
2. 列表2
3. 列表3
{% endhighlight %}
{% highlight shell-session %}
无序列表:

* 列表1
* 列表2
* 列表3
{% endhighlight %}

* ***对应的html结构:***
{% highlight html %}
<p>有序列表:</p>

<ol>
<li>列表1</li>
<li>列表2</li>
<li>列表3</li>
</ol>
{% endhighlight %}
{% highlight html %}
<p>无序列表:</p>

<ul>
<li>列表1</li>
<li>列表2</li>
<li>列表3</li>
</ul>
{% endhighlight %}

* ***在页面中显示的效果:***

有序列表:

1. 列表1
2. 列表2
3. 列表3

无序列表:

* 列表1
* 列表2
* 列表3

---

###5. 链接的写法
* ***markdown中的写法:***

行内式写法:
{% highlight shell-session %}
这是行内式写法的[例子](http://example.com/ "Title")

这是行内式写法没有title属性的[例子](http://example.net/)
{% endhighlight %}
参考式写法1:
{% highlight shell-session %}
这是参考式写法1的[例子][id]
[id]: http://example.com/  "Optional Title Here"
{% endhighlight %}
参考式写法2:
{% highlight shell-session %}
这是参考式写法2的[例子][]
[例子]: http://example.com/  "Optional Title Here"
{% endhighlight %}

* ***对应的html结构:***

行内式:
{% highlight html %}
<p>这是行内式写法的<a href="http://example.com/" title="Title">例子</a></p>

<p>这是行内式写法没有title属性的<a href="http://example.net/">例子</a></p>
{% endhighlight %}
参考式1:
{% highlight html %}
<p>这是参考式写法1的<a href="http://example.com/" title="Optional Title Here">例子</a></p>
{% endhighlight %}
参考式2:
{% highlight html %}
<p>这是参考式写法2的<a href="http://example.com/" title="Optional Title Here">例子</a></p>
{% endhighlight %}
* ***在页面中显示的效果:***

这是行内式写法的[例子](http://example.com/ "Title")

这是行内式写法没有title属性的[例子](http://example.net/)

这是参考式写法1的[例子] [id]

[id]: http://example.com/  "Optional Title Here"

这是参考式写法2的[例子][]

[例子]: http://example.com/  "Optional Title Here"

---

###6. 反斜杠转译

Markdown 支持以下这些符号前面加上反斜杠来帮助插入普通的符号：

{% highlight shell-session %}
\   反斜线
`   反引号
*   星号
_   底线
{}  花括号
[]  方括号
()  括弧
#   井字号
+   加号
-   减号
.   英文句点
!   惊叹号
{% endhighlight %}

以上,其实还有图片的插入,不过和添加链接类似,在此不再赘述了.
