---
layout: default
title: Home
active_section: home
---
<p class="eyebrow">journal</p>
<h1>{{ site.title }}</h1>
<p class="lead">{{ site.description }}</p>

<section class="section-space">
  <h2>niche</h2>
  <p>text-first like <code>ephiv.github.io</code>, markdown shell stuff, found out it's great for reading and to write a blog in</p>
</section>

<section class="section-space">
  <h2>recent posts</h2>
  <div class="post-list">
    {% for post in site.posts limit: 3 %}
    <article class="post-card">
      <p class="post-meta">{{ post.date | date: "%B %-d, %Y" }}</p>
      <h3><a href="{{ site.github.url | default: site.baseurl | default: '' }}{{ post.url }}">{{ post.title }}</a></h3>
      <p>{{ post.description | default: post.excerpt | strip_html | truncate: 160 }}</p>
    </article>
    {% endfor %}
  </div>
</section>
