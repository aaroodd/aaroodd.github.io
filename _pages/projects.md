---
layout: page
title: projects
permalink: /projects/
description: A mix of research and technical work.
nav: true
nav_order: 3
display_categories: [research, technical]
horizontal: false
---

<!-- pages/projects.md -->
<div class="projects">
  {% if site.enable_project_categories and page.display_categories %}
    {% for category in page.display_categories %}
      <a id="{{ category }}" href=".#{{ category }}">
        <h2 class="category">{{ category }}</h2>
      </a>
      {% assign categorized_projects = site.projects | where: "category", category %}
      {% assign sorted_projects = categorized_projects | sort: "importance" %}
      <div class="row row-cols-1 row-cols-md-3 g-4">
        {% for project in sorted_projects %}
          {% include projects.liquid %}
        {% endfor %}
      </div>
    {% endfor %}
  {% else %}
    {% assign sorted_projects = site.projects | sort: "importance" %}
    <div class="row row-cols-1 row-cols-md-3 g-4">
      {% for project in sorted_projects %}
        {% include projects.liquid %}
      {% endfor %}
    </div>
  {% endif %}
</div>
