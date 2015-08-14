---
title: Kudos
headline: Kudos
permalink: /kudos/
---
<div class="testimonials">
  {% for testimonial in site.data.testimonials %}
    <div class="card">
      <img src="{{site.baseurl}}/assets/images/testimonials/{{testimonial.image}}.jpg" alt="">
      <p>
        <q>{{testimonial.testimonial}}</q>
        <cite><strong>{{testimonial.name}}, {{testimonial.title}}</strong></cite>
      </p> 
    </div> 
  {% endfor %}
</div>