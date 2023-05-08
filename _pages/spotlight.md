---
permalink: /spotlight/
layout: splash
classes: wide
title: Native Plant Spotlight 
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/garden/grass.jpg
  # overlay_image: /assets/images/icons/spotlight_background.jpg

plant_spotlights: 
    april: 224 # western houndstongue 
    march: 73 # red flowering currant
    february: 195 # coast silk tassel
    january: 153 # mistmaiden
---

{% for objs in page.plant_spotlights %}
{% assign month = objs[0] %} 
{% assign plant_id = objs[1] %} 
{% for plant in site.plants %}
    {% if plant.plant_id == plant_id %}
        {% include plant_summary_card.html plant=plant title=month %} 
    {% endif %}
{% endfor %}
{% endfor %}

