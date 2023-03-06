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

plant_spotlight_id: 73 

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
{% for plant in site.plants %}
    {% if plant.plant_id == page.plant_spotlight_id %}
        {% include plant_summary_card.html plant=plant %} 
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
<div class="instagram" style="text-align:center">
    <img src="/assets/images/icons/instagram-bw.png" style="margin-bottom: 15px"/>
    <h2 style="padding:0;margin:0;line-height:1; border-bottom: 0">Follow Our Nursery </h2>
    <div class="powr-social-feed" id="cb2d6f13_1675967745"></div><script src="https://www.powr.io/powr.js?platform=html"></script>
</div>
