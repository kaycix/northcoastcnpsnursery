---
permalink: /garden/
layout: splash
classes: wide
title: Demonstration Garden 
#excerpt: "The one thing we need more than hope is action. Because once we start to act, hope is everywhere - Greta Thunberg"
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/garden/wildflowers.jpg

intro:
    - excerpt: "<p>The demonstration garden was created in 2019 by sustainable landscape designer Christine Kelly, with the help of CNPS and Helping Humboldt volunteers. It also functions as a living seed bank for the nursery.</p>
    <p>
        The garden is nestled in a corner of the nursery, spanning 0.03 acres (~1,120 square feet). It represents 4 distinctive eco-systems, and is home to over 90 species of Humboldt County and California native plants. Diligent plant labeling makes this garden especially useful for aspiring botanists. 
   </p>" 

gallery:
  - url: /assets/images/garden/path_with_columbines2.jpg
    image_path: /assets/images/garden/path_with_columbines2.jpg
    alt: "North Coast CNPS Demonstration Garden"
    title: "North Coast CNPS Demonstration Garden"
  - url: /assets/images/garden/grass_purple_flower.jpg
    image_path: /assets/images/garden/grass_purple_flower.jpg
    alt: "North Coast CNPS Demonstration Garden"
    title: "North Coast CNPS Demonstration Garden"
  - url: /assets/images/garden/colorful_annuals.jpg
    image_path: /assets/images/garden/colorful_annuals.jpg
    alt: "North Coast CNPS Demonstration Garden"
    title: "North Coast CNPS Demonstration Garden"
  - url: /assets/images/garden/grassy_yerba_buena.jpg
    image_path: /assets/images/garden/grassy_yerba_buena.jpg
    alt: "North Coast CNPS Demonstration Garden"
    title: "North Coast CNPS Demonstration Garden"
  - url: /assets/images/garden/pink_flowers.jpg
    image_path: /assets/images/garden/pink_flowers.jpg
    alt: "North Coast CNPS Demonstration Garden"
    title: "North Coast CNPS Demonstration Garden"
  - url: /assets/images/garden/woodland_flowers.jpg
    image_path: /assets/images/garden/woodland_flowers.jpg
    alt: "North Coast CNPS Demonstration Garden"
    title: "North Coast CNPS Demonstration Garden"

---

{% include feature_row id="intro" type="center" %}

{% include gallery caption="CK Photography" %}

<img src="/assets/images/garden/map.jpg">

<!-- filter all plants to find those with cnps_demo in garden -->
{% assign garden_tag = "cnps_demo" %}
{% assign garden_sections = "" | split: ',' %}

{% assign garden_plants = site.plants | where_exp:"item",
    "item.gardens contains garden_tag" %}

{% assign garden_sections = garden_plants | group_by_exp: "item",
    "item.gardens[garden_tag]" %}

**Notice:** The list of plants below is a work in progress. More to be added. Stay tuned! 
{: .notice}

{% for section in garden_sections %}
{{ section.name[0] | capitalize }}<br/>
<hr>
<table class="plant_list">
    {% for plant in section.items %}
<tr>
<td>
{% if plant.icon and plant.icon.small %}
<img src='{{plant.icon.small.url}}' />
{% endif %}
</td>
<td>
{% if plant.url %}
<a href="{{plant.url}}">
{% endif %}
{{ plant.name.common[0] | capitalize }}
{% if plant.url %}
</a>
{% endif %}
({{ plant.name.scientific | capitalize }})
</td>
</tr>
    {% endfor %}
</table>
{% endfor %}

