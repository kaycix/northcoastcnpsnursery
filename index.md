---
title: "Welcome to our native plant nursery."
layout: splash

banner:
    excerpt: <b>Save the Date!</b> Our Native Plant Sale returns this Spring May 6 - May 7, 2023. 

header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/nursery_overview.jpg
  actions:
    - label: "Hours & Directions"
      url: "/contact/"
excerpt: "Come visit our fully volunteer-run nursery located in Freshwater Farms Reserve in Eureka, CA. We grow over 100 species of Pacific Northwest and California native plants. Our nursery has been supplying this region with beautiful native plants since 2015."

#intro: 
#    - excerpt: "We are a non-profit volunteer-run nursery located in beautiful Freshwater Farms Reserve in Eureka, CA." 
#
# add comment to kick off another build


feature_row:
  - image_path: /assets/images/starts.jpg
    alt: "Plant Sale"
    title: "Plant Sales"
    excerpt: "<img src='/assets/images/icons/stop-sign-small.png' style='float:left; margin-right: 5px;' />Hang tight! Plant sales are on hold as we gear up for our Spring sale, May 6th  & May 7th, 2023.<br/><br/>Pricing (unless otherwise marked): <br/>4-inch pot: $5.00<br/> 1-gallon pot: $10.00 - $12.00"
    #url: "/category/cnps-2022-fall"
    #url: "/category/cnps-master-inventory"
    #btn_label: "More Information"
    #btn_class: "btn--primary"
  - image_path: /assets/images/garden.jpg
    alt: "Demonstration Garden"
    title: "Demonstration Garden"
    excerpt: "The demonstration garden occupies a corner of the nursery and is a valuable example of what homeowners can accomplish on a small suburban lot."
    url: "/garden"
    btn_label: "Explore the Garden"
    btn_class: "btn--info"
  - image_path: /assets/images/plants.jpg
    alt: "Volunteer"
    title: "Volunteer"
    excerpt: "Join us as we continue to help restore local ecosystems by providing affordable native plants for the home gardener."
    url: "/volunteer"
    btn_label: "Join Our Team"
    btn_class: "btn--info"
---
<!-- TODO Make this into a template -->
{% for plant in site.plants %}
   {% if plant.plant_id == 153 %} 
<div class="feature_blurb plant_spotlight">
    {% if plant.icon and plant.icon.small and plant.icon.small.url %}
    <img class="plant align-left" src="{{plant.icon.small.url}}">
    {% endif %}
    <div>
        <img class="spotlight" src="/assets/images/icons/spotlight.png" />
        <h2>
            {% if plant.common_name and plant.common_name.size > 0 %}
            Plant Spotlight: <span>{{plant.common_name[0]}}</span>
            {% endif %}
        </h2>
        <div class="info">
            <div class="scientific_name">
                {% if plant.title %}
                <b>Scientific Name:</b> {{plant.title | capitalize }}
                {% endif %}
            </div>
            <div class="description">
                {% if plant.description and plant.description.short %}
                {{ plant.description.short }}
                {% endif %}
            </div>
            {% if plant.references and plant.references.size > 0 and plant.references[0].url and plant.references[0].name  %}
            <a class="btn--inverse btn" href="{{plant.references[0].url}}">View on {{plant.references[0].name}}</a>
            {% endif %}
        </div>
    </div>
    <div class="clear"></div>
</div>
    {% endif %}
{% endfor %}


{% include feature_row %}

<div class="feature_blurb consultations">
    <h2>
        Native Plant Consultations
    </h2>
    <div class="info">
        <div class="description">
            The North Coast CNPS provides free on-site landscaping consultations. 
            Volunteer consultants will answer questions and discuss recommendations for
            <ul>
                <li>tackling invasives</li>
                <li>handling landscaping challenges</li>
                <li>finding the right natives to fit your needs</li>
            </ul>
            Wherever you are in your native plant journey, our consultants can help!
        </div>
        <a class="btn btn--primary" href="mailto:nc.cnps.consult@gmail.com?subject=New Consultation Request!">Request a Free Consultation</a>
    </div>
</div>
