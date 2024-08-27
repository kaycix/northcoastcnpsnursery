---
permalink: /sale/deerresistant/

layout: splash
classes: wide spring-sale
#title: <a href="/sale/">Spring Native Plant Sale</a> 
title: <a href="/sale/">Fall Native Plant Sale</a> 
excerpt: "Freshwater Farms Reserve<br/>5158 Mrytle Ave, Eureka, CA"
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  #overlay_image: /assets/images/backgrounds/waxy_coneflower2.jpeg
  overlay_image: /assets/images/backgrounds/lupine.jpg
---

<!-- Jekyll 3.9 doesnt support and/or in where_exp so we have to do this the messy way -->

{% assign tag = "deerResistant" %}
{% assign inventory_tag = "cnps_2024_fall" %}

{% assign plants = site.plants | where_exp:"item",
    "item.tags contains tag" %}
{% assign inventory_plants = plants | where_exp:"item",
    "item.inventory contains inventory_tag" %}

<div class="subheading">
    <h4><a href="/sale/all/">All Plants</a> >  Deer Resistant ({{inventory_plants.size}})</h4>
    <p class="notice">
    There are few gardening heartaches quite like waking up to find that hungry deer have visited your garden! These are some plants that Calscape has tagged as being deer resistant. We have to add that an extremely hungry deer and young deer will try anything. However, this is a great list to browse if you've had a history with deer problems. 
    </p>
</div>

{% include plant_list.html 
    plants = inventory_plants
%}



