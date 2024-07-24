---
title: Shop
permalink: "/shop/singlesv3"
layout: shop-innerv3
nameclass: singles
---

<div class="singles">
    <h3>7" Singles</h3><div class="shop-nav"><a href="{{site.baseurl}}/shop/compilations">Compilations</a> |  <a href="{{site.baseurl}}/shop/albums">Albums</a> | <a href="{{site.baseurl}}/shop/eps">EPs</a> | <a href="{{site.baseurl}}/shop/digital">Digital</a> | <a href="{{site.baseurl}}/shop/boxsets">Box Sets</a></div>
    <ul class="single-list">
        {% assign ordered_releases = site.releases  | sort:"cataloguenumber" | reverse  %}
        {% for release in ordered_releases  %}
            {% if release.categories contains "single" %}
            {% include releasev3.html %}
            {% endif %}
        {% endfor %} 
    </ul>
</div>


