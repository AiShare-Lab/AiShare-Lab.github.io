---
layout: page
title: Team
permalink: /team/
nav: true
display_categories: [Professor, Lecturer, Doctoral student, Graduate student, Undergraduate]
importance: 3
---
<div>
This page lists our team members
</div>


<div class="projects">
    {% for category in page.display_categories %}
      <h2 class="category">{{category}}</h2>
      <p> </p>
      {% assign members = site.team | where: "category", category %}
      <!-- Generate cards for each project -->
        <div class="container">
          <div class="row row-cols-2">
          {% for member in members %}
            {% include member.html %}
          {% endfor %}
          </div>
        </div>
    {% endfor %}

</div>