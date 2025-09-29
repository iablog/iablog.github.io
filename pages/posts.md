---
layout: default
title: Posts
permalink: /posts/
---

<div class="posts">
    {% for post in site.posts %}
        <img src="{{ site.baseurl}}/{{ post.image }}">
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        <h3> {{ post.subtitle }} </h3>
        <p> {{post.author}} | {{ post.date | date: "%d %b %Y" }} </p>
    {% endfor %}
</div>