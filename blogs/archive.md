---
layout: default
current: archive
title: "Archive"
permalink: /blogs/archive/
navigation: true
logo: 
class: page-template
subclass: 'post page'
---

<h1>{{ page.title }}</h1>

<ul>
{% for post in site.posts %}
  <li>
    <!-- <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a> -->
    <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
    <span>- {{ post.date | date: "%b %d, %Y" }}</span>
  </li>
{% endfor %}
</ul>