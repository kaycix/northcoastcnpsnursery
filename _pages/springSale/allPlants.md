---
permalink: /sale/all/

layout: splash
classes: wide spring-sale
title: Spring Native Plant Sale 
excerpt: "Freshwater Farms Reserve<br/>5158 Mrytle Ave, Eureka, CA"
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/backgrounds/lupine.jpg
---
{% assign inventory_tag = "cnps_2023_spring" %}
{% assign inventory_plants = site.plants | where_exp:"item",
    "item.inventory contains inventory_tag" %}

<div class="hours">
    <h4>All Plants ({{inventory_plants.size}})</h4>
</div>

{% include plant_list.html 
    plants = inventory_plants
%}