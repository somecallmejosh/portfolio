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
        <h2>{{job.job_title}}</h2>
        <p>
          {% if job.website %}
            <a href="{{job.website}}">{{job.employer}}</a>
            {% else %}
            {{job.employer}}
          {% endif %}
        </p>
        <p>{{job.dates}}</p>
        <ul>{{job.job_description}}</ul>
      </div>
    </div> 
  {% endfor %}
</section>
