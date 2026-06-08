---
layout: default
title: Notes
permalink: /notes/
eyebrow: Technical Notes
lead: 方法笔记、读文献记录和项目复盘。
---

{% if site.posts.size > 0 %}
  <div class="post-list">
    {% for post in site.posts %}
      <article>
        <p class="post-meta">{{ post.date | date: "%Y-%m-%d" }}</p>
        <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
        {{ post.excerpt }}
      </article>
    {% endfor %}
  </div>
{% else %}
  <p class="note-box">还没有笔记。后续可以在 <code>_posts</code> 目录中添加 Markdown 文件。</p>
{% endif %}
