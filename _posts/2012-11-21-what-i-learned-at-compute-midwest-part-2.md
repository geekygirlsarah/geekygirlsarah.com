---
title: What I Learned at Compute Midwest (Part 2)
date: 2012-11-21T14:35:56+00:00
permalink: /2012/11/21/what-i-learned-at-compute-midwest-part-2/
# canonical_url: "https://yoursite.com/custom-canonical-url"
categories:
  - Conferences
  - Hackathons
  - Uncategorized
tags:
  - Abbey T
  - Android
  - computemw
  - conferences
  - hackathon
---

This post was originally from the blog site Binary Girls that my friends Abbey, Sarah, and I started. I’m saving it here for archival reasons.
{: .notice--info} 

<a href="http://www.computemidwest.com/" target="_blank" rel="noopener noreferrer"><u><span style="color: #0066cc;">Compute Midwest</span></u></a>,<img class="alignright size-full wp-image-285" src="/assets/images/CMW_logo-150x150.png" alt="Compute Midwest logo" width="150" height="150" /> a regional conference focusing on new ideas in technology, was two weekends ago. In this post, I want to talk about the other half of the conference, the hackathon.

This hackathon was also a 24-hour competition where you develop a fully working mobile app or website from scratch. <!--more-->Nothing pre-built was allowed (except third-party APIs and any sort of paper-based design plans). Abbey and I teamed up again. Unfortunately, Kevin and Sarah couldn&#8217;t make this one. We developed an app called 

<a title="Projects" href="http://www.binarygirls.com/projects/" target="_blank" rel="noopener noreferrer"><u><span style="color: #0066cc;">Alpha Scram</span></u></a> for Android. While the app seemed a hit among some, it had some problems and we definitely learned from the experience.

We had a very great idea, but when we learned our team was cut in half, we debated whether we still could pull it off. We determined that we probably couldn&#8217;t, and so we came up with another idea. The original word game idea was Abbey&#8217;s, and after talking it through and ironing out the game play, we had something feasible to develop in the allotted time. She is a Java developer at her company, and I own two Android devices, so it only made sense for us to make an Android app this time (where we made an iPhone game last time). Truthfully, neither of us had developed for Android before, so we had a learning curve. We had discovered <a href="https://www.jetbrains.com/idea/" target="_blank" rel="noopener noreferrer"><u><span style="color: #0066cc;">IntelliJ</span></u></a>, which had some cooler built-in features for Android development than Eclipse did, so we used that. We both made most of the images for our last game, but I volunteered to make them for this one. And so from there we got started.

[<img class="alignright wp-image-291 size-medium" src="/assets/images/Screenshot_2012-11-10-23-21-38-180x300.png" alt="Alpha Scram screenshot" width="180" height="300" />](http://www.binarygirls.com/wp-content/uploads/2012/11/Screenshot_2012-11-10-23-21-38.png)I&#8217;m a horrible designer. I can sort of make my way through <a href="http://www.gimp.org/" target="_blank" rel="noopener noreferrer"><u><span style="color: #0066cc;">GIMP</span></u></a> but am no professional by any means. (If there&#8217;s some status below &#8220;amateur,&#8221; I&#8217;m probably that.)  But the great thing about a game with an educational theme to it is that if you make your drawings that look like chalkboards with chalk, then you can be as sloppy as you want! And so I made some preliminary images to get us started, and some changes later after our game&#8217;s look changed a bit.

Abbey started coding most of the basics of it while I was trying to design the GUI. It reminded me a lot of doing stuff for Visual Basic, one of the first PC-based languages I learned. While the drag and drop tools in IntelliJ are similar to VB, several things are different. First, Android isn&#8217;t based on pixels but a depth percentage. It&#8217;s an interesting concept that resizes your elements to fit any size screen, where pixels are specific to a screen size. Once I figured out how that worked, it became a bit easier. Also, elements by default seemed to be based on their positions to other elements and not on the screen itself, which also was a bit different. I figured it out, and soon had a nice looking layout. Abbey coded up the buttons, and then we could make words! A random letter generator came, and we had some random consonants that showed up. She got the timer working, and we had a working game!

Of course the big problem with a game that you have to make words with is how do you know it&#8217;s a word? &#8220;DFJG&#8221; shouldn&#8217;t earn you any points but it did. So I spent a while trying to figure out how to use Android&#8217;s spell checker. After a good 30 minutes of trying to figure it out, I gave up and just made a SQLite database with several word lists merged together. Our 150KB game turned into a 3.5MB game, but hey, we only have 24 hours to get it working! We could fix that later.

We added in some help screens, a stats screen, and we had a game. Except it crashed on my phone every time it started. Oops. I took over and started debugging it, and with Abbey checking syntax for things on her computer and me stepping through code and debugging, we got a 100% working app with 37 minutes to spare!

So there were some things I got out of this competition:

  * First, have a plan. We went in with some ideas of what we wanted to do, but nothing solidified. We debated working with another team but didn&#8217;t end up pursuing it. We really needed a better game plan going into it.
  * We both had some knowledge of what we were developing in. While Abbey knew enough Java to quickly figure out the code, the structure of the Android packages were different enough that both of us were scratching our heads at different points. We probably should have learned it better before going in, or at least looked up the packages we needed ahead of time so we didn&#8217;t spend as long learning and spent more time working on the app.
  * We didn&#8217;t use any of the sponsored APIs. While we won a prize last time despite not using any, it really hurts our changes considerably of winning anything. Like 2 prizes without and up to about a dozen with.
  * Along similar lines, our app was very similar to our last one. While the game play was quite different, there were a lot of the same elements to it, so that probably hurt our chances of winning too. Android was also different than iPhone, but developing the same game for a different system isn&#8217;t really original.
  * I was nervous about joining another team. I know Abbey&#8217;s, Sarah&#8217;s, and Kevin&#8217;s skills now, but if I joined another team, they wouldn&#8217;t know mine or I theirs. So that would be harder. I think what worries me a bit more is that i&#8217;m still a student and not as well-versed on the newer languages (Ruby/Rails, Python, HTML5, etc.) nor am I a good designer (I&#8217;m super jealous of how some of those apps looked!). So if I could find a team that could use the skills I do know, that&#8217;d be perfect, but there&#8217;s a bit of uncertainty to it.
  * Have fun. I did, even without the win. And I learned the basics of Android development. While I would have to brush up on more Java and learn the package structure to be able to write my own app from scratch, I got a good learning experience with my good friend Abbey.

What&#8217;s the future of the app? Well, we&#8217;re meeting this week to fix some of the bugs, and hopefully implement some more stable fixes to the app than what we hacked together that weekend, but we hope to post it to the Google Play store in maybe a few weeks or so. You can always check the status of it at our Project Page.

And finally, what about that idea we had in the first place? The four of us have already talked and we&#8217;re doing it at the next hackathon. I have a very HIGH confidence it could win at least one prize. It will take a ton of planning, a lot of learning some stuff ahead of time, but we&#8217;re sure we can get it up and going in 24 hours. And if we can find a designer, we&#8217;re sure it will look amazing too!

Have you been involved in any competitions like this? What are some of the things you&#8217;ve learned? Any suggestions on what we could do better next time?