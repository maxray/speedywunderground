---
title: Shop
permalink: "/shop/singles"
image: "/uploads/comp.png"
layout: shop-inner
---

<div class="singles">
    <h3>Singles</h3><div class="shop-nav"><a href="{{site.baseurl}}/shop/compilations">Compilations</a> | <a href="{{site.baseurl}}/shop/merch">Merch</a></div>
    <ul class="single-list">
        {% assign ordered_releases = site.releases | sort:"title" | reverse %}
        {% for release in ordered_releases  %}
            {% if release.categories contains "single" %}
            {% include release.html %}
            {% endif %}
        {% endfor %} 
    </ul>
</div>


