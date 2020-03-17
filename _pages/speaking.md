---
title: "Speaking"
layout: splash
permalink: /speaking/
date: 2019-06-30T21:39:00-04:00
classes: 
  - wide
  - landing
header:
  overlay_color: "#000"
  overlay_filter: "0.2"
  overlay_image: /assets/images/splash_bg_minkwic_2015.jpg
  caption: "Speaking at MINK WIC 2015, which I also helped organize"
---

{% assign today = "now" | date: "%Y-%m-%d" %}

Over the years, I've given over 60 presentations that range from workshops to keynote presentations. I've also spoken 
locally, regionally, nationally, and internationally. 

In 2020, I am only speaking at conferences I am invited to, and I am submitting to my top 5 favorite conferences. 
However, if you’re interested in having me speak, please reach out anyway! Drop me a message on my 
[Contact](/contact/) page.

Jump to section: 
[Upcoming Events](#upcoming-events){: .btn .btn--inverse .btn--large }
[Why I Speak](#why-i-speak){: .btn .btn--inverse .btn--large }
[My Talks](#my-talks){: .btn .btn--inverse .btn--large }
[Past Events](#past-events){: .btn .btn--inverse .btn--large }
{: .notice--primary.text-center}

## Upcoming Events

All upcoming talks, workshops, and travel have been canceled due to the Coronavirus. 

## Why I Speak

I really love speaking about the intersection of where tech and people come together. As a polyglot (multiple-language) 
software engineer, I've worked in a variety of tech stacks and areas and I have a wide range of interests. My talks 
often reflect this and I bring a different perspective to many topics in the field, both technically and professionally.

I've also learned that as people get more experienced in their field, they tend to lose the ability to talk about what 
they work on and what they know, especially to newer people. Giving talks helps keep that communication 
skill growing so that I not only know what I'm talking about, but I can relate it to other technical and non-technical 
people alike.

If you see a talk that interests you, would like to discuss creating a talk, or want to discus something specifically 
for your event, please reach out to me. I'd love to chat more about it. Drop me a line on my [Contact](/contact/) page.

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

**Workshops**
- [“What is a HashTrieStackFilter?” A Data Structures & Algorithms Refresher For Everyone](/speaking/wtf-is-a-hashtriestackfiltermap/)


## Past Events

| Date | Event, Location | Talk Type | Talk Title | 
|------|-----------------|-----------|------------|
{% for item in site.data.conftalks reversed %}{% assign date = item.talk_date | date: "%Y-%m-%d" %}{% if date < today %}{% if item.event_start_date == item.event_end_date %}{{ item.event_start_date | date_to_xmlschema | date_to_string: "ordinal", "US" }}{% else %}{{ item.event_start_date | date_to_xmlschema | date_to_string: "ordinal", "US" }} - {{ item.event_end_date | date_to_xmlschema | date_to_string: "ordinal", "US" }}{% endif %} | {% if item.event_url %}<a href="{{ item.event_url}}" target="_blank" rel="noopener">{{ item.event_name }}</a>{% else %}{{ item.event_name }}{% endif %}, {{ item.event_location }} | {{ item.talk_type }} | {% if item.talk_url %}<a href="{{ item.talk_url}}">{{ item.talk_title }}</a>{% else %}{{ item.talk_title }}{% endif %}
{% endif %}{% endfor %}
