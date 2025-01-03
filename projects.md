---
layout: page
title: Projects
subtitle:
    - Ocean Modeling 
    - Computational Fluid Dynamics 
    - Numerical Linear Algebra
    - Stochastic Modeling
    - Machine Learning
---

<div class="projects-list">
{% assign projCategory = site.projects | group_by_exp:"project", "project.categories"  %}

{% for category in projCategory %}
{% if category.name %}
  <h2><a>{{ category.name }}</a></h2>
{% else %}
  <p>{{ Print }}</p>
{% endif %}

{% for project in category.items %}
    <div class="project-entry">
      <h2>
        <strong>{{ project.title }}</strong>
      </h2>
      <p>{{ project.content }}</p>
    </div>
{% endfor %}
<br>
{% endfor %}
</div>
