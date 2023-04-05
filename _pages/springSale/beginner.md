---
permalink: /sale/beginner/

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

{% assign tag = "beginner" %}
{% assign inventory_tag = "cnps_2023_spring" %}

{% assign plants = site.plants | where_exp:"item",
    "item.tags contains tag" %}
{% assign inventory_plants = plants | where_exp:"item",
    "item.inventory contains inventory_tag" %}

<div class="subheading">
    <h4><a href="/sale/all/">All Plants</a> >  Beginner Favorites ({{inventory_plants.size}})</h4>
    <p class="notice">
    Starting out with natives can be an exciting but daunting process. Here are a few of our favorites to help get you started. Our best advice is to get to know your site (sun exposure, existing plants, etc) and don't be afraid to experiment and embrace the learning curve that comes with trying new things.
    </p>
</div>

{% include plant_list.html 
    plants = inventory_plants
%}


