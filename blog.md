---
title: blog
permalink: /posts/
active_section: blog
lead: everything
---
<div class="post-list">
  {% if site.posts.size > 0 %}
    {% for post in site.posts %}
    <article class="post-card">
      <p class="post-meta">{{ post.date | date: "%B %-d, %Y" }}</p>
      <h2><a href="{{ site.github.url | default: site.baseurl | default: '' }}{{ post.url }}">{{ post.title }}</a></h2>
      <p>{{ post.description | default: post.excerpt | strip_html | truncate: 180 }}</p>
    </article>
    {% endfor %}
  {% else %}
  <p class="empty-state">No posts yet.</p>
  {% endif %}
</div>
