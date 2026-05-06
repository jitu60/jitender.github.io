---
layout: default
title: Tags
---

<h1>Browse by Tags</h1>

{% assign tags = site.posts | map: 'tags' | join: ',' | split: ',' | uniq | sort %}

{% for tag in tags %}
  <section id="{{ tag | slugify }}" style="margin: 3rem 0;">
    <h2 style="border-bottom: 3px solid var(--accent-color); padding-bottom: 0.5rem; display: inline-block;">#{{ tag }}</h2>
    <div class="posts-list" style="margin-top: 1.5rem;">
      {% for post in site.posts %}
        {% if post.tags contains tag %}
          <div style="padding: 1rem 0; border-bottom: 1px solid var(--border-color);">
            <div style="display: flex; justify-content: space-between; align-items: flex-start;">
              <div style="flex: 1;">
                <a href="{{ post.url | relative_url }}" style="text-decoration: none;">
                  <h3 style="margin: 0; color: var(--secondary-color);">{{ post.title }}</h3>
                </a>
                {% if post.excerpt %}
                  <p style="margin: 0.5rem 0 0 0; color: var(--text-light); font-size: 0.95rem;">{{ post.excerpt }}</p>
                {% endif %}
              </div>
              <span style="color: var(--text-light); white-space: nowrap; margin-left: 1rem;">{{ post.date | date: "%b %d, %Y" }}</span>
            </div>
          </div>
        {% endif %}
      {% endfor %}
    </div>
  </section>
{% endfor %}
