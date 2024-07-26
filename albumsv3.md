---
title: Shop
permalink: "/shop/albumsv3"
layout: shop-innerv3
nameclass: albums
---

<div class="eps">
    <h3>Albums</h3><div class="shop-nav"><a href="{{site.baseurl}}/shop/compilations">Compilations</a> | <a href="{{site.baseurl}}/shop/eps">EPs</a> | <a href="{{site.baseurl}}/shop/singles">7" Singles</a> | <a href="{{site.baseurl}}/shop/digital">Digital</a> | <a href="{{site.baseurl}}/shop/boxsets">Box Sets</a></div>
    <ul class="album-list">
        {% assign ordered_releases = site.releases | sort:"sku" | reverse  %}
        {% for release in ordered_releases  %}
            {% if release.categories contains "album" %}
            {% include release.html %}
            {% endif %}
        {% endfor %} 
    </ul>
</div>


