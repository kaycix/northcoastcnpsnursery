---
permalink: /sale/shrubs/

banner:
    excerpt: Spring sale pages are under construction and shared to a limited audience. Please don't share publicly. 


layout: splash
classes: wide spring-sale
title: Spring Native Plant Sale 
excerpt: "Freshwater Farms Reserve<br/>5158 Mrytle Ave, Eureka, CA"
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/backgrounds/lupine.jpg
---

<!-- Jekyll 3.9 doesnt support and/or in where_exp so we have to do this the messy way -->

{% assign inventory_tag = "cnps_2023_spring" %}
{% assign shrub_plants = site.plants | where_exp:"item",
    "item.category == 'shrub'" %}
{% assign inventory_plants = shrub_plants | where_exp:"item",
    "item.inventory contains inventory_tag" %}

<div class="hours">
    <h4><a href="/sale/all/">All Plants</a> >  Shrubs ({{inventory_plants.size}})</h4>
</div>

{% include plant_list.html 
    plants = inventory_plants
%}

