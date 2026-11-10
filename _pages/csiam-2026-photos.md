---
layout: academic
permalink: /talks/csiam-2026/photos/
title: "CSIAM 2026 Photos"
seo_title: "CSIAM 2026 Photos | Ricardo Zihao Huang"
description: "Photos from Ricardo Zihao Huang's talk at CSIAM 2026 at Hebei Normal University."
nav_key: talks
---

<h1 class="page-heading">CSIAM 2026 Photos</h1>

<p class="gallery-context">Hebei Normal University, China · May 17, 2026</p>

{% assign gallery_prefix = '/images/talks/csiam-2026/' %}
{% assign photo_count = 0 %}
<div class="photo-gallery">
  {% for image in site.static_files %}
    {% assign image_extension = image.extname | downcase %}
    {% if image.path contains gallery_prefix %}
      {% if image_extension == '.jpg' or image_extension == '.jpeg' or image_extension == '.png' or image_extension == '.webp' %}
        {% assign photo_count = photo_count | plus: 1 %}
        <figure class="photo-gallery-item">
          <a href="{{ image.path | relative_url }}">
            <img src="{{ image.path | relative_url }}" alt="CSIAM 2026 conference photo {{ photo_count }}" loading="lazy" decoding="async">
          </a>
        </figure>
      {% endif %}
    {% endif %}
  {% endfor %}
</div>

{% if photo_count == 0 %}
  <p class="gallery-empty">Photos will be added here.</p>
{% endif %}
