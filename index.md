---
layout: default
title: Home
active_section: home
---
<p class="eyebrow">journal</p>
<h1>{{ site.title }}</h1>
<p class="lead">{{ site.description }}</p>

<div class="meta-block">
  <p><strong>comments:</strong> every post is wired for giscus-backed discussions</p>
  {% if site.posts.first %}
  <p><strong>latest:</strong> <a href="{{ site.github.url | default: site.baseurl | default: '' }}{{ site.posts.first.url }}">{{ site.posts.first.title }}</a></p>
  {% endif %}
</div>

<section class="section-space">
  <h2>the only niche</h2>
  <p>text-first like <code>ephiv.github.io</code></p>
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

<section class="section-space">
  <h2>how to keep it moving</h2>
  <p>Write new posts in <code>_posts/</code> using standard Jekyll filenames, then fill in the giscus IDs in <code>_config.yml</code> once Discussions are enabled on the repository.</p>
</section>
