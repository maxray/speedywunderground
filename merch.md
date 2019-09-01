---
title: Shop
permalink: "/shop/merch"
layout: shop-inner
nameclass: merch
---

<div class="merch">
    <h3> Merch</h3><div class="shop-nav"><a href="{{site.baseurl}}/shop/compilations">Compilations</a> | <a href="{{site.baseurl}}/shop/eps">EPs</a> | <a href="{{site.baseurl}}/shop/singles">Singles</a></div>
    <div class="merch-list">
            {% assign ordered_merch = site.products | sort:"title"  %}
            {% for product in ordered_merch  %}
                {% if product.categories contains "merch" %}
                    {% include product.html %}
                {% endif %}
            {% endfor %} 
    </div>
</div>
