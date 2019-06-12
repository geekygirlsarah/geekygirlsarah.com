---
title: "What I'm Doing Now"
layout: splash
author: sarah
permalink: /now/
date: 2019-05-19T12:00:00-04:00
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/code-mash-lightning-talk.jpg
#   actions:
#     - label: "Download"
#       url: "https://github.com/mmistakes/minimal-mistakes/"
#   caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
---

Everything you’ve wanted to know about Sarah and what’s happening right now!

Quick link:  sarahwithee.com/now

(This list current as of {{ site.data.now.updated | date_to_xmlschema | date_to_string: "ordinal", "US"}}.)

## Now

{% for item in site.data.now.now %}
- {{ item.text }}{% endfor %}

## Near Future

{% for item in site.data.now.near_future %}
- {{ item.text }}{% endfor %}

## Availability

{% for item in site.data.now.availability %}
- {{ item.text }}{% endfor %}


_Thank you to Derek Sivers for the idea of making a /now page._
