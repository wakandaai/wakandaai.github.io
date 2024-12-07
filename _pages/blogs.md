---
title: "Blogs"
layout: page
sitemap: false
permalink: /blogs/
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

{% if site.posts.size !=0 %}
<ul>
  {% for post in site.posts %}
    <li>
      {{ post.date | date_to_string }}: <a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ post.title}}</a>
    </li>
  {% endfor %}
</ul>
{% else %}
<div class="jumbotron">
  We will share some of our reflections and discoveries with you very soon...
</div>

{% endif %}
