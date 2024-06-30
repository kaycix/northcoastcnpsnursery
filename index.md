---
title: "Welcome to our native plant nursery."
layout: splash

header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/nursery_overview.jpg
  actions:
    - label: "Hours & Directions"
      url: "/contact/"
excerpt: "Come visit our fully volunteer-run nursery located in Freshwater Farms Reserve in Eureka, CA. We grow over 100 species of Pacific Northwest and California native plants. Our nursery has been supplying this region with beautiful native plants since 2015."


#banner: 
    #excerpt: ""

sale_banner: false

#intro: 
#    - excerpt: "We are a non-profit volunteer-run nursery located in beautiful Freshwater Farms Reserve in Eureka, CA." 
#

plant_spotlight_id: 147 
plant_spotlight_title: August 

feature_row:
  - image_path: /assets/images/sale-feature.jpg
    alt: "Plant Sale"
    title: "Plant Sales"
    excerpt: "The nursery and demonstration garden are open during <a href='/contact'>Volunteer Hours</a>. Cash or check are appreciated, but we also accept credit.<br/><br/>Pricing, unless otherwise marked: <br/>4-inch pot: $5.00<br/> 1-gallon pot: $10.00 - $12.00"
    #excerpt: "Plant sales have resumed during our regular <a href='/contact'>Volunteer Open Hours</a>. Our inventory (which peaks during our seasonal sales in May and September) is greatly reduced. Cash or check is appreciated."
    #excerpt: "Plant sales have resumed during our <a href='/contact'>Volunteer Open Hours</a>. Our inventory (which peaks during our seasonal sales in May and September) is greatly reduced. Cash or check is appreciated.<br/><br/>Pricing, unless otherwise marked: <br/>4-inch pot: $5.00<br/> 1-gallon pot: $10.00 - $12.00"
    url: "/inventory/cnps-2024-summer"
    btn_label: "View Inventory"
    btn_class: "btn--info"
  - image_path: /assets/images/garden/garden-feature.jpg
    alt: "Demonstration Garden"
    title: "Demonstration Garden"
    excerpt: "The demonstration garden occupies a corner of the nursery and is a valuable example of what homeowners can accomplish on a small suburban lot."
    url: "/garden"
    btn_label: "Explore the Garden"
    btn_class: "btn--info"
  - image_path: /assets/images/volunteers/hands-feature.jpg
    alt: "Volunteer"
    title: "Volunteer"
    excerpt: "Volunteer at the nursery and make a difference! Learn all about identifying and growing native plants while helping us in our mission of providing affordable native plants for the home gardener."
    url: "/volunteer"
    btn_label: "Join Our Team"
    btn_class: "btn--info"
---
{% include feature_row %}

<div style="display:none">
    {% for plant in site.plants %}
        {% if plant.plant_id == page.plant_spotlight_id %}
            {% include plant_summary_card.html title=page.plant_spotlight_title plant=plant %} 
        {% endif %}
    {% endfor %}
</div>
<div class="feature_blurb consultations" style="display:none">
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
<div class="instagram" style="text-align:center">
    <img src="/assets/images/icons/instagram-bw.png" style="margin-bottom: 15px"/>
    <h2 style="padding:0;margin:0;line-height:1; border-bottom: 0">Follow Our Nursery </h2>
    <div class="powr-social-feed" id="cb2d6f13_1675967745"></div><script src="https://www.powr.io/powr.js?platform=html"></script>
</div>
