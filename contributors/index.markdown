---
layout: page
title: "contributors"
date: 2014-05-10 -0800
comments: false
categories: [personal blog]
sharing: false
---

You should develop my blog site, contribute by solving the problems you see. If you have such a request, just send me a "pull request"!


Every post in my blog has an edit link that lets you edit the blog post directly in the browser and automatically sends me a pull request.

Or [visit my repository]({{site.github_repo_url}}) and send me a pull request the old fashioned way.

<ul>
{% for contributor in site.github.contributors %}
  <li>
    <img src="{{ contributor.avatar_url }}" width="32" height="32" /> <a href="{{ contributor.html_url }}">{{ contributor.login }}</a>
  </li>
{% endfor %}
</ul>
