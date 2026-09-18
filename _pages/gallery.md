---
layout: page
title: Gallery
permalink: /gallery/
nav: true
nav_order: 8.5
description: Photos from the group... when we get some

gallery_images:
  - path: assets/img/group_photo.jpeg
    alt: The Kretchmer Group
---

<!--
  To add a photo: append an entry to `gallery_images` in this page's front matter, e.g.
    - path: assets/img/your_photo.jpg
      alt: Description of the photo
-->
<div class="gallery grid grid-cols-2 md:grid-cols-3 gap-4">
  {% for photo in page.gallery_images %}
    {% include figure.liquid path=photo.path class="img-fluid rounded z-depth-1" alt=photo.alt %}
  {% endfor %}
</div>
