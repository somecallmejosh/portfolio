---
title: Resume
headline: Résumé
permalink: /resume/
---
<section class="resume--items">
  {% for job in site.data.jobs %}
    <div class="card">
      <div class="resume--content">
        <h2>{{job.job_title}}</h2>
        <p>
          <img
              srcset="{{site.baseurl}}/assets/images/resume/1x/{{job.image}}.jpg 1x,
                  {{site.baseurl}}/assets/images/resume/2x/{{job.image}}.jpg  2x"
              src="{{site.baseurl}}/assets/images/resume/1x/{{job.image}}.jpg .jpg"
              alt="{{job.employer}} Logo" />
          {% if job.website %}
            <a href="{{job.website}}">{{job.employer}}</a>
            {% else %}
             <span>{{job.employer}}</span>
          {% endif %}
        </p>
        <p>{{job.dates}}</p>
        <ul>{{job.job_description}}</ul>
      </div>
    </div> 
  {% endfor %}
</section>
