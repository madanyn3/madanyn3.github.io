---
layout: page
title: Blogs
permalink: /blogs/
---

#### Welcome to My Blog

This is where I share my thoughts, ideas, and updates on the mini-projects I work on from time to time. Since my thoughts are shaped by my experiences, they're naturally influenced by my perspective. I'd love to hear your views and have a conversation about them!

---

## 📝 Quick Reads

{% comment %}
Group Quick Reads by series
{% endcomment %}
{% assign quick_reads = site.blogs | where: "category", "quick-read" | sort: "date" %}
{% assign series_posts = quick_reads | where_exp: "post", "post.series != nil" | group_by: "series" %}
{% assign standalone_posts = quick_reads | where_exp: "post", "post.series == nil" %}

{% comment %}
Display series subsections
{% endcomment %}
{% for series_group in series_posts %}
  <h3>{{ series_group.name | replace: "-", " " | capitalize }}</h3>
  <ul>
    {% for post in series_group.items %}
      <li>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a> 
        <small>({{ post.date | date: "%Y-%m-%d" }})</small>
      </li>
    {% endfor %}
  </ul>
{% endfor %}

{% comment %}
Display standalone quick reads
{% endcomment %}
{% if standalone_posts.size > 0 %}
  <h3>Other Thoughts</h3>
  <ul>
    {% for post in standalone_posts %}
      <li>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a> 
        <small>({{ post.date | date: "%Y-%m-%d" }})</small>
      </li>
    {% endfor %}

  </ul>
{% endif %}

---

## 📚 Deep Dives

Longer, detailed explorations and analyses.

<ul>
  <li>
    <a href="https://medium.com/@myn.create/why-apple-silicon-is-better-7d6628aa0c3e" target="_blank" rel="noopener noreferrer">
      Why Apple Silicon is Better
    </a> 
    <small>(2025-01-26)</small>
  </li>
  <li>
    <a href="https://medium.com/@myn.create/life-in-disequilibrium-a9524f2e7fee" target="_blank" rel="noopener noreferrer">
      Life in Disequilibrium
    </a> 
    <small>(2025-11-10)</small>
  </li>
</ul>
