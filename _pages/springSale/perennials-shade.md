---
permalink: /sale/perennials/shade/

layout: splash
classes: wide spring-sale
#title: <a href="/sale/">Fall Native Plant Sale</a> 
title: <a href="/sale/">Spring Native Plant Sale</a> 
excerpt: "Freshwater Farms Reserve<br/>5158 Mrytle Ave, Eureka, CA"
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  #overlay_image: /assets/images/backgrounds/waxy_coneflower2.jpeg
  overlay_image: /assets/images/backgrounds/lupine.jpg
---

<!-- Jekyll 3.9 doesnt support and/or in where_exp so we have to do this the messy way -->

{% assign inventory_tag = "cnps_2025_spring" %}
{% assign perennial_plants = site.plants | where_exp:"item",
    "item.category == 'perennial herb'" %}

{% assign inventory_plants = perennial_plants | where_exp:"item",
    "item.inventory contains inventory_tag" %}

{% assign shade_plants = inventory_plants | where_exp:"item",
    "item.sun_requirements contains 'Full Shade'" %}

<div class="hours">
    <h4><a href="/sale/all/">All Plants</a> >  <a href="/sale/perennials/">Perennials</a> > Shade ({{shade_plants.size}}) </h4>
</div>
<div style="margin-bottom: 20px;">
    Browse by:
    <a href="/sale/perennials/sun/">Sun</a> |
    Shade 
</div>

{% include plant_list.html 
    plants = shade_plants
%}


