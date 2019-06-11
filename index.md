---
title: "Sarah Withee"
layout: splash
author: sarah
permalink: /
date: 2019-05-19T12:00:00-04:00
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/code-mash-lightning-talk.jpg
#   actions:
#     - label: "Download"
#       url: "https://github.com/mmistakes/minimal-mistakes/"
#   caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
excerpt: "Polyglot software engineer. International tech speaker. Hardware and robot tinkerer. Conference organizer. User of  100% organic sarcasm & puns."
author_profile: true
intro: 
  - excerpt: 'Nullam suscipit et nam, tellus velit pellentesque at malesuada, enim eaque. Quis nulla, netus tempor in diam gravida tincidunt, *proin faucibus* voluptate felis id sollicitudin. Centered with `type="center"`'
feature_row:
  - image_path: assets/images/icons8-code-100.png
    alt: "Code icon"
    title: "Developing"
    excerpt: "I am a software engineer who is passionate about the intersection of tech and people."
    # url: "resume/"
    # btn_label: "Resume"
    # btn_class: "btn--primary"
  - image_path: /assets/images/icons8-lecturer-100.png
    alt: "Lecturer icon"
    title: "Speaking"
    excerpt: "I've given keynotes, technical talks, and powerful talks capable of making people laugh and cry at the same time."
    # url: "speaking/"
    # btn_label: "Speaking"
    # btn_class: "btn--primary"
  - image_path: assets/images/icons8-blog-100.png
    alt: "Blog icon"
    title: "Blogging"
    excerpt: "I write about projects I've worked on, as well as a variety of other technical and personal topics."
    # url: "blog/"
    # btn_label: "Read"
    # btn_class: "btn--primary"
# feature_block1:
#   # - image_path: assets/images/icons8-code-100.png
#     # alt: "Code icon"
#     title: "Upcoming Talks"
#     data_type: "talks"
#     number: 3
#     # sort_by: "upcoming"
#     url: "speaking/"
#     btn_label: "All Talk Schedule"
#     btn_class: "btn--primary"
# feature_block2:
#   # - image_path: /assets/images/icons8-lecturer-100.png
#     # alt: "Lecturer icon"
#     title: "Recent Podcasts"
#     data_type: "podcasts"
#     number: 3
#     # sort_by: "recent"
#     url: "media/"
#     btn_label: "All Media"
#     btn_class: "btn--primary"
# feature_block3:
#   # - image_path: assets/images/icons8-blog-100.png
#     # alt: "Blog icon"
#     title: "Recent Blog Posts"
#     data_type: "posts"
#     number: 3
#     # sort_by: "recent"
#     url: "blog/"
#     btn_label: "All Posts"
#     btn_class: "btn--primary"


---

<!-- {% include feature_row %} -->


<div class="home_feature_table">
    <div class="home_feature_table_row">
        <div class="home_feature_image_center">
            <img src="assets/images/icons8-code-100.png" alt="Code icon" />
        </div>
        <div class="home_feature_image_center">
            <img src="assets/images/icons8-lecturer-100.png" alt="Lecturer icon" />
        </div>
        <div class="home_feature_image_center">
            <img src="assets/images/icons8-blog-100.png" alt="Blog icon" />
        </div>
    </div>
    <div class="home_feature_table_row">
        <div class="home_feature_table_cell_third">
            <h2>Developing</h2>
            <p>I am a software engineer who is passionate about the intersection of tech and people.</p>
        </div>
        <div class="home_feature_table_cell_third">
            <h2>Speaking</h2>
            <p>I’ve given keynotes, technical talks, and powerful talks capable of making people laugh and cry at the same time.</p>
        </div>
        <div class="home_feature_table_cell_third">
            <h2>Blogging</h2>
            <p>I write about projects I’ve worked on, as well as a variety of other technical and personal topics.</p>
        </div>
    </div>
</div>




<div class="home_feature_table">
    <div class="home_feature_table_row">
        <div class="home_feature_table_cell_image">
            <img src="assets/images/icons8-code-100.png" alt="Code icon" />
        </div>
        <div class="home_feature_table_cell">
            <h2>Upcoming Talks</h2>
            {% include feature_block data_type="talks" show_number=3 %}
            <a href="speaking/" class="btn btn--primary">All Talk Schedule</a>
        </div>
    </div>
    <div class="home_feature_table_row">
        <div class="home_feature_table_cell_image">
            <img src="assets/images/icons8-lecturer-100.png" alt="Lecturer icon" />
        </div>
        <div class="home_feature_table_cell">
            <h2>Recent Podcasts</h2>
            {% include feature_block data_type="podcasts" show_number=2 %}
            <a href="speaking/" class="btn btn--primary">All Media</a>
        </div>
    </div>
    <div class="home_feature_table_row">
        <div class="home_feature_table_cell_image">
            <img src="assets/images/icons8-blog-100.png" alt="Blog icon" />
        </div>
        <div class="home_feature_table_cell">
            <h2>Recent Blog Posts</h2>
            {% include feature_block data_type="posts" show_number=2 %}
            <a href="speaking/" class="btn btn--primary">All Posts</a>
        </div>
    </div>
</div>

<style type="text/css">
    .home_feature_table
    {
        display: table;
        width: 100%;
    }
    .home_feature_table_title
    {
        display: table-caption;
        text-align: center;
        font-weight: bold;
        font-size: larger;
    }
    .home_feature_table_heading
    {
        display: table-row;
        font-weight: bold;
        text-align: center;
    }
    .home_feature_table_row
    {
        display: table-row;
    }
    .home_feature_table_cell
    {
        display: table-cell;
        border: none;
        /* border-width: thin; */
        padding-left: 5px;
        padding-right: 5px;
    }
    .home_feature_table_cell_third
    {
        display: table-cell;
        border: none;
        /* border-width: thin; */
        padding-left: 5px;
        padding-right: 20px;
        width: 33%
    }
    .home_feature_table_cell_image
    {
        display: table-cell;
        border: none;
        /* border-width: thin; */
        padding-left: 5px;
        padding-right: 5px;
        width: 125px;
    }
    .home_feature_image_center
    {
        margin-left: auto;
        margin-right: auto;
        display: table-cell;
        border: none;
        /* border-width: thin; */
        padding-left: 5px;
        padding-right: 5px;
    }
</style>
