---
title: Resume
headline: Résumé
permalink: /resume/
---

<section class="resume--items">
  {% for job in site.data.jobs %}
    <div class="card">
      <div class="resume--logo">
        <img src="{{site.baseurl}}/assets/images/resume/{{job.image}}.png" alt="{{job.employer}} Logo">
      </div>
      <div class="resume--content">
        <h2><strong>{{job.job_title}}</strong></h2>
        <strong>{{job.employer}}</strong><br>
        {{job.website}}<br>
        {{job.dates}}
        <ul>{{job.job_description}}</ul>
      </div>
    </div> 
  {% endfor %}
</section>
