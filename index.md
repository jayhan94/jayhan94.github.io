---
title: 飞飞鸟
description: 计算机/产品相关内容输出
---

# 欢迎来到飞飞鸟
分享是最好的学习方法.
这里会不定期发布编程相关的技术/产品内容

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
