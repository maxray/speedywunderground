---
title: Shop
permalink: "/shop/albums"
layout: shop-inner
nameclass: albums
---

<div class="eps">
    <h3>Albums</h3><div class="shop-nav"><a href="{{site.baseurl}}/shop/compilations">Compilations</a> | <a href="{{site.baseurl}}/shop/eps">EPs</a> | <a href="{{site.baseurl}}/shop/singles">7" Singles</a> | <a href="{{site.baseurl}}/shop/digital">Digital</a></div>
    <ul class="album-list">
        {% assign ordered_releases = site.releases | sort:"sku" | reverse  %}
        {% for release in ordered_releases  %}
            {% if release.categories contains "album" %}
            {% include release.html %}
            {% endif %}
        {% endfor %} 
    </ul>
</div>


