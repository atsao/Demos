---
layout: default
title: Home
permalink: /
weight: 0
---
<div class="row">

  {% assign pages = site.pages | sort: 'weight' %}
  {% assign url = page.url | remove:'index.html' %}
  {% for p in pages %}
    {% if p.layout == "page" and p.active == "y" %}
      <div class="col-xs-12 col-sm-6 col-md-4">
        <h3><a href="{{ p.url }}">{{ p.title }}</a></h3>
        <p>{{ p.description }}</p>
        <a href="{{ p.url }}" class="btn btn-success">View Project</a>
      </div>
    {% endif %}
  {% endfor %}
    
</div>
