---
title: Portfolio
headline: Portfolio
permalink: /portfolio/
---
<div class="portfolio--teasers">
  {% for portfolio_item in site.portfolio_items %}
    <article class="card">
      <a href="{{portfolio_item.url | prepend: site.baseurl}} ">
        <img src="{{site.baseurl}}/assets/images/portfolio/{{portfolio_item.image}}.png" alt="{{portfolio_item.title}}" class="img-responsive">
        <p>
          {{portfolio_item.title}}
        </p> 
      </a>
    </article>
  {% endfor %}
</div>
