---
layout: page
permalink: /publications/
title: Publications
nav: true
nav_order: 3
---

{% include_relative shared_style.html %}

<style>
  /* Heading for the earlier-work section; matches the bold headings on the People page */
  .publications h2.category { font-weight: 700; font-size: 2.25rem; color: var(--global-text-color); margin-top: 3.5rem; margin-bottom: 0.5rem; }
  /* Year headings: bold and in the normal text color (theme default is a faint gray) */
  .publications h2.bibliography { font-weight: 700; font-size: 1.75rem; color: var(--global-text-color); }
</style>

<!-- _pages/publications.md -->

<!-- Bibsearch Feature -->

{% include bib_search.liquid %}

<div class="publications">

<!-- Archive papers sit above the newest year as one ungrouped block, headed like a year -->
<h2 class="bibliography">Archive</h2>

{% bibliography --group_by none --query @*[category=archive] %}

{% bibliography --query @*[category=gatech] %}

<h2 class="category">Work prior to GA Tech:</h2>

{% bibliography --query @*[category=prior] %}

</div>
