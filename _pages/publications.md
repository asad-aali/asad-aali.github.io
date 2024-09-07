---
layout: page
permalink: /publications/
title: publications
description: 
nav: true
nav_order: 2
---

<div class="publication-list">
  {% for pub in site.data.papers %}
    <div class="publication-item">
      <!-- Cover Image on the Left -->
      <div class="cover-image">
        <img src="{{ pub.cover_image }}" alt="Cover image for {{ pub.title }}">
      </div>
      
      <!-- Publication Details on the Right -->
      <div class="publication-details">
        <h2>{{ pub.title }}</h2>
        <p>{{ pub.author }}</p>
        <p><em>{{ pub.journal }}</em>, {{ pub.year }}</p>
        <div class="publication-links">
          {% if pub.html %}
            <a href="{{ pub.html }}" class="button">HTML</a>
          {% endif %}
          {% if pub.pdf %}
            <a href="{{ pub.pdf }}" class="button">PDF</a>
          {% endif %}
          {% if pub.code %}
            <a href="{{ pub.code }}" class="button">CODE</a>
          {% endif %}
          {% if pub.slides %}
            <a href="{{ pub.slides }}" class="button">SLIDES</a>
          {% endif %}
        </div>
      </div>
    </div>
  {% endfor %}
</div>