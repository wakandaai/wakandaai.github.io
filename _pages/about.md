---
title: "About"
layout: gridlay
sitemap: false
permalink: /about/
---

<style>
img{
  border-radius: 10px;
}
.col-md-3 {
  margin-top:10px;
  margin-bottom:10px;
  padding:0px;
  display:block;
  overflow:hidden;
  text-align:center;
  display: table-cell;
  background: white;
  border-radius: 20px;
  height: auto;
}
iframe {
  margin:0;
  padding:0;
  width: 175px;
  display: inline;
  vertical-align: middle;
}
</style>

## About

{% for p in site.data.project %}

<div class="jumbotron">
<div class="row">
<div class="col-sm-4">
  <img src="{{ site.url }}{{ site.baseurl }}/images/{{ p.photo }}" width="100%" style="max-width:250px"/></br>
    <i>*AI-generated image</i>
</div>
<div class="col-sm-8 col-xs-12">
  <h3>{{ p.name }}</h3>
  <h4><i>{{ p.info }}</i></h4>
  {% if p.email %}<a href="mailto:{{ p.email }}" target="_blank"><i class="fa fa-envelope-square fa-3x"></i></a> {% endif %}
  {% if p.github %} <a href="{{ p.github }}" target="_blank"><i class="fa fa-github-square fa-3x"></i></a> {% endif %}
  <h4>Duration: {{ p.duration }}</h4>
</div>
</div>
</div>
{% endfor %}

{% if site.data.grants %}

<div class="jumbotron">
  <h4>Grants</h4>
  <ul>
    {% for grant in site.data.grants %}
      <li>{{ grant.name }} </li>
      {{ grant.description }}
      
    {% endfor %}
  </ul>
</div>
{% endif %}

{% if site.data.awards %}

<div class="jumbotron">
  <h3>Awards</h3>
  <ul>
    {% for award in site.data.awards %}
      <li>{{ award.name | replace: "-","&#8211;" }}</li>
    {% endfor %}
  </ul>
</div>
{% endif %}

{% if site.data.people %}

<div class="jumbotron">
  <h3>Students and Mentoring</h3>
  <ul>
    {% for student in site.data.people %}
      <li>{{ student.name }}, {{ student.location }} ({{ student.degree }}, {{ student.year }})</li>
    {% endfor %}
  </ul>
</div>
{% endif %}

<div class="jumbotron">
  <h4>Consortium</h4>
  <div style='display:block; text-align:center; margin-left:auto; margin-right:auto;'>
  {% for uni in site.data.consortium %}<a href="{{ uni.url }}" target="_blank"><img src='{{ site.url }}{{ site.baseurl }}/images/{{ uni.image }}' style='max-height: 80px; max-width: 200px; margin: 1%'/></a>{% endfor %}
  </div>
</div>

<div class="jumbotron">
<div class="row">
<div class="col-sm-4">
  <img src="{{ site.url }}{{ site.baseurl }}/images/afretec-impact.png" width="100%" style="max-width:250px"/>
</div>
<div class="col-sm-8 col-xs-12">
  <h4>About AFRETEC</h4>
The <a href="https://engineering.cmu.edu/afretec/index.html">African Engineering and Technology (AFRETEC) Network </a> is a pan-African collaboration of technology-focused universities from across the continent are working together to build engineering and technology capacity in Education, Knowledge Creation, and Entrepreneurship. The initiative is led by Carnegie Mellon University Africa and the network is in partnership with the Mastercard Foundation.
</div>
</div>
</div>

<div class="jumbotron">
  <h4>Sponsors</h4>
  <div style='display:block; text-align:center; margin-left:auto; margin-right:auto;'>
  {% for funder in site.data.funders %}<a href="{{ funder.url }}" target="_blank"><img src='{{ site.url }}{{ site.baseurl }}/images/{{ funder.image }}' style='max-height: 80px; max-width: 400px; margin: 1%'/></a>{% endfor %}
  </div>
</div>