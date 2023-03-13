---
permalink: /sale/
layout: splash
# tried to inherit from sale layout which inherited from splash layout but splash layout was called first? resulting in blanks where sale defined variables

banner:
    excerpt: Spring sale pages are currently under development. Please do not share publicly.

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
    excerpt: "Please park at Freshwater Farms Reserve and follow the signs to the nursery. Sign Up Genius is required for Saturday shopping due to parking lot limitations."
    #url: "/test"
    #btn_label: "Parking Information"
    #btn_class: "btn--info"
  - image_path: /assets/images/plants.jpg
    alt: "Volunteer"
    title: "Volunteer"
    excerpt: "Our sale is a fully volunteer-run event and we would love for you to help out. See our <a href='/volunteer/#sale'>Volunteer page</a> for more information."
    #url: "/volunteer"
    #btn_label: "Join Our Team"
    #btn_class: "btn--info"
  - image_path: /assets/images/starts.jpg
    alt: "Inventory"
    title: "Participating Nurseries & Vendors"
    excerpt: "Proudly partnering with Samara Restoration, Mattole Restoration Council, Lost Foods, Bob Vogt, Beresford's Bulbs and Brant's Plants."
    #url: "/category/cnps-2022-fall"
    #url: "/category/cnps-master-inventory"
    #btn_label: "More Information"
    #btn_class: "btn--primary"
---
<div class="hours">
    <h4>Saturday May 6, Open 9:00 am - 5:00 pm.*</h4>
    <h4>Sunday May 7, Open 9:00am - 4:00 pm.</h4>
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
            Browse by Type
            <ul>
                <li>
                    <a href="/sale/shrubs/">Shrubs</a>
                </li>
                <li>
                    <a href="/sale/perennials/">Perennials</a>
                </li>
                <li>
                    <a href="/sale/annuals/">Annuals</a>
                </li>
                <li><a href="/sale/vines/">Vines</a></li>
                <li><a href="/sale/trees/">Trees</a></li>
                <li><a href="/sale/ferns/">Ferns</a></li>
                <li><a href="/sale/grasses/">Grasses</a></li>
            </ul>
        </div>
        <div class="inventory_category box">
            Browse by Category
            <ul>
                <li>Hedges</li>
                <li>Groundcovers</li>
                <li>Beginner-Friendly</li>
                <li>Wildlife-Friendly</li>
                <li>Habitat</li>
                <li>Edible</li>
            </ul>
        </div>
        <div class="clear"></div>
    </div>
</div>
{% include feature_row %}

<div class="thanks-block" style="display:none">
    <h1>Thank You</h1>
    <div style="display:none">
    <p>We want to send huge thank yous to everyone who supports us in some way.</p>
    <p>Thank you to those of you who shop our sales. From those of you rewilding entire yards, to those of you tending small native plants on your balcony, we appreciate you eco-warriors! We all do what we can and every little bit helps.</p>
    <p>We appreciate the nurseries and vendors that we partner with and the community of sharing and support you offer us. We feel so lucky to be working alongside you.</p>
    <p>Thank you to nursery managers Chris and Barbara for your tireless efforts and countless hours of hard work. We couldn't ask for more dedicated leaders.</p>
    <p>Thank you to all our nursery volunteers. Whether you have volunteered for one hour or many more, we appreciate you! This has been a particularly long winter but seeing everyone show up, ready to work in the cold mornings warms our hearts: 
    Alice, Andrea, Anita, Barbara, Bobby, Brian, Callie, Carol, Charlie, Chris, Christine, Dino, Emily, Hannah, Kate, Kellie, Kevin, Jessi, Jessica, June, Matt, Marcia, Rebecca, Sam, Sharon, Steph, Steve, Trey, Victoria
    </p>
    </div>
</div>
