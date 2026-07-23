---
layout: page
title: Research
permalink: /research/
description: Our group develops and applies theoretical and computational methods to understand chemical structure, dynamics, and mechanism. Below is an overview of our current research directions.
nav: true
nav_order: 2
---

<!-- pages/projects.md -->
<style>
  .projects .card {
    box-shadow: none !important;
    border: none !important;
    background: transparent;
  }
  .projects .card:hover {
    box-shadow: none !important;
  }
  .projects .card-img-top {
    height: 220px;
    object-fit: cover;
    width: 100%;
  }
  .projects .card-title {
    font-size: 1.15rem;
    text-align: center;
    padding-bottom: 0.6rem;
    margin-bottom: 0.8rem;
    border-bottom: 1px solid rgba(128, 128, 128, 0.35);
  }
  .projects .card-text {
    text-align: justify;
  }
</style>
<div class="projects">
  {% assign sorted_projects = site.projects | sort: "importance" %}
  <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      <div class="col mb-4">
	<div class="card h-100 border-0">	
          {% if project.img %}
            {% assign ext = project.img | split: "." | last | downcase %}
            {% if ext == "mp4" or ext == "webm" %}
              <video class="card-img-top" autoplay loop muted playsinline>
                <source src="{{ project.img | relative_url }}" type="video/{{ ext }}" />
              </video>
            {% else %}
              <img src="{{ project.img | relative_url }}" alt="{{ project.title }}" class="card-img-top" loading="lazy" />
            {% endif %}
          {% endif %}
      <div class="card-body">
            <h3 class="card-title">{{ project.title }}</h3>
	    <div class="card-text">{{ project.description | markdownify }}</div>       
          </div>
        </div>
      </div>
    {% endfor %}
  </div>
</div>
