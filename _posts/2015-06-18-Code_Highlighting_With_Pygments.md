---
title: "Code Highlighting With Pygments"
tags: [pygments,jekyll]
---

Just an example of how to highlight code with Pygments in Jekyll. More info can be found at the below link. <br/>
[http://josephmansfield.uk/articles/custom-syntax-highlighting-jekyll-pygments.html](http://josephmansfield.uk/articles/custom-syntax-highlighting-jekyll-pygments.html)



<u><b>C# Example</b></u>

{{ "{% highlight csharp " }}%} <br/>
public ExampleMethod(int x) <br/>
{ <br/>
&nbsp;&nbsp;&nbsp;&nbsp;	string y = "demo"; <br/>
&nbsp;&nbsp;&nbsp;&nbsp;	string z = x + y; <br/>
} <br/>
{{ "{% endhighlight csharp " }}%} <br/>

{% highlight csharp %} 
public ExampleMethod(int x)
{
	string y = "demo";
	string z = x + y;
}
{% endhighlight %}

<br/>
<u><b>Python Example</b></u>

{{ "{% highlight python " }}%} <br/>
def test_function():  <br/>
&nbsp;&nbsp;&nbsp;&nbsp;    print("Test")  <br/>
{{ "{% endhighlight " }}%}


{% highlight python %} 
def test_function():
    print("Test")
{% endhighlight %}




