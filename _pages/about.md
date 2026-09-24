---
layout: about
title: Home
permalink: /

selected_papers: true # includes a list of papers marked as "selected={true}"
social: false # includes social icons at the bottom of the page

announcements:
  enabled: false

latest_posts:
  enabled: false
---

{% include_relative shared_style.html %}

<!-- The theme hardcodes this heading as lowercase "selected publications"; capitalize it here. -->
<!-- Also hide the bib "note" line (e.g. "Publisher: ...") on the home page; it still shows on the Publications page. -->
<!-- The heading matches the names on the People page (bold, 2.25rem, normal text color); the :has rule styles the h2, the a rule is a fallback. -->
<style>
  h2:has(> a[href$="/publications/"]) { font-weight: 700; font-size: 2.25rem; color: var(--global-text-color); }
  h2 > a[href$="/publications/"] { text-transform: capitalize; font-weight: 700; font-size: 2.25rem; }
  .publications .periodical + .periodical { display: none; }
</style>

<div class="group-photo" style="line-height: 0; margin-bottom: 1.5rem;">
  {% include figure.liquid loading="eager" path="assets/img/group_photo.jpeg" class="img-fluid rounded z-depth-1" alt="The Kretchmer Group" %}
</div>

The Kretchmer Group is a multifaceted theoretical chemistry group that develops and utilizes new methods at the intersection of electronic structure and quantum dynamics. We apply these methods to understand complex electron dynamics in all its forms, investigating processes ranging from charge and spin transport in quantum materials to attosecond-scale dynamics in molecular clusters.
