---
layout: about
title: Home
permalink: /
subtitle: Theoretical chemistry at the intersection of electronic structure and quantum dynamics.

selected_papers: true # includes a list of papers marked as "selected={true}"
social: false # includes social icons at the bottom of the page

announcements:
  enabled: false

latest_posts:
  enabled: false
---

<div class="group-photo" style="position: relative; line-height: 0;">
  {% include figure.liquid loading="eager" path="assets/img/group_photo.jpeg" class="img-fluid rounded z-depth-1" alt="The Kretchmer Group" %}
  {% assign people = "dan,11,30,8,48|josh,17.5,33,9,50|owen,27,34,8,46|jordan,45.5,22,8.5,52|mikhayla,51.5,40,9,48|victor,64.5,30,8.5,50" | split: "|" %}
  {% for p in people %}
    {% assign f = p | split: "," %}
    <a
      href="{{ '/people/#' | append: f[0] | relative_url }}"
      title="{{ f[0] | capitalize }}"
      aria-label="{{ f[0] | capitalize }}"
      style="position: absolute; left: {{ f[1] }}%; top: {{ f[2] }}%; width: {{ f[3] }}%; height: {{ f[4] }}%; z-index: 2;"
    ></a>
  {% endfor %}
</div>

<div class="caption">The Kretchmer Group. Click a face to jump to that person.</div>

The Kretchmer Group is a multifaceted theoretical chemistry group that develops and utilizes new methods at the intersection of electronic structure and quantum dynamics. We apply these methods to understand complex electron dynamics in all its forms, investigating processes ranging from charge and spin transport in quantum materials to attosecond-scale dynamics in molecular clusters.

We are located in the [School of Chemistry and Biochemistry](https://chemistry.gatech.edu/) at the Georgia Institute of Technology. If you are interested in joining us, see our [Join Us!]({{ '/join/' | relative_url }}) page.
