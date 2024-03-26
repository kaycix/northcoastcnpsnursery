---
permalink: /sale/butterfly/

layout: splash
classes: wide spring-sale
title: <a href="/sale/">Spring Native Plant Sale</a> 
#title: <a href="/sale/">Fall Native Plant Sale</a> 
excerpt: "Freshwater Farms Reserve<br/>5158 Mrytle Ave, Eureka, CA"
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  #overlay_image: /assets/images/backgrounds/waxy_coneflower2.jpeg
  overlay_image: /assets/images/backgrounds/lupine.jpg
---

<!-- Jekyll 3.9 doesnt support and/or in where_exp so we have to do this the messy way -->

{% assign tag = "butterfly" %}
{% assign inventory_tag = "cnps_2024_spring" %}

{% assign plants = site.plants | where_exp:"item",
    "item.tags contains tag" %}
{% assign inventory_plants = plants | where_exp:"item",
    "item.inventory contains inventory_tag" %}

{% assign inventory_perennial_plants = inventory_plants | where_exp:"item",
    "item.category == 'perennial herb'" %}

<div class="subheading">
    <h4><a href="/sale/all/">All Plants</a> >  Butterfly Garden ({{inventory_perennial_plants.size}})</h4>
    <p class="notice">
    Is there anything more rewarding than a native plant garden humming with insect activity? Click into the Calscape link to learn about which butterfly species are attracted to each plant. 
    </p>
</div>

{% include plant_list.html 
    plants = inventory_perennial_plants
%}




