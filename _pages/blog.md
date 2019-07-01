---
title: "Blog"
layout: splash
permalink: /blog/
date: 2019-05-19T12:00:00-04:00
header:
  overlay_color: "#000"
  overlay_filter: "0.2"
  overlay_image: /assets/images/splash_bg_alterconf_2016.jpg
  caption: "Speaking at AlterConf Portland 2016 reading a quote on vulnerability by Brené Brown"
---

These are some of my assorted thoughts and writings from the last several years. Feel free to check them out!

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a> ({{ post.date | date_to_xmlschema | date_to_string: "ordinal", "US" }})
    </li>
  {% endfor %}
</ul>