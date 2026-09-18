---
layout: page
permalink: /publications/
title: Publications
nav: true
nav_order: 3
---

{% include_relative shared_style.html %}

<style>
  /* Section heading between the Georgia Tech and earlier work; matches the bold headings on the People page */
  .publications h2.category { font-weight: 700; font-size: 2.25rem; color: var(--global-text-color); margin-top: 3.5rem; margin-bottom: 0.5rem; }
</style>

<!-- _pages/publications.md -->

<!-- Bibsearch Feature -->

{% include bib_search.liquid %}

<div class="publications">

{% bibliography --query @*[category=gatech] %}

<h2 class="category">Work prior to GA Tech:</h2>

{% bibliography --query @*[category=prior] %}

</div>
