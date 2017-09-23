---
layout: post
title: "Same Characters in String"
date: 2017-09-14 01:15ly
author: semih
comments: true
categories: [Algorithm, C#]
tags: [c#, algorithm]
---
As you seen the following code example, the algorithm helps to find the same characters in a string. This is my way.
{% highlight c# %}
using System;
using System.Linq;

public class Program
{
    public static void Main(string[] args)
    {
        Console.WriteLine(GetSameCharacters("blabla"));
    }

    public static string GetSameCharacters(string s)
    {
        string sameCharacters = "";

        int stringLength = s.Length;
        char[] array = new char[stringLength];

        for(int i=0;i<stringLength;i++)
        {
            for(int j=i+1;j<stringLength;j++)
            {
                if(s[i] == s[j] && !sameCharacters.Contains(s[i]))
                {
                    sameCharacters += s[i];
                }
            }
        } 

        return sameCharacters;
    }
}
{% endhighlight %}

Output:
{% highlight c# %}
bla
{% endhighlight %}
