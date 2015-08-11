---
title: Kudos
headline: Kudos
permalink: /kudos/
---
<setcion class="testimonials">
  {% for testimonial in site.data.testimonials %}
    <article class="card">
    <img src="{{site.baseurl}}/assets/images/testimonials/{{testimonial.image}}.jpg" alt="">
    <p>
      <q>{{testimonial.testimonial}}</q>
      <cite><strong>{{testimonial.name}}, {{testimonial.title}}</strong></cite>
    </p> 
    </article> 
  {% endfor %}
</setcion>