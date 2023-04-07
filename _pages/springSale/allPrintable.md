---
permalink: /sale/all/print
---
{% assign inventory_tag = "cnps_2023_spring" %}
{% assign inventory_plants = site.plants | where_exp:"item",
    "item.inventory contains inventory_tag" %}

<div class="subheading" style="margin-left:30px">
    <h4>Spring Sale 2023 Inventory List</h4>
</div>

<table class="plant_list">
<tr>
    <td>
    </td>
    <td>
        Common Name
    </td>
    <td>
        Scientific Name
    </td>
    <td>
        Humboldt Native
    </td>
</tr>
{% for plant in inventory_plants %}
<tr>
    <td>
        {{ forloop.index }}
    </td>
    <td>
        {{ plant.name.common[0] | capitalize }}
    </td>
    <td style="min-width:200px; max-width: 600px;">
        {{ plant.name.scientific | capitalize }}
    </td>
    <td style="text-align: center; min-width: 100px">
    {% if plant.humboldt_native %}
        &#x2713;
    {% endif %}
    </td>
</tr>
{% endfor %}
</table>


