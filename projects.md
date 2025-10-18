---
layout: page 
permalink: /projects/
---

<section class="projects-page">
  <div class="container">
    <h1>Our Projects</h1>
    <p>Each of our research and development projects reflects our focus on practical, responsible, and local-first AI systems.</p>
    <p>Below are a few of our key initiatives.</p>

    <div class="grid">
      {% for project in site.projects %}
        <div class="card project">
          {% if project.image %}
            <img src="{{ project.image | relative_url }}" alt="{{ project.title }}">
          {% endif %}
          <h3><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h3>
          <p>{{ project.summary }}</p>
        </div>
      {% endfor %}
    </div>
  </div>
</section>
