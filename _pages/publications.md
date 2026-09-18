---
layout: page
permalink: /publications/
title: Publications
nav: true
nav_order: 3
---

{% include_relative shared_style.html %}

<!-- _pages/publications.md -->

<!-- Bibsearch Feature -->

{% include bib_search.liquid %}

<div class="publications">

{% bibliography --query @*[category=gatech] %}

<h2 class="category">Work prior to GA Tech:</h2>

{% bibliography --query @*[category=prior] %}

</div>
