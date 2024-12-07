---
title: "Talks"
layout: gridlay
sitemap: false
permalink: /talks/
---

<style>
.btn{
    margin-bottom:5px;
    padding-top:1px;
    padding-bottom:1px;
    padding-left:15px;
    padding-right:15px;
}
.jumbotron{
    padding:3%;
    padding-bottom:10px;
    padding-top:10px;
    margin-top:10px;
    margin-bottom:30px;
}
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

<div class="jumbotron">
### Invited Talks
{% assign invited_talks = site.data.publications | where: "type", "incollection" | where_exp: "item", "item.keywords contains 'invited'" %}
{% if invited_talks.size > 0 %}
  {% bibliography --query @incollection[keywords ^= invited] %}
{% else %}
  <p>Coming soon!</p>
{% endif %}
</div>

<div class="jumbotron">
### Regular Talks
{% assign regular_talks = site.data.publications | where: "type", "incollection" | where_exp: "item", "item.keywords contains 'invited' == false" %}
{% if regular_talks.size > 0 %}
  {% bibliography --query @incollection[keywords != invited] %}
{% else %}
  <p>Coming soon!</p>
{% endif %}
</div>
