---
layout: page
title: Projects
permalink: /projects/
description: Research and personal projects.
nav: true
nav_order: 3
display_categories: [current, past]
horizontal: false
---
Below are some of the projects I have worked on or am currently involved with.  
<h6>Kindly email me with:</h6>
<ul>
    <li>Brief CV </li>
    <li>Motivation letter (ranging from 1/2 to 1 page)
        <ol>
            <li>Specify the projects you are interested in or suggest a project within the RL field.</li>
            <li>Mention your intended start date.</li>
            <li>Describe any relevant experiences you might have.</li>
        </ol>
    </li>
</ul>

Please note that prior knowledge in RL is <span style="color: #00ab37;">NOT</span> a prerequisite.

<!-- pages/projects.md -->
<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_projects = site.projects | where: "category", category -%}
  {%- assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
  {% endfor %}

{%- else -%}
<!-- Display projects without categories -->
  {%- assign sorted_projects = site.projects | sort: "importance" -%}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
{%- endif -%}
</div>
