---
permalink: /sale/annuals/

layout: splash
classes: wide spring-sale
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
{% assign annual_plants = site.plants | where_exp:"item",
    "item.category == 'annual herb'" %}
{% assign inventory_plants = annual_plants | where_exp:"item",
    "item.inventory contains inventory_tag" %}

<div class="hours">
    <h4><a href="/sale/all/">All Plants</a> >  Annuals ({{inventory_plants.size}})</h4>
</div>

{% include plant_list.html 
    plants = inventory_plants
%}

