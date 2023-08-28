---
permalink: /sale/
layout: splash
# tried to inherit from sale layout which inherited from splash layout but splash layout was called first? resulting in blanks where sale defined variables

classes: wide spring-sale

title: <a href="/sale/">Fall Native Plant Sale</a> 
excerpt: "Freshwater Farms Reserve<br/>5158 Mrytle Ave, Eureka, CA"

header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/backgrounds/waxy_coneflower2.jpeg

feature_row:
  - image_path: /assets/images/backgrounds/bad-parking.jpg
    alt: "Parking"
    title: "Parking"
    excerpt: "Parking is available at Freshwater Farms Reserve. Accessible parking is located directly in front of the barn and available on a first-come, first-served basis"
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
    excerpt: "Proudly partnering with Samara Restoration, Lost Foods, Bob Vogt Trees, Beresford's Bulbs and Brant's Plants."
    #url: ""
    #btn_label: "More Information"
    #btn_class: "btn--primary"
---
<div class="hours">
    <h4>Saturday September 23, Sign Up to Shop*</h4><!-- <a href="https://www.signupgenius.com/go/904054DA5A823A2F94-spring1" target="_blank">Sign Up to Shop</a>!</h4> -->
    <h4>Sunday September 24, Open 10:00am - 3:00 pm</h4>
</div>
<p style="text-align:center; font-size: 0.8em">
* Saturday shoppers will need to sign up for a shopping slot via Sign Up Genius - available September 1. 
</p>
<!--
<p style="text-align:center; font-size: 0.8em">
* Sunday shoppers stop by whenever. No signups necessary! 
</p>
-->

{% assign inventory_tag = "cnps_2023_fall" %}
{% assign inventory_plants = site.plants | where_exp:"item",
    "item.inventory contains inventory_tag" %}

<div class="browse-block">
    <p class="notice--warning" style="margin-top: 0em !important"><b>Note: </b> We are still actively compiling our inventory.  The list will be final on September 1st.</p>
    <div class="clear"></div> 
    <div class="heading">
        <h1>Browse our Inventory:</h1>
        <a class="btn btn--primary" href="/sale/all/">View All Plants&nbsp; 
            <span class="count">&nbsp;({{ inventory_plants.size }})</span>
        </a>
    </div>
    <div class="clear"></div>
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
                    <a href="/sale/vines/">Vines</a> 
                </div>
                <div class="row">
                    <a href="/sale/succulents/">Succulents</a>
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
                <div class="row">
                    <a href="/sale/deerresistant/">
                    Deer Resistant
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
<div class="faq-block">
    <h2>Frequently Asked Questions</h2>
    <div>
        <b>I'm interested! How do I sign up?</b>
        <p>
            Check back here on September 1st! You will be able to sign up for a shopping slot on Saturday. Sunday will be a regular shopping day - no sign ups necessary. 
        </p>
    </div>
    <div>
        <b>I might want to shop for longer than 30-minutes. Should I reserve multiple time slots?</b>
        <p>
        No need to! Just sign up for one time slot and extend your visit as needed.  
        </p>
    </div>
    <div>
        <b>What payment methods are accepted?</b>
        <p>
            Cash and check are always 👍. However, we do also take credit - thank you!
        </p>
    </div>
    <div style="display:none">
        <b>I'm having trouble signing up using Sign Up Genius.</b>
        <p>
        Send us an email with your name and preferred time slot. We will sign you up and send you an email confirmation.
        </p>
    </div>
    <div>
        <b>Why should I sign up to shop?</b>
        <p>
            Sign ups are only required on Saturday.  We recommend doing so if: 
            <br/>&#9702; You plan on showing up with a list! Some species are popular and we do run out.
            <br/>&#9702; You want to go but the extra motivation of signing up will help. (We've all been there 😉) 
        </p>
    </div>
</div>

<div class="thanks-block" style="display:none">
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

