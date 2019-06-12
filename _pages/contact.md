---
title: "Contact"
layout: splash
author: sarah
permalink: /contact/
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

I want to hear from you! Whether it's feedback on something I worked on, wanting 
to collaborate on a project, or speaking at an event, I'd love for you to reach out.

I'm most easily accessible on Twitter [@geekygirlsarah](https://twitter.com/geekygirlsarah).

You're welcome to send me an email with the form below and I'll try to get back 
with you as soon as possible.


<form name="contact" method="post" data-netlify="true" netlify-honeypot="captcha">
  <p>
    <label>Your name*: <input type="text" name="name" required=""/></label>   
  </p>
  <p>
    <label>Your email*: <input type="email" name="email" required="" /></label>
  </p>
  <p>
    <label>Your phone: <input type="tel" name="phone" /></label>
  </p>
  <p class="hidden">
    <label>Don’t fill this out if you're human: <input name="captcha" /></label>
  </p>
  <p>
    <label>Why are you reaching out?: <select name="reason" >
      <option value="job">Talk about a job</option>
      <option value="speaking">Conference/event speaking request</option>
      <option value="podcast">Podcast guest request</option>
      <option value="website">Website issue</option>
      <option value="hey">Just reaching out</option>
      <option value="other">Something else</option>
    </select></label>
  </p>
  <p>
    <label>Subject: <input type="text" name="subject" /></label>   
  </p>
  <p>
    <label>Your message*: <textarea name="message" required=""></textarea></label>
  </p>
  <p>
    <button type="submit">Send</button>
  </p>
</form>
