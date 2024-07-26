---
title: Shop - Compilations
permalink: "/shop/compilationsv3"
layout: shop-innerv3
nameclass: compilations
---

<div class="compilations">
    <h3>Compilations</h3>
    <div class="shop-nav"><a href="{{site.baseurl}}/shop/albums">Albums</a> | <a href="{{site.baseurl}}/shop/eps">EPs</a> | <a href="{{site.baseurl}}/shop/singles">7" Singles</a> | <a href="{{site.baseurl}}/shop/digital">Digital</a> | <a href="{{site.baseurl}}/shop/boxsets">Box Sets</a></div> 
    <ul class="comp-list">
            {% assign ordered_comps = site.releases | sort:"cataloguenumber" | reverse %}
            {% for release in ordered_comps  %}
            {% if release.categories contains "compilation" %}
            {% include releasev3.html %}
            {% endif %}
        {% endfor %} 
    </ul>
</div>
