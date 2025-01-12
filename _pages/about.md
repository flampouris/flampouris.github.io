---
title: "About"
layout: gridlay
sitemap: false
permalink: /about/
---

### **About**

{% for member in site.data.pi %}

<div class="jumbotron">
<div class="row">
<div class="col-sm-4">
  <img src="{{ site.url }}{{ site.baseurl }}/images/{{ member.photo }}" width="100%" style="max-width:250px"/>
</div>
<div class="col-sm-8 col-xs-12">
  <h3>{{ member.name }}</h3>
  <h4><i>{{ member.info }}</i></h4>
  {% if member.email %}<a href="mailto:{{ member.email }}" target="_blank"><i class="fa fa-envelope-square fa-3x"></i></a> {% endif %}
  {% if member.linkedin %} <a href="{{ site.url }}{{ site.baseurl }}/{{ member.linkedin }}" target="_blank"><i class="fa fa-linkedin-square fa-3x"></i></a> {% endif %}
  {% if member.cv %} <a href="{{ site.url }}{{ site.baseurl }}/{{ member.cv }}" target="_blank"><i class="ai ai-cv-square ai-3x"></i></a> {% endif %}
  {% if member.scholar %} <a href="{{ member.scholar }}" target="_blank"><i class="ai ai-google-scholar-square ai-3x"></i></a> {% endif %}
  {% if member.github %} <a href="{{ member.github }}" target="_blank"><i class="fa fa-github-square fa-3x"></i></a> {% endif %}
  {% if member.researchgate %} <a href="{{ member.researchgate }}" target="_blank"><i class="ai ai-researchgate-square ai-3x"></i></a> {% endif %}

  <ul style="overflow: hidden">
    {% for education in member.education %}
      <li>{{ education | replace: "-","&#8211;" }}</li>
    {% endfor %}
  </ul>

</div>
</div>
</div>
{% endfor %}

{% if site.data.positions %}

<div class="jumbotron">
  <h3>Professional Experience</h3>
  <ul>
    {% for position in site.data.positions %}
      <li>{{ position.title }}, {{ position.employer }} {{position.client}} ({{ position.location }}, {{ position.year }})</li>
    {% endfor %}
  </ul>
</div>
{% endif %}

{% if site.data.visitor %}

<div class="jumbotron">
  <h3>Visiting Positions</h3>
  <ul>
    {% for position in site.data.visitor %}
      <li>{{ position.title }}, <em> {{position.subject}} </em>, {{ position.host }}, {{position.location}} ({{ position.year }})</li>
    {% endfor %}
  </ul>
</div>
{% endif %}

{% if site.data.member %}

<div class="jumbotron">
  <h3>Membership</h3>
  <ul>
    {% for member in site.data.member %}
      <li>{{ member.name }}</li>
    {% endfor %}
  </ul>
</div>
{% endif %}

{% if site.data.reviewer %}

<div class="jumbotron">
  <h3>Reviewer</h3>
  <ul>
    {% for journal in site.data.reviewer %}
      <li>{{ journal.name }}</li>
    {% endfor %}
  </ul>
</div>
{% endif %}

<div class="jumbotron">
  <h3>Sponsors</h3>

  Over the years, my work has neem supported by several National and International Public, Non-Profit and Private Organizations.
  
  <div style='display:block; text-align:center; margin-left:auto; margin-right:auto;'>
  {% for funder in site.data.funders %}<a href="{{ funder.url }}" target="_blank"><img src='{{ site.url }}{{ site.baseurl }}/images/{{ funder.image }}' style='max-height: 80px; max-width: 200px; margin: 1%'/></a>{% endfor %}
  </div>
</div>

