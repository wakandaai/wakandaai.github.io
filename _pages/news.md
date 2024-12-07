---
title: "News"
layout: textlay
sitemap: false
permalink: /news.html
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
## News

{% if site.data.news %}
<div class="jumbotron">
{% for article in site.data.news %}
<b>{{ article.date }}</b>

{{ article.headline }}
{% endfor %}

</div>

{% else %}
<div class="jumbotron">
  We will share our updates with you very soon...
</div>
{% endif %}