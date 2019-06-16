---
title: "Speaking"
layout: splash
author: sarah
permalink: /speaking/
date: 2019-05-19T12:00:00-04:00
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: assets/images/splash_bg_minkwic_2015.jpg
#   actions:
#     - label: "Download"
#       url: "https://github.com/mmistakes/minimal-mistakes/"
#   caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
---

Sarah has given various presentations and talks. If you’re interested in having her speak, please send a message on the Contact page.

## Upcoming Speaking Events

{% assign today = "now" | date: "%Y-%m-%d" %}

| Date | Event | Location | Talk Type | Talk Title | 
|------|-------|----------|-----------|------------|
{% for item in site.data.conftalks %}{% assign event_date = item.date | date: "%Y-%m-%d" %}{% if event_date >= today %}{% if item.date == item.end_date %}{{ item.date | date_to_xmlschema | date_to_string: "ordinal", "US" }}{% else %}{{ item.date | date_to_xmlschema | date_to_string: "ordinal", "US" }} - {{ item.end_date | date_to_xmlschema | date_to_string: "ordinal", "US" }}{% endif %} | {{ item.event }} | {{ item.location }} | {{ item.type }} | {{ item.title }}
{% endif %}{% endfor %}

## Past Speaking Events

| Date | Event | Location | Talk Type | Talk Title | 
|------|-------|----------|-----------|------------|
{% for item in site.data.conftalks reversed %}{% assign event_date = item.date | date: "%Y-%m-%d" %}{% if event_date < today %}{% if item.date == item.end_date %}{{ item.date | date_to_xmlschema | date_to_string: "ordinal", "US" }}{% else %}{{ item.date | date_to_xmlschema | date_to_string: "ordinal", "US" }} - {{ item.end_date | date_to_xmlschema | date_to_string: "ordinal", "US" }}{% endif %} | {{ item.event }} | {{ item.location }} | {{ item.type }} | {{ item.title }}
{% endif %}{% endfor %}
