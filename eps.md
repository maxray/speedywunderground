---
title: Shop
permalink: "/shop/eps"
layout: shop-inner
nameclass: eps
---

<div class="eps">
    <h3>EPs</h3><div class="shop-nav"><a href="{{site.baseurl}}/shop/compilations">Compilations</a> <!--| <a href="{{site.baseurl}}/shop/albums">Albums</a> --> | <a href="{{site.baseurl}}/shop/singles">7" Singles</a> | <a href="{{site.baseurl}}/shop/digital">Digital</a></div>
    <ul class="single-list">
        {% assign ordered_releases = site.releases | sort:"title" | reverse %}
        {% for release in ordered_releases  %}
            {% if release.categories contains "ep" %}
            {% include release.html %}
            {% endif %}
        {% endfor %} 
    </ul>
</div>


