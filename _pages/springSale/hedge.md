---
permalink: /sale/hedge/

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

{% assign tag = "hedge" %}
{% assign inventory_tag = "cnps_2023_spring" %}

{% assign plants = site.plants | where_exp:"item",
    "item.tags contains tag" %}
{% assign inventory_plants = plants | where_exp:"item",
    "item.inventory contains inventory_tag" %}

<div class="subheading">
    <h4><a href="/sale/all/">All Plants</a> >  Hedge Plants ({{inventory_plants.size}})</h4>
    <p class="notice">
    A native hedge is the perfect blend of beauty and functionality. Make sure you also check out our list of <a href="/sale/trees">Trees</a>. Make sure to click into the Calscape link if you want to look for evergreen varities.
    </p>
</div>

{% include plant_list.html 
    plants = inventory_plants
%}




