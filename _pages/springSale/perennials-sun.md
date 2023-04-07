---
permalink: /sale/perennials/sun/

layout: splash
classes: wide spring-sale
title: <a href="/sale/">Spring Native Plant Sale</a> 
excerpt: "Freshwater Farms Reserve<br/>5158 Mrytle Ave, Eureka, CA"
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/backgrounds/lupine.jpg
---

<!-- Jekyll 3.9 doesnt support and/or in where_exp so we have to do this the messy way -->

{% assign inventory_tag = "cnps_2023_spring" %}
{% assign perennial_plants = site.plants | where_exp:"item",
    "item.category == 'perennial herb'" %}

{% assign inventory_plants = perennial_plants | where_exp:"item",
    "item.inventory contains inventory_tag" %}

{% assign sun_plants = inventory_plants | where_exp:"item",
    "item.sun_requirements contains 'Full Sun'" %}

<div class="hours">
    <h4><a href="/sale/all/">All Plants</a> >  <a href="/sale/perennials/">Perennials</a> > Sun ({{sun_plants.size}}) </h4>
</div>
<div style="margin-bottom: 20px;">
    Browse by:
    Sun |
    <a href="/sale/perennials/shade/">Shade</a> 
</div>

{% include plant_list.html 
    plants = sun_plants
%}

