---
title: Shop - Compilations
permalink: "/shop/compilations"
layout: shop-inner
---

<div class="compilations">
    <h3>Compilations</h3><div class="shop-nav"><a href="{{site.baseurl}}/shop/singles">Singles</a> | <a href="{{site.baseurl}}/shop/merch">Merch</a></div>
    <ul class="comp-list">
            {% assign ordered_comps = site.releases | sort:"title" | reverse %}
            {% for release in ordered_comps  %}
            {% if release.categories contains "compilation" %}
            {% include release.html %}
            {% endif %}
        {% endfor %} 
    </ul>
</div>
