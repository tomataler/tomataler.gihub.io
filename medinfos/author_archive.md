---
layout: default
current: author_archive
title: "Author Archive"
permalink: /medinfos/author-archive/
navigation: true
logo: 
class: page-template
subclass: 'post page'
---
<h1>{{ page.title }}</h1>

{% for author in site.authors %}
  <h2>{{ author[0] }}</h2>
  <ul>
    {% for post in site.posts %}
      {% if post.author == author[0] %}
        <li>
          <!-- <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a> -->
          <a href="{{ post.url | prepend: root_url }}">{{ post.title }}</a>
          <span>- {{ post.date | date: "%b %d, %Y" }}</span>
        </li>
      {% endif %}
    {% endfor %}
  </ul>
{% endfor %}