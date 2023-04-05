---
permalink: /sale/
layout: splash
# tried to inherit from sale layout which inherited from splash layout but splash layout was called first? resulting in blanks where sale defined variables

classes: wide spring-sale

title: <a href="/sale/">Spring Native Plant Sale</a> 
excerpt: "Freshwater Farms Reserve<br/>5158 Mrytle Ave, Eureka, CA"

header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/backgrounds/lupine.jpg

feature_row:
  - image_path: /assets/images/backgrounds/bad-parking.jpg
    alt: "Parking"
    title: "Parking"
    excerpt: "Parking is available at Freshwater Farms Reserve. Sign Up Genius is required for Saturday visitors due to parking limitations."
    url: "https://goo.gl/maps/Qg5BhABbH88Jaser9"
    btn_label: "View Map"
    btn_class: "btn--primary"
  - image_path: /assets/images/plants.jpg
    alt: "Volunteer"
    title: "Volunteer"
    excerpt: "Our sale is a fully volunteer-run event. Please contact us if you are interested in helping out."
    url: "/volunteer/#sale"
    btn_label: "More Information"
    btn_class: "btn--primary"
  - image_path: /assets/images/starts.jpg
    alt: "Inventory"
    title: "Participating Nurseries & Vendors"
    excerpt: "Proudly partnering with Samara Restoration, Mattole Restoration Council, Lost Foods, Bob Vogt Trees, Beresford's Bulbs and Brant's Plants."
    #url: ""
    #btn_label: "More Information"
    #btn_class: "btn--primary"
---
<div class="hours">
    <h4>Saturday May 6, Sign Up to Shop!*</h4>
    <h4>Sunday May 7, Open 10:00am - 3:00 pm.</h4>
</div>
<p style="text-align:center; font-size: 0.8em">
* Saturday shoppers will need to sign up for a shopping slot via Sign Up Genius - available April 8.
</p>

{% assign inventory_tag = "cnps_2023_spring" %}
{% assign inventory_plants = site.plants | where_exp:"item",
    "item.inventory contains inventory_tag" %}

<div class="browse-block">
    <div class="heading">
        <h1>Browse our Inventory:</h1>
        <a class="btn btn--primary" href="/sale/all/">View All Plants&nbsp; 
            <span class="count">&nbsp;({{ inventory_plants.size }})</span>
        </a>
    </div>
    <div class="content">
        <div class="inventory_type box">
            <h4>
                Browse by Type
            </h4>
            <div class="column">
                <div class="row">
                    <a href="/sale/shrubs/">Shrubs</a>
                </div>
                <div class="row">
                    <a href="/sale/perennials/">Perennials</a>
                </div>
                <div class="row">
                    <a href="/sale/annuals/">Annuals</a>
                </div>
                <div class="row">
                    <a href="/sale/vines/">Vines</a> 
                </div>
            </div>
            <div class="column">
                <div class="row">
                    <a href="/sale/trees/">Trees</a>
                </div>
                <div class="row">
                    <a href="/sale/ferns/">Ferns</a>
                </div>
                <div class="row">
                    <a href="/sale/grasses/">Grasses</a>
                </div>
                <div class="row">
                    <a href="/sale/succulents/">Succulents</a>
                </div>
            </div>
            <div class="clear"></div>
        </div>
        <div class="inventory_category box">
            <h4>
            Browse by Category
            </h4>
            <div class="column">
                <div class="row">
                    <a href="/sale/beginner/">
                    Beginner Favorites
                    </a>
                </div>
                <div class="row">
                    <a href="/sale/hedge/">
                    Hedges
                    </a>
                </div>
                <div class="row">
                    <a href="/sale/groundcover/">
                    Ground Covers
                    </a>
                </div>
            </div>
            <div class="column">
                <div class="row">
                    <a href="/sale/butterfly/">
                    Butterfly Garden
                    </a>
                </div>
                <div class="row">
                    <a href="/sale/drought/">
                    Drought-Tolerant
                    </a>
                </div>
                <div class="row">
                    <a href="/sale/moisture">
                    Moisture-Loving
                    </a>
                </div>
            </div>
            <div class="clear"></div>
            <a href="" style="font-size: 0.9em; display:none;">Browse More Categories..</a>
        </div>
        <div class="clear"></div>
    </div>
</div>
{% include feature_row %}

<div class="thanks-block">
    <h1>Thank You</h1>
    <div>
    <p>
    Thank you for being with us on this journey to spread native plants and protect biodiversity!
    </p>
    <p>Thank you to everyone who shops our sales - from those of you rewilding entire yards to those of you tending a few native plants on your balcony. Your stories continue to motivate and inspire us.</p>
    <p>We appreciate the nurseries and vendors that we partner with and the community of sharing and support you offer us. We feel so lucky to be working alongside such passionate people.</p>
    <p>Thank you to nursery managers Chris and Barbara for your tireless efforts and countless hours of hard work. We couldn't ask for more dedicated leaders.</p>
    <p>Lastly, huge thank yous to all our nursery and garden volunteers. Whether you have volunteered for one hour or many more, we appreciate you! This has been a particularly long winter but seeing everyone show up, ready to work in the cold mornings warms our hearts. 
    </p>
    </div>
</div>
