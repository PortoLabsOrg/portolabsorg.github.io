---
layout: page
permalink: /blog/
---

<section class="blog-page">
  <div class="container">
    <h1>Latest Articles</h1>
    <p>Research updates, project news, and notes from the PortoLabs team.</p>

    <div class="posts-list">
      {% for post in site.posts %}
        <article class="post-preview">
          <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
          <p class="meta">{{ post.date | date: "%B %d, %Y" }}</p>
          {% if post.excerpt %}
            <p>{{ post.excerpt | strip_html | truncate: 180 }}</p>
          {% endif %}
          <a href="{{ post.url | relative_url }}" class="btn-sm">Read more</a>
        </article>
      {% endfor %}
    </div>
  </div>
</section>
