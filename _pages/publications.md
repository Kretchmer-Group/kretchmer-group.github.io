---
layout: page
permalink: /publications/
title: Publications
nav: true
nav_order: 3
---

{% include_relative shared_style.html %}

<style>
  /* Section headings separating archive, Georgia Tech and earlier work; matches the bold headings on the People page */
  .publications h2.category { font-weight: 700; font-size: 2.25rem; color: var(--global-text-color); margin-top: 3.5rem; margin-bottom: 0.5rem; }
  /* Year headings: bold and in the normal text color (theme default is a faint gray) */
  .publications h2.bibliography { font-weight: 700; font-size: 1.75rem; color: var(--global-text-color); }
  /* The undated preprints get an empty year heading; hide it so screen readers don't announce a blank heading */
  .publications h2.bibliography:empty { display: none; }
</style>

<!-- _pages/publications.md -->

<!-- Bibsearch Feature -->

{% include bib_search.liquid %}

<div class="publications">

<h2 class="category">Archive Papers</h2>

{% bibliography --query @*[category=archive] %}

<h2 class="category">Work at GA Tech</h2>

{% bibliography --query @*[category=gatech] %}

<h2 class="category">Work prior to GA Tech:</h2>

{% bibliography --query @*[category=prior] %}

</div>
