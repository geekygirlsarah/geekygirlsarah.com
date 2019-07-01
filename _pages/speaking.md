---
title: "Speaking"
layout: splash
author: sarah
permalink: /speaking/
date: 2019-05-19T12:00:00-04:00
classes: 
  - wide
  - landing
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: assets/images/splash_bg_minkwic_2015.jpg
---

Over the years, I've given over 55 presentations that range from workshops to keynote presentations. I've also spoken 
locally, regionally, nationally, and internationally. If you’re interested in having me speak, please reach out! Send 
me a message on my [Contact](/contact/) page.

Jump to section: 
[Upcoming Events](#upcoming-events){: .btn .btn--inverse .btn--large }
[About My Talks](#about-my-talks){: .btn .btn--inverse .btn--large }
[My Talks](#my-talks){: .btn .btn--inverse .btn--large }
[Past Events](#past-events){: .btn .btn--inverse .btn--large }
{: .notice--primary.text-center}

## Upcoming Events

{% assign today = "now" | date: "%Y-%m-%d" %}

| Date | Event | Location | Talk Type | Talk Title | 
|------|-------|----------|-----------|------------|
{% for item in site.data.conftalks %}{% assign event_date = item.date | date: "%Y-%m-%d" %}{% if event_date >= today %}{% if item.date == item.end_date %}{{ item.date | date_to_xmlschema | date_to_string: "ordinal", "US" }}{% else %}{{ item.date | date_to_xmlschema | date_to_string: "ordinal", "US" }} - {{ item.end_date | date_to_xmlschema | date_to_string: "ordinal", "US" }}{% endif %} | {% if item.event_url %}<a href="{{ item.event_url}}" target="_blank">{{ item.event }}</a>{% else %}{{ item.event }}{% endif %} | {{ item.location }} | {{ item.type }} | {% if item.talk_url %}<a href="{{ item.talk_url}}">{{ item.title }}</a>{% else %}{{ item.title }}{% endif %}
{% endif %}{% endfor %}

## About My Talks

I really love speaking about the intersection of where tech and people come together. As a polyglot (multiple-language) 
software engineer, I've worked in a variety of tech stacks and fields and I have a wide range of interests. My talks 
often reflect this and I bring a different perspective to many topics in the field, both technically and professionally.

If you see a talk that interests you, or would like to discuss maybe creating a talk or discussing something 
specifically for your event, please reach out to me. I'd love to chat more about it. Drop me a line on my 
[Contact](/contact/) page.

## My Talks

Here's a list of my talks I've given.

**Keynote-Worthy Talks**
- [Building an Open Source Artificial Pancreas](/speaking/building-an-open-source-artificial-pancreas/)
- [Doors](/speaking/doors/)
- [The Power of Secrets](/speaking/the-power-of-secrets/)

**Technical Talks**
- [A Primer on Functional Programming](/speaking/a-primer-on-functional-programming/)
- [Building an Open Source Artificial Pancreas](/speaking/building-an-open-source-artificial-pancreas/)
- [“Hey Mycroft”: Getting Started with the Open Source Home Assistant](/speaking/hey-mycroft-getting-started-with-the-open-source-home-assistant/)
- [Intro to Hacking with the Raspberry Pi](/speaking/intro-to-hacking-with-the-raspberry-pi/)
    
**Professional Skills/Human Skills Talks**
- [Building an Open Source Artificial Pancreas](/speaking/building-an-open-source-artificial-pancreas/)
- [Building Your Team to Last: Successful Onboarding and Mentoring Practices](/speaking/building-your-team-to-last/)
- [Doors](/speaking/doors/)
- Life as a Midwestern Developer
- [Maintaining Your Mental and Emotional Health While Job Hunting](/speaking/maintaining-your-mental-and-emotional-health-while-job-hunting/)
- [The Power of Secrets](/speaking/the-power-of-secrets/)
- [Pursuing a Passion Project: Struggles and Successes]()


## Past Events

| Date | Event | Location | Talk Type | Talk Title | 
|------|-------|----------|-----------|------------|
{% for item in site.data.conftalks reversed %}{% assign event_date = item.date | date: "%Y-%m-%d" %}{% if event_date < today %}{% if item.date == item.end_date %}{{ item.date | date_to_xmlschema | date_to_string: "ordinal", "US" }}{% else %}{{ item.date | date_to_xmlschema | date_to_string: "ordinal", "US" }} - {{ item.end_date | date_to_xmlschema | date_to_string: "ordinal", "US" }}{% endif %} | {% if item.event_url %}<a href="{{ item.event_url}}" target="_blank">{{ item.event }}</a>{% else %}{{ item.event }}{% endif %} | {{ item.location }} | {{ item.type }} | {% if item.talk_url %}<a href="{{ item.talk_url}}">{{ item.title }}</a>{% else %}{{ item.title }}{% endif %}
{% endif %}{% endfor %}
