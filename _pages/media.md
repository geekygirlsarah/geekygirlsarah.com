---
title: "Media and Press"
layout: splash
permalink: /media/
date: 2019-06-30T21:52:00-04:00
header:
  overlay_color: "#000"
  overlay_filter: "0.2"
  overlay_image: assets/images/splash_bg_robotteam_2013-2.jpg
  caption: "The second competition robot I helped program and build in 2013"
---

I have been in a variety of podcasts, articles, blog posts, and videos. Here’s a list of several of them.

Jump to section: 
[Podcasts](#podcasts){: .btn .btn--inverse .btn--large }
[Articles or Blog Posts](#articles-or-blog-posts){: .btn .btn--inverse .btn--large }
[Videos](#videos){: .btn .btn--inverse .btn--large }
{: .notice--primary.text-center}

## Podcasts

<img style="float: right;" src="/assets/images/hallway-chats-podcast-screenshot.jpg" width="300" height="199" alt="Screenshot of Sarah recording a podcast on Hallway Chats">
{% for item in site.data.podcasts reversed %}
- [{{ item.show }}]({{ item.url }}) {{ item.episode }} - {{ item.date | date_to_xmlschema | date_to_string: "ordinal", "US" }}{% endfor %}

## Articles or Blog Posts:

<img style="float: right;" src="/assets/images/the-new-stack-ilooklikeanengineer.jpg" width="300" height="819" alt="Screenshot of The New Stack's article on #ILookLikeAnEngineer featuring Sarah's tweet picture at the top">

{% for item in site.data.articles reversed %}
- [{{ item.title }}]({{ item.url }}) - {{ item.source }}, {{ item.date | date_to_xmlschema | date_to_string: "ordinal", "US" }}{% endfor %}

## Videos

<img style="float: right;" src="/assets/images/google-year-in-review-2015-screenshot.jpg" width="250" height="400" alt="Screenshot of the Google 2015 Year in Search video on Youtube with 15 women holding #ILookLikeAnEngineer signs, including Sarah">
{% for item in site.data.videos reversed %}
- [{{ item.title }}]({{ item.url }}) - {{ item.source }}, {{ item.date | date_to_xmlschema | date_to_string: "ordinal", "US" }}{% endfor %}
