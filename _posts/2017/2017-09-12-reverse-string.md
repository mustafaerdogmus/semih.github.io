---
layout: post
title: "Reverse String"
date: 2017-09-12 18:31ly
author: semihkirdinli
comments: true
categories: [Algorithm, C#]
tags: [c#, algorithm]
---
There are 2 methods for reversing the string input. *ReverseStringDirect(s)* method completely reverses the string and   *ReverseStringOnlyOrder(s)* method reverses only collating sequence of the words, their writing are the same in themselves.
{% highlight c# %}
using System;

public class Program
{
    public static void Main()
    {
	string s = "Hello world!";
	Console.WriteLine("ReverseStringDirect: " + ReverseStringDirect(s));
	Console.WriteLine("ReverseStringOnlyOrder: " + ReverseStringOnlyOrder(s));
    }
    
    public static string ReverseStringDirect(string s)
    {
        char[] array = new char[s.Length];
        int forward = 0;
        for (int i = s.Length - 1; i >= 0; i--)
        {
            array[forward++] = s[i];
        }
        return new string(array);
    }
	
    public static string ReverseStringOnlyOrder(string s)
    {
        int wordsLength = 0;
        string result = "";
        
        for (int i=0; i<s.Length; i++)
        {
            if(s[i] == ' ')
            {
                result = " " + result;
                wordsLength = 0;
            } else
            {
                result = result.Insert(wordsLength, s[i].ToString());
                wordsLength++;
            }
        }
        return result;
    }
}
{% endhighlight %}

Output:
{% highlight c# %}
ReverseStringDirect: !dlrow olleH
ReverseStringOnlyOrder: world! Hello
{% endhighlight %}
