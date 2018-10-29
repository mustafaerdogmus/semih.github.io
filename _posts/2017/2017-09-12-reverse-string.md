---
layout: post
title: "Reverse String"
date: 2017-09-12 18:31ly
author: semih
comments: true
categories: [Algorithm, Java]
tags: [java, algorithm]
---
In the following example, reversal string operation is shown in Java language. *ReverseString(s)* method completely reverses the string.
{% highlight java %}
public class ReverseString {

	public static void main(String[] args) {
		String s = "Hello world!";
		System.out.println("Reverse: " + Reverse(s));
	}

	public static String Reverse(String s) {
		
		char[] array = new char[s.length()];
		int forward = 0;
		for (int i = s.length() - 1; i >= 0; i--) {
			array[forward++] = s.charAt(i);
		}
		return new String(array);
	}
	
}
{% endhighlight %}

Output:
{% highlight java %}
ReverseString: !dlrow olleH
{% endhighlight %}
