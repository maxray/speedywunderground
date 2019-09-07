---
title: Shop
permalink: "/shop/singles"
layout: shop-inner
nameclass: singles
---

<div class="singles">
    <h3>Singles</h3><div class="shop-nav"><a href="{{site.baseurl}}/shop/compilations">Compilations</a> | <a href="{{site.baseurl}}/shop/eps">EPs</a> | <a href="{{site.baseurl}}/shop/merch">Merch</a></div>
    <ul class="single-list">
        {% assign ordered_releases = site.releases | sort:"sku" | reverse %}
        {% for release in ordered_releases  %}
            {% if release.categories contains "single" %}
            {% include release.html %}
            {% endif %}
        {% endfor %} 
    </ul>
</div>


