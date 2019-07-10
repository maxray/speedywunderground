---
title: Shop - Compilations
permalink: "/shop/compilations"
image: "/uploads/comp.png"
layout: shop-inner
---

<div class="compilations">
    <h3>Compilations</h3>
    <ul class="comp-list">
            {% assign ordered_comps = site.releases | sort:"title" | reverse %}
            {% for release in ordered_comps  %}
            {% if release.categories contains "compilation" %}
            {% include release.html %}
            {% endif %}
        {% endfor %} 
    </ul>
</div>
