---
title: Shop - Box Sets
permalink: "/shop/boxsets"
layout: shop-inner
nameclass: boxsets
---

<div class="boxsets">
<h3>Box Sets</h3><div class="shop-nav"><a href="{{site.baseurl}}/shop/compilations">Compilations</a> | <a href="{{site.baseurl}}/shop/eps">EPs</a> | <a href="{{site.baseurl}}/shop/singles">7" Singles</a> | <a href="{{site.baseurl}}/shop/digital">Digital</a></div>
    <div class="boxsets">
        {% assign ordered_releases = site.releases | sort:"sku" | reverse  %}
        {% for release in ordered_releases  %}
            {% if release.categories contains "boxset" %}
            {% include bs-release.html %}
            {% endif %}
        {% endfor %} 
    </div>
</div>
