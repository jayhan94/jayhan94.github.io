---
title: 编程西行记
description: 编程相关的技术博客
---

# 欢迎来到编程西行记
分享是最好的学习方法.
这里会不定期发布编程相关的技术博客，聚焦在:
- 计算机基础
- 编程语言基础
- 大数据处理和分析

欢迎阅读.

## 文章分类

{% assign categories = site.posts | group_by: "category" %}
{% for category in categories %}
  <div class="category-section">
    <h2 class="category-title">{{ category.name }}</h2>
    <div class="post-list">
      {% for post in category.items %}
        <article class="post-item">
          <h3 class="post-title">
            <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
          </h3>
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
  </div>
{% endfor %} 
