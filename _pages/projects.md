---
layout: page
title: Research
permalink: /research/
nav: true
nav_order: 2
---

{% include_relative shared_style.html %}

<!-- pages/projects.md -->
<style>
  .projects .project-entry {
    margin-bottom: 2rem;
  }
  .projects .project-entry:not(:last-child) {
    padding-bottom: 2rem;
    border-bottom: 1px solid rgba(128, 128, 128, 0.35);
  }
  .projects .profile {
    width: 100%;
    margin-bottom: 1rem;
  }
  .projects .profile img,
  .projects .profile video {
    width: 100%;
    display: block;
  }
  .projects .project-title {
    margin-top: 0;
    margin-bottom: 0.8rem;
  }
  .projects .project-description {
    text-align: justify;
  }
  .projects .project-description p:last-child {
    margin-bottom: 0;
  }
  @media (min-width: 576px) {
    .projects .profile {
      width: 32%;
    }
    .projects .profile.float-right {
      float: right;
      margin-left: 1.5rem;
    }
    .projects .profile.float-left {
      float: left;
      margin-right: 1.5rem;
    }
  }
</style>

<div class="projects">
  {% assign sorted_projects = site.projects | sort: "importance" %}
  {% for project in sorted_projects %}
    {% assign remainder = forloop.index | modulo: 2 %}
    {% if remainder == 1 %}
      {% assign align = "right" %}
    {% else %}
      {% assign align = "left" %}
    {% endif %}
    <div class="project-entry clearfix">
      {% if project.img %}
        <div class="profile float-{{ align }}">
          {% assign ext = project.img | split: "." | last | downcase %}
          {% if ext == "mp4" or ext == "webm" %}
            <video class="img-fluid z-depth-1 rounded" autoplay loop muted playsinline>
              <source src="{{ project.img | relative_url }}" type="video/{{ ext }}" />
            </video>
          {% else %}
            <img
              src="{{ project.img | relative_url }}"
              alt="{{ project.title }}"
              class="img-fluid z-depth-1 rounded"
              loading="lazy"
            />
          {% endif %}
        </div>
      {% endif %}
      <h3 class="project-title">{{ project.title }}</h3>
      <div class="project-description">{{ project.description | markdownify }}</div>
    </div>
  {% endfor %}
</div>
