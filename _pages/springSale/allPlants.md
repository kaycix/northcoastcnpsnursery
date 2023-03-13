---
permalink: /sale/all/

banner:
    excerpt: Spring sale pages are under construction and shared to a limited audience. Please don't share publicly. 


layout: splash
classes: wide spring-sale
title: <a href="/sale/">Spring Native Plant Sale</a> 
excerpt: "Freshwater Farms Reserve<br/>5158 Mrytle Ave, Eureka, CA"
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/backgrounds/lupine.jpg
---
{% assign inventory_tag = "cnps_2023_spring" %}
{% assign inventory_plants = site.plants | where_exp:"item",
    "item.inventory contains inventory_tag" %}

<div class="subheading">
    <h4>All Plants ({{inventory_plants.size}})</h4>
</div>

**Notice:** Our inventory list is still being finalized. Check back for updates! 
{: .notice}

<div style="margin-bottom: 20px;">
    Browse:
    <a href="/sale/shrubs/">Shrubs</a> | 
    <a href="/sale/trees/">Trees</a> |
    <a href="/sale/perennials/">Perennials</a> |
    <a href="/sale/annuals/">Annuals</a> | 
    <a href="/sale/ferns/">Ferns</a> | 
    <a href="/sale/grasses/">Grasses</a> | 
    <a href="/sale/succulents/">Succulents</a> |
    <a href="/sale/vines/">Vines</a>
</div>

{% include plant_list.html 
    plants = inventory_plants
%}
