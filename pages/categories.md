---
layout: default
title: Categorias
permalink: /categories/
---

<div class="post-list">
  
  {% for category in site.categories %}
    {% assign category_name = category | first %}
    {% assign category_slug = category_name | slugify %}
    
    <h2 style="color: #0a0a0aff; margin-top: 50px; margin-bottom: 30px; font-size: 2.5em;">
      {{ category_name }}
    </h2>
    
    {% for post in category.last %}
      <div style="margin-bottom: 40px; padding-left: 0;">
        
        <h3 style="margin-bottom: 10px;">
          <a href="{{ site.baseurl }}{{ post.url }}" style="color: #6a6c6eff; text-decoration: none;">
            {{ post.title }}
          </a>
        </h3>
        
        <p style="font-size: 0.95em; color: #999; margin: 8px 0;">
          {{ post.date | date: "%d %b %Y" }}
        </p>
        
        <p style="color: #131212ff; line-height: 1.6; margin: 15px 0;">
          {{ post.excerpt | strip_html | truncatewords: 40 }}
        </p>
        
      </div>
    {% endfor %}
    
  {% endfor %}
</div>