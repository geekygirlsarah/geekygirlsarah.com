---
title: "Blog"
layout: splash
author: sarah
permalink: /blog/
date: 2019-05-19T12:00:00-04:00
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: assets/images/splash_bg_codemash_2019.jpg
#   actions:
#     - label: "Download"
#       url: "https://github.com/mmistakes/minimal-mistakes/"
#   caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
---

Uh, something insightful goes here...

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a> ({{ post.date | date_to_xmlschema | date_to_string: "ordinal", "US" }})
    </li>
  {% endfor %}
</ul>