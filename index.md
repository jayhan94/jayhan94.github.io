---
title: 编程西行记
description: 编程相关的技术博客
---

# 欢迎来到编程西行记

分享是最好的学习方法.
这里会不定期发布编程相关的技术博客，重点关注基础芝士，以及数据领域相关技术, 欢迎阅读.

## 最新文章

<div class="post-list">
{% for post in site.posts %}
  <article class="post-item">
    <h2 class="post-title">
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </h2>
    <div class="post-meta">
      <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%Y年%m月%d日" }}</time>
    </div>
    <div class="post-excerpt">
      {{ post.excerpt | strip_html | truncatewords: 50 }}
    </div>
    <a href="{{ post.url | relative_url }}" class="read-more">阅读更多 →</a>
  </article>
{% endfor %}
</div> 
