---
title: Portfolio
headline: Portfolio
permalink: /portfolio/
menu: main
---
<div class="portfolio--teasers">
  {% for portfolio_item in site.portfolio_items %}
    <div class="card">
      <a href="{{portfolio_item.url | prepend: site.baseurl}} ">        
        <img
            src="{{site.baseurl}}/assets/images/portfolio/desktop/1x/{{portfolio_item.image}}.jpg"
            srcset="{{site.baseurl}}/assets/images/portfolio/desktop/1x/{{portfolio_item.image}}.jpg 1x,
                {{site.baseurl}}/assets/images/portfolio/desktop/2x/{{portfolio_item.image}}2x.jpg 2x"
            class="img-responsive"
            alt="{{portfolio_item.title}}" />
        <p>
          {{portfolio_item.title}}
        </p> 
      </a>
    </div>
  {% endfor %}
</div>
