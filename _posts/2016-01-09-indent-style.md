---
title: Girintileme Stilleri(Indent Styles)
categories:
  - coding-standarts
tags:
  - indent
  - styles
  - programming
  - coding
  - standarts
---

Girintileme yapma kodumuzun okunurluğunu ve kalitesini arttırır. Koddaki hataların daha kolay görülmesini sağlar. Girintileme için çeşitli standartlar belirlenmiştir ve bu standartlardan birini seçip kullanmak hem bireysel hem de ekip ile yapılan geliştirmeler için önemli bir konudur.

## K&R(Kernighan&Ritchie) Style

{% highlight c startinline=true %}
    if (index > 0) {
        index--;
	return("foo");
    } else {
        index++;
	return("bar");
}
{% endhighlight %}

## K&R Style(Stroustrup)

{% highlight c startinline=true %}
    if (index > 0) {
        index--;
	return("foo");
    } 
    else {
        index++;
	return("bar");
    }
{% endhighlight %}

## K&R Style(Linux Kernel)

{% highlight c startinline=true %}
    if (index > 0) {
            index--;
	    return("foo");
    } else {
            index++;
	    return("bar");
    }
{% endhighlight %}

## K&R Style(BSD KNF)

{% highlight c startinline=true %}
    if (index > 0) {
            index--;
	    return("foo");
    } else {
            index++;
	    return("bar");
    }
{% endhighlight %}

## Allman Style

{% highlight c startinline=true %}
    if (index > 0) 
    {
        index--;
	return("foo");
    } 
    else 
    {
        index++;
	return("foo");
    }
{% endhighlight %}

## GNU Style

{% highlight c startinline=true %}
    if (index > 0) 
      {
        index--;
	return("foo");
      } 
    else 
      {
        index++;
	return("foo");
      }
{% endhighlight %}

## Whitesmiths Style

{% highlight c startinline=true %}
    if (index > 0) 
        {
        index--;
	return("foo");
        } 
    else 
        {
        index++;
	return("foo");
        }
{% endhighlight %}

## Hortsmann Style

{% highlight c startinline=true %}
    if (index > 0) 
    {   index--;
	return("foo");
    } 
    else 
    {   index++;
	return("foo");
    }
{% endhighlight %}

## Pico Style

{% highlight c startinline=true %}
    if (index > 0) 
    {  index--;
       return("foo"); } 
    else 
    {  index++;
       return("foo"); }
{% endhighlight %}

## Ratliff Style

{% highlight c startinline=true %}
    if (index > 0) {
        index--;
	return("foo");
    } else {
        index++;
	return("foo");
    }
{% endhighlight %}

## Lisp Style

{% highlight c startinline=true %}
    if (index > 0) {
        index--;
	return("foo"); } 
    else {
        index++;
	return("foo"); }
{% endhighlight %}
