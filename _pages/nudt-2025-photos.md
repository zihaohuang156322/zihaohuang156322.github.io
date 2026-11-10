---
layout: academic
permalink: /talks/nudt-2025/photos/
title: "NUDT Seminar 2025 Photos"
seo_title: "NUDT Seminar 2025 Photos | Ricardo Zihao Huang"
description: "Photos from Ricardo Zihao Huang's seminar at the National University of Defense Technology in 2025."
nav_key: talks
---

<h1 class="page-heading">NUDT Seminar 2025 Photos</h1>

<p class="gallery-context">National University of Defense Technology, China · Dec. 28, 2025</p>

{% assign gallery_prefix = '/images/talks/nudt-2025/' %}
{% assign photo_count = 0 %}
<div class="photo-gallery">
  {% for image in site.static_files %}
    {% assign image_extension = image.extname | downcase %}
    {% if image.path contains gallery_prefix %}
      {% if image_extension == '.jpg' or image_extension == '.jpeg' or image_extension == '.png' or image_extension == '.webp' %}
        {% assign photo_count = photo_count | plus: 1 %}
        <figure class="photo-gallery-item">
          <a href="{{ image.path | relative_url }}">
            <img src="{{ image.path | relative_url }}" alt="NUDT seminar photo {{ photo_count }}" loading="lazy" decoding="async">
          </a>
        </figure>
      {% endif %}
    {% endif %}
  {% endfor %}
</div>

{% if photo_count == 0 %}
  <p class="gallery-empty">Photos will be added here.</p>
{% endif %}
