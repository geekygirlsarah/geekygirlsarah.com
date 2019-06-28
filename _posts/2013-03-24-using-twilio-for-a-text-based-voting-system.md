---
id: 332
title: Using Twilio for a Text-Based Voting System
date: 2013-03-24T00:00:16+00:00
author: wordpress
layout: post
guid: http://sarahwithee.com/?p=332
permalink: /2013/03/24/using-twilio-for-a-text-based-voting-system/
categories:
  - Projects
  - School
  - Uncategorized
tags:
  - excitement
  - Mr. Engineer
  - MySQL
  - PHP
  - projects
  - SCE
  - school
  - texting
  - Twilio
  - UMKC
---
_This post was originally from the blog site Binary Girls that my friends Abbey, Sarah, and I started. I’m saving it here for archival reasons._

* * *

You know how on shows like American Idol and Dancing with the Stars you&#8217;re able to text who you want to vote for, and by the end of the show they already have the votes tabulated? Well, I built one of those about a month ago. Here&#8217;s a bit more of the story behind that.<!--more-->

<a href="http://www.eweek.org/" target="_blank" rel="noopener noreferrer"><u><span style="color: #0066cc;">National Engineers Week</span></u></a> is a week at the end of February to celebrate the contributions that engineers make to society. At <a href="http://www.umkc.edu" target="_blank" rel="noopener noreferrer"><u><span style="color: #0066cc;">UMKC</span></u></a>, the <a href="http://sce.umkc.edu/" target="_blank" rel="noopener noreferrer"><u><span style="color: #0066cc;">School of Computing and Engineering</span></u></a> (SCE) holds their own E-Week, and invite all of the SCE organizations to team up together and hold activities and events that all of the students can participate in. The <a href="http://www.swe.org" target="_blank" rel="noopener noreferrer"><u><span style="color: #0066cc;">Society of Women Engineers</span></u></a> chapter has held an event for the past three years called Mr. Engineer, a beauty pageant of sorts, but a lot nerdier. And with guys.

This year, the seven contestants were judged based on their nerdy wear, a trivia round, and a talent portion. The audience (about 100 people) also could vote on their favorite contestant. The problem with last year&#8217;s competition was that they used paper ballots, which are just awful to count manually, but also people were taking extras and cheating by giving extra votes to their friends.

At both hackathons I attended, they had a company called <a href="http://www.twilio.com" target="_blank" rel="noopener noreferrer"><u><span style="color: #0066cc;">Twilio</span></u></a> as one of the suggested APIs (Application Programming Interface). Twilio offers a cloud-based way to offer text and voice interactivity  that you can programmatically control. I did a bit of research, expecting it to be a crazy, large, complicated API to learn. In less than 15 minutes I already had a phone number AND it was already responding to texts and calls. &#8220;This might just be a piece of cake after all!&#8221; I thought.

School has kept me really busy, but this was a really exciting project to me, so I managed to pass up a bit of math homework and did a couple of hours or programming on this. Soon I had a voting system that when texted, would tabulate votes, and refuse to accept multiple votes from the same number.

&#8220;But Sarah,&#8221; I would hear, &#8220;what if they don&#8217;t have a cell phone?&#8221;  Really? Practically everyone does, and I&#8217;m sure everyone attending an _engineering_ event would have one.

&#8220;But Sarah,&#8221; I also heard, &#8220;what i they don&#8217;t have texting?&#8221; Really? Every phone out there since the mid-90s supports texting. Even if they have to pay a nickel or dime to text. And why not spend that to vote for your favorite candidate?

So after some tests with my phone, I took it to other SWE members who tested it out. It worked for the 5 of them. Then to the student council meeting a week later, and it worked for the 20 of them. The big test: The event.

I paid to get the full account, and the time came at the event: The People&#8217;s Choice vote. They had 5 minutes to vote, and the phone number showed up on the projector. I watched on my own computer at the votes. And I anxiously waited during those 5 minutes, expecting something bad to happen.

<figure id="attachment_333" aria-describedby="caption-attachment-333" style="width: 300px" class="wp-caption alignright"><img class="size-medium wp-image-333" src="http://sarahwithee.com/wp-content/uploads/mrengineer_twilio-300x161-300x161.jpg" alt="Mr. Engineer results screenshot" width="300" height="161" /><figcaption id="caption-attachment-333" class="wp-caption-text">Mr. Engineer results screenshot</figcaption></figure>

And nothing did. My program worked _flawlessly!_

The candidate was crowned a few minutes later after they had to tally up the judges&#8217; votes (that was by hand) but a few minutes to crown him definitely beat the 15 minutes just to count the votes last time. And there was no cheating! (I could tell as my logs showed several people tried voting multiple times!)

All in all I was rather proud. I was definitely a &#8220;holy cow my program worked flawlessly!&#8221; high for the rest of the night! And I learned a super cool API system that I can hopefully do something cool with.

_Have you ever worked on a project that you were beyond ecstatic that it worked so flawlessly? Tell me about it in the comments below!_

~ Sarah

P.S. Any good ideas on what I should with my Twilio account now? I&#8217;m thinking text-based Hangman game or something.

P.P.S. People have wondered how I built it. Twilio makes calls to a special page on my server (a PHP script) and it responds by generating an XML file in return which tell Twilio what to do in response to the call/text. I had it check the vote to see if it was valid, check a MySQL database to see if the vote already existed, then stored it in the database. Another PHP script just did some quick calls to the database to tally the votes.