---
title: Shop - Compilations
permalink: "/shop/compilations"
layout: shop-inner
nameclass: compilations
---

<div class="compilations">
    <h3>Compilations</h3>
    <div class="shop-nav"><a href="{{site.baseurl}}/shop/albums">Albums</a> | <a href="{{site.baseurl}}/shop/eps">EPs</a> | <a href="{{site.baseurl}}/shop/singles">7" Singles</a> | <a href="{{site.baseurl}}/shop/digital">Digital</a></div> 
    <ul class="comp-list">
            <!-- {% assign ordered_comps = site.releases | sort:"cataloguenumber" | reverse %} -->
           {% assign ordered_comps = site.releases  %}
           {% for release in ordered_comps  %}
            {% if release.categories contains "compilation" %}
            {% include release.html %}
            {% endif %}
        {% endfor %} 
    </ul>
</div>
