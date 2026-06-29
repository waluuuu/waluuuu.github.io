---
title: Home
---

<section class="intro">
  <p class="eyebrow">WalUU</p>
  <h1>写一点正在想的东西。</h1>
  <p class="lede">这里会放新的文章、笔记和一些不必太正式的记录。旧内容已经清空，从这里重新开始。</p>
</section>

<section class="post-list" aria-labelledby="posts-title">
  <h2 id="posts-title">文章</h2>
  {% if site.posts.size > 0 %}
    <div class="entries">
      {% for post in site.posts %}
        <article class="entry">
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
          <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%Y-%m-%d" }}</time>
          {% if post.excerpt %}
            <p>{{ post.excerpt | strip_html | truncate: 96 }}</p>
          {% endif %}
        </article>
      {% endfor %}
    </div>
  {% else %}
    <p class="empty">还没有文章。</p>
  {% endif %}
</section>
