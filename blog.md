---
layout: default
paginate: true
title: Blog
---

<div class="blog-header">
  <h1>Blog</h1>
  <p>Learnings, insights, and explorations in AI, LLMs, Big Data, and System Design</p>
</div>

<div class="content-wrapper">
  <div>
    <ul class="posts-list">
      {% for post in paginator.posts %}
        <li>
          <a href="{{ post.url | relative_url }}">
            <span class="post-date">{{ post.date | date: "%Y-%m-%d" }}</span>
            <span class="post-title">{{ post.title }}</span>
          </a>
          {% if post.excerpt %}
            <p style="margin: 0.5rem 0 0 0; color: var(--text-light); font-size: 0.95rem;">{{ post.excerpt }}</p>
          {% endif %}
          {% if post.tags %}
            <div class="post-tags" style="margin-top: 0.5rem;">
              {% for tag in post.tags %}
                <a href="{{ '/tags' | relative_url }}#{{ tag | slugify }}" class="post-tag">{{ tag }}</a>
              {% endfor %}
            </div>
          {% endif %}
        </li>
      {% endfor %}
    </ul>

    <!-- Pagination -->
    {% if paginator.total_pages > 1 %}
      <div class="pagination">
        {% if paginator.previous_page %}
          {% if paginator.previous_page == 1 %}
            <a href="{{ '/blog' | relative_url }}">← Previous</a>
          {% else %}
            <a href="{{ '/blog/page/' | relative_url }}{{ paginator.previous_page }}/">← Previous</a>
          {% endif %}
        {% endif %}

        {% for page in (1..paginator.total_pages) %}
          {% if page == paginator.page %}
            <span class="current">{{ page }}</span>
          {% elsif page == 1 %}
            <a href="{{ '/blog' | relative_url }}">{{ page }}</a>
          {% else %}
            <a href="{{ '/blog/page/' | relative_url }}{{ page }}/">{{ page }}</a>
          {% endif %}
        {% endfor %}

        {% if paginator.next_page %}
          <a href="{{ '/blog/page/' | relative_url }}{{ paginator.next_page }}/">Next →</a>
        {% endif %}
      </div>
    {% endif %}
  </div>

  <!-- Sidebar with Tag Cloud -->
  <aside class="sidebar">
    <div class="sidebar-widget">
      <h3>Tags</h3>
      <div class="tag-cloud">
        {% assign tags = site.posts | map: 'tags' | join: ','  | split: ',' | uniq | sort %}
        {% for tag in tags %}
          <a href="{{ '/tags' | relative_url }}#{{ tag | slugify }}" class="tag-link">#{{ tag }}</a>
        {% endfor %}
      </div>
    </div>
    <div class="sidebar-widget">
      <h3>Recent Posts</h3>
      <ul style="list-style: none; padding: 0;">
        {% for post in site.posts limit:5 %}
          <li style="margin-bottom: 0.8rem; padding-bottom: 0.8rem; border-bottom: 1px solid rgba(0,0,0,0.1);">
            <a href="{{ post.url | relative_url }}" style="font-size: 0.9rem;">{{ post.title }}</a>
            <div style="font-size: 0.8rem; color: var(--text-light); margin-top: 0.3rem;">{{ post.date | date: "%b %d, %Y" }}</div>
          </li>
        {% endfor %}
      </ul>
    </div>
  </aside>
</div>
