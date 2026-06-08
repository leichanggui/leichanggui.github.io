---
layout: default
title: Notes
permalink: /en/notes/
eyebrow: Technical Notes
lead: Method notes, literature reading, and project reflections.
lang: en
cn_url: /notes/
en_url: /en/notes/
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
  <p class="note-box">No notes yet. Markdown posts can be added under the <code>_posts</code> directory.</p>
{% endif %}
