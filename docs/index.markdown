---
layout: default
description: "ENTER HERE"
---
<html>
<head>
<style>
h1 {text-align: center;}
p {text-align: center;}
div {text-align: center;}
</style>
</head>
<body>

<h1>Photo Sets</h1>
<ul>
  {% comment %}
    Get all "photo_set" pages and display a list with links to them.
  {% endcomment %}
  {% assign photo_pages = site.pages | where: "layout", "photo_set" %}
  {% for photo_page in photo_pages %}
    <li>
      <a href="{{ photo_page.url | prepend: site.baseurl }}">{{ photo_page.title }}</a>
    </li>
  {% endfor %}
</ul>