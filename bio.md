---
title: Bio
headline: Bio
permalink: /bio/
menu: main
---
<div class="bio--content">
  <img
    src="{{site.baseurl}}/assets/images/resume/josh-bio.jpg"
    srcset="{{site.baseurl}}/assets/images/resume/josh-bio.jpg 1x,
      {{site.baseurl}}/assets/images/resume/josh-bio2x.jpg 2x"
    alt="{{page.title}}" />
  <p>By day, I help develop large scale web applications for <a href="{{site.work_link}}">{{site.work_org}}</a> in Brookline, MA. My goal is to build simple, yet blazingly fast websites using modern technologies.</p>

  <p>I have mentored Front End Web Development and Modern Web Design students at <a href="http://thinkful/com">Thinkful</a>. I helped them establish new careers in web design and/or modernize their current skill-sets. It is a rewarding experience, and it helps me to stay current in this fast paced industry.</p>

  <p><strong>I am currently available for freelance design and front end development work</strong>. <a href="mailto:{{site.email}}">Contact me today</a> to discuss your project.</p>

</div>

<div class="resume--items">
  {% for job in site.data.jobs %}
    <div class="card">
      <div class="resume--content">
        <h2>{{job.job_title}}</h2>
        <p>

          <img

          {% if job.employer == "America's Test Kitchen" %}
              src="{{site.baseurl}}/assets/images/resume/1x/{{job.image}}.png"
              srcset="{{site.baseurl}}/assets/images/resume/1x/{{job.image}}.png 1x,
              {{site.baseurl}}/assets/images/resume/2x/{{job.image}}.png 2x"
            {%else%}
              src="{{site.baseurl}}/assets/images/resume/1x/{{job.image}}.jpg"
              srcset="{{site.baseurl}}/assets/images/resume/1x/{{job.image}}.jpg 1x,
                {{site.baseurl}}/assets/images/resume/2x/{{job.image}}.jpg 2x"
          {%endif%}

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
</div>
