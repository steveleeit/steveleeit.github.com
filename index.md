---
layout: page
title: Steve Lee 
tagline: Simple Life
---
{% include JB/setup %}
是Steve的博客，欢迎您。
#文章列表:
<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
