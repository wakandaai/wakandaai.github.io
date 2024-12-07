---
title: "Software"
layout: gridlay
sitemap: false
permalink: /software/
---

<style>
img{
  border-radius: 10px;
}
iframe {
  width: 175px;
  display: inline;
  vertical-align:middle;
  <!-- margin-bottom:5px; -->
  <!-- margin-left:5px; -->
  <!-- border: 1px solid red; -->
}
.col-md-3 {
  margin:0;
  padding:0;
  margin-top:10px;
  margin-bottom:10px;
  display:block;
  overflow:hidden;
  text-align:center;
  display: table-cell;
  height: auto;
  float: none;
  background:white;
  border-radius:20px;
  <!-- border: 1px solid black; -->
}
</style>

## Software Packages

<div class="jumbotron">
<div class="row align-items-end">
<div class="col-md-12 col-sm-12">



{% if site.data.software %}
{% for s in site.data.software %}
  <h5>{{ s.name }}</h5>
  <ul style="list-style-type: none; margin: 0; padding: 0;">
      <li>
        <a href="{{ s.url }}" target="_blank"><button class="btn btn-success btn-sm">LINK</button></a>
        <a href="{{ site.url }}{{ site.baseurl }}/docs/data_docs.pdf" target="_blank"><button class="btn btn-danger btn-sm">PAPER</button></a> 
      </li>
      {% if s.authors %}
      <h6>Author(s):</h6>
      {% for auth in s.authors %}
      <ul style="overflow: hidden">
        <li> {{ auth }} </li>
      </ul>
      {% endfor %}
      {% endif %}
  </ul><br>
    {% endfor %}

{% else %}
<div class="jumbotron">
  Coming soon...
</div>
{% endif %}

</div>
</div>
</div>
