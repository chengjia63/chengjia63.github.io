---
layout: default
title: Reviews
exclude: true
---
# Reviews

<ul>
{% for post in site.reviews %}
    <li>
    <a href="{{ post.url }}">
        [{{ post.author }} {{ post.year }}]<br>{{ post.title }}</a>
    </li>
{% endfor %}
</ul>

### [Review template](https://gist.github.com/kasikci/49e7107dfdee281d6f6450b132555550) credit: Prof. Kasikci
