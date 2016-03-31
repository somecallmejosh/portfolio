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
  <p>By day, I help design and develop large scale web applications for <a href="{{site.work_link}}">{{site.work_org}}</a> in Collinsville, CT. We build fantasy sports games for the NFL, NASCAR, PGA, and many other professional sporting organizations. Have a look at my <a href="{{site.baseurl}}/portfolio">portfolio</a> for some of my most recent design and development projects.</p>

  <p>In the evenings and on weekends, I work as a Front End Web Developer and Modern Web Design Mentor at <a href="http://thinkful/com">Thinkful</a>. I work with students to help them establish new careers in web design and/or modernize their current skillsets. It's a rewarding job, and it helps me to stay current in this fast paced industry.</p>

  <p><strong>I am currently available for freelance design and front end development work</strong>. <a href="mailto:{{site.email}}">Contact me today</a> to discuss your project.</p>

</div>

<div class="resume--items">
  {% for job in site.data.jobs %}
    <div class="card">
      <div class="resume--content">
        <h2>{{job.job_title}}</h2>
        <p>
          <img
            src="{{site.baseurl}}/assets/images/resume/1x/{{job.image}}.jpg"
            srcset="{{site.baseurl}}/assets/images/resume/1x/{{job.image}}.jpg 1x,
              {{site.baseurl}}/assets/images/resume/2x/{{job.image}}.jpg 2x"
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
