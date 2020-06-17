---
title: Shop
permalink: "/shop/digital"
layout: shop-inner
nameclass: digital
---

<div class="singles">
    <h3>Digital</h3><div class="shop-nav"><a href="{{site.baseurl}}/shop/compilations">Compilations</a> | <a href="{{site.baseurl}}/shop/albums">Albums</a> | <a href="{{site.baseurl}}/shop/eps">EPs</a> | <a href="{{site.baseurl}}/shop/singles">7" Singles</a></div>
    <h3>Quarantine Series</h3>
    <ul class="single-list">
        {% assign ordered_releases = site.releases  | sort:"cataloguenumber" | reverse  %}
        {% for release in ordered_releases  %}
             {% if release.categories contains "digital" and release.tags contains "quarantine"%}
            {% include release.html %}
            {% endif %}
        {% endfor %} 
    </ul>
    <hr>
     <h3>Digital Streams</h3>
     <ul class="single-list">
        {% assign ordered_releases = site.releases  | sort:"cataloguenumber" | reverse  %}
        {% for release in ordered_releases  %}
            {% if release.categories contains "digital" and release.tags contains "stream"%}
            {% include release.html %}
            {% endif %}
        {% endfor %} 
    </ul>
</div>


