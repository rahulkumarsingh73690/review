---
layout: default
type: theme
title: Social App
description: All New Social Apps Collection
permalink: /application/social/

meta-title: Social App
meta-description:  All New Social Apps Collection
---
  
{% include masthead/masthead-page.html %}

<div class="container">

  <!-- Show paginated posts for the specificed collection -->
  <div class="row">
    {% assign sorted = site.application | sort: "rank" %}
    {% for application in sorted %}
    {% if application.categories contains 'social' %}
    <div class="col-md-4">
      <div class="item-preview mb-5">
        <a class="item-preview-img box-shadow-lg d-block mb-3" href="{{ application.src }}">
          <img class="img-fluid" src="{{ application.img-thumbnail }}" alt="{{ application.img-desc }}">
        </a>
        <div class="item-preview-title">{{ application.title }}</div>
        <div class="item-preview-description">{{ application.bump }}</div>
      </div>
    </div>
    {% endif %}
    {% endfor %}

  </div>
  <!-- /.row -->


</div>
<!-- /.container -->
