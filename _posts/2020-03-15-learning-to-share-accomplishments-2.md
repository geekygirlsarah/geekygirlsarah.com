---
title: "Learning to Share Accomplishments: Part 2 - Sharing My Accomplishments"
date: 2020-03-15T10:00:00-04:00
permalink: /2020/03/15/learning-to-share-accomplishments-2/
author_profile: true
toc: true
toc_label: "Post Contents"
toc_icon: "file-alt"
medium_post:
  - ""
categories:
  - Accomplishments
  - Job Hunting
tags:
  - 
---

This post is a part of a series on job hunting and job interviewing.
{: .notice--info}

<figure>
    <img src='https://www.hdwallpaper.nu/wp-content/uploads/2017/04/cat-11.jpg' alt='Until I figure out a better image' width="50%" height="50%" />
    <figcaption>Until I figure out a better image to put here.....</figcaption>
</figure>
This is the second part of a two-part post. The first part is more on how to share your career accomplishments. You 
may want to read it first. [Part 1 is here.](../learning-to-share-accomplishments-1/)

For part 2 of this post, I want to actually talk about those accomplishments. I think it's helpful for me to get out 
there and while it may not be as interesting or relevant for you, maybe in looking it over you can see some ways you 
can talk about your own accomplishments as well. 

## What I Personally Have Worked on in My Past Jobs

I want to spend some time looking back at my work. Like I said above, I've apparently had some times I've been terrible 
at talking about this in job interviews, so I wanted a list. I kind of want to use it as a thought exercise for me, 
but maybe also to help sell myself to anyone who might be reading this post. I don't intend this to be literally 
everything I've worked on, but perhaps more of the highlights from different points in my career. And who knows, maybe 
a future employer might see this and think I really would be an awesome addition to their team.

One other thing: I have literally had job interviews where, despite all of my developer experience, have looked at me 
and said "Looks like you do a lot of teaching stuff. Maybe you should be a teacher and not a developer." I've found 
it puts me in an incredibly awkward place to have to defend why I am applying for a developer job and these people 
don't even see me in that light. I'm not sure if that's, again, me not "selling myself" well or if that's me not 
writing out my resume well enough, or just things like conferences are more visible than projects I've worked on (which 
are usually NDAs or not publicly available). So I hope this post helps with that as well.

### Best Team: Data Pipeline Team

This team was created to replace a $1M/year third-party product with an in-house solution. The third-party product was 
expensive, a pain to set up, didn't scale well, and the company only used about 10% of it. Ours was built for this 
specific solution, scaled with the click of a few buttons, and cost closer to $1000/month (a VAST savings). 

**What did I Do?**

* I was the generalist on this team. I felt like I was the glue that when given a random problem to solve, thing to 
  research, or item to build, I just did it. This work often helped fix some problems that would have delayed our 
  release or fix an issue that would have popped up later on. 
* I figured out the best way to do an AWS-based service queue system for our monitoring microservice. I did the 
  research by looking at all of AWS's types of queueing systems and their costs of running. I later implemented a basic 
  prototype, and then wrote the final code to convert our monitoring service to push to it.
* We had a broken build for our client executable that wasn't building separate versions correctly. I wrote some shell 
  scripts that fixed Travis CI (for our Mac version) and AppVeyor (for our Windows version) to get both working. It 
  then built and uploaded to AWS S3 buckets in the correct versioned structure.
* I contributed at least one feature to the code base of every Scala microservice we had when I had no prior Scala 
  experience. (It's similar to Haskell, which I had done a project on in the past, so I picked it up quickly.)
* A teammate couldn't get one of our services working in Scala so they rewrote it all in Ruby over a weekend. We ended 
  up keeping that, but it was built to run locally. After that person quit shortly after, I Dockerized it, wrote the CI 
  scripts to deploy it to AWS, and got it to work with AWS's Aurora databases (as opposed to a local Postgres install). 
  I later ended up resolving at least 85% of the security flaws that came up in a security audit on it. I did this 
  without prior Ruby or Ruby on Rails knowledge, which I picked up quickly).
* When I was hired, they wanted me to start work immediately and relocate to Pittsburgh as I could. I started work 
  within about two weeks of the offer, and spent the first two months working remote out of Kansas City (where the time 
  zone was an hour earlier than my team). I also was packing to move at the same time I did this work.
* From day one, I was given ownership of two of the 8-10 microservices our project had.
* I wrote and modified existing Terraform scripts to add additional deploy and containerization features for some of 
  our microservices. (I had never used Terraform before either.)
* After our original manager was fired and a new one was brought in, I regularly checked in on and mentored the junior 
  member of our team when the new manager didn't take that on.
* We didn't have 1-on-1 meetings after our original manager wasn't there anymore. I tried to have unofficial 1:1s with 
  the two original remaining team members just to make sure they were doing ok. 

### Favorite Work Project: Team Metric Tracker

I really liked this project not because it was particularly complex or really cool, but because of the creative 
solutions that came out of it.

Our five-person team was all hired at the same time. We were on a three month internal project which helped us learn 
the security protocols for software at the bank. The project was sold to us as "make this Excel spreadsheet into a web 
app". Once we dived in deep, we realized this was a quirky problem with some hidden issues. The spreadsheet had a 
dozen tabs, data from several years, a constantly evolving report, and a dozen users that all added data to it. Our 
basic web app turned into a quirky data project that required data auditing, a report-designing system, hierarchies of 
management, and redefining terminology the department used. (For more fun, we were told another team tried to tackle 
this in the past and couldn't do it.)

**What did I Do?**

* While many of us worked on the original design and wireframes, I came up with the idea of redefining their terminology 
  (what we called "metrics" and different kinds of metrics) so it made sense to us (the client used a lot of words 
  interchangeably), and later I designed a way to abstract out the database tables to make it easy to store the 
  different kinds of metrics in the same table. It resulted in faster queries later.
* To ensure people could edit the actual data metrics, we had a sort of "meta" database table describing the metrics 
  themselves, then a table to store the metric data. (ex: "Widgets per hour" vs "this month we did 12 widgets/hr".) I 
  had suggested this idea originally and it replaced an old idea that wasn't really effective.
* Some metrics were calculated (ex: average per year might be the sum of the metric divided by 12). We wanted to ensure 
  users couldn't mess up these formulas. I came up with two ideas. The first was to make a formula that could be stored 
  with both constants (as in the "12" above) as well as ID numbers (so some metric might be database ID 45). Prefixing 
  a 'c' or 'i' on the number meant we could tell what the number meant, and ID numbers could just pull the metric from 
  it's table and row. This remained fast to query. 
* The second idea was to provide the user a calculator-like interface to allow users to enter only valid formulas. 
  While the calculator wasn't my idea, the validation scheme was. On the front end, we gave them a literal calculator 
  that you could also drag metric names into the equation. This used a state machine I designed to ensure whatever 
  they put in couldn't be saved until the formula was mathematically correct. On the back end, we used a math parsing 
  framework to validate the entry before it was saved.
* We needed to add auditing to the data so it tracked who entered what. I designed this system where audits were stored 
  in a separate audit table, both making saves and lookups easy.
* We needed a hierarchy of who could add, edit, or delete particular sets of data. I came up with the idea of tying in 
  our system with Active Directory so we could actually look up the management ladder and allow people to edit the 
  people's entries that were under them. If they moved teams, left the company, etc., they lost access as it 
  was in AD already, and required no special login or management tables in our product.
* We needed a way to create and run reports. We learned about a tool other teams used but realized on a short time 
  frame we probably wouldn't integrate it well so we built our own. I designed the structure of how people would 
  design reports, and then later with another team member, came up with a structure for how it would be stored in the 
  database.
* Reports were VERY slow in the beginning. I developed a caching system that would pre-calculate all calculated 
  metrics, and store those values as they were entered. Using the cached data took reports from a minute or longer to 
  load to about a second or less to load. 
* The other developers shied away from creating PDFs. I found a library and implemented an export of a report to PDF 
  files.
* Not only did we get a minimal viable product out in three months, but the next group of five hired after us took over 
  the project to finish our features. In addition, other departments in the bank saw our project and loved the open 
  design of it and wanted to adopt it for their own use.

### My Successes While Interning For Two Summers

I interned with a electronic document management company that loved me so much they brought me back the next summer. I 
was on different teams each time.

**What did I Do?**

* The first summer, I was handed a tiny bit of code that was supposed to build out a set of sample documents to test 
  in a report. After two months, I had expanded that from that tiny bit to an entire testing framework that would create 
  documents and test them against the business intelligence reports automatically. This reduced the work of our QA 
  person about 50% because she didn't have to manually test reports.
* I added internationalization to the the business intelligence installer application.
* The second summer, I was given a C# program to add features to. I had not learned C# before. I added the features 
  requested, but also discovered some quirks in how it ran on particular clients' machines. I also fixed those 
  additional bugs.
* I added a variety of features to a large JavaScript app that used jQuery (which I had never used at the time).
* During the second summer, I helped fellow interns not only understand the products they were working on, but often 
  went over and paired with them on debugging sessions to find errors and help them "rubber duck" on tasks. I 
  helped out 5 interns that summer.
* The developers of both of my teams had said they could tell I really was good at development and would be absolutely 
  happy if I joined their team after graduating.
* I was the first intern to show off a "Innovation Week" project in front of the whole company. It not only made many 
  of the 200+ developers know who I was after that, but the next year it inspired some other interns to build and share 
  a project of their own.
* People on both teams had told me they were surprised I was an intern as I had a lot of the skillsets of a full-time 
  software developer.
  
### Other Projects and Teams

**What did I Do?**

* At another team at the bank, I was the lowest experienced person there. I redesigned and rewrote a large chunk of 
  some software that made loan documentation.
* At the same team, I made design changes to the rewrite of another project that substantially reduced server workload 
  and network bandwidth.
* I was a part of a hackathon team at the bank that built a real time credit card fraud detection system. (The prior 
  system was SQL queries ran periodically throughout the day.) Our 15 person team implemented this system in 2 days 
  that processed over 2 GB of credit card transactions in under 10 seconds with 90% accuracy. The managers estimated 
  that, when refined then put into production, would save them about $1.2 billion dollars annually. 
* In 2007, I was hired on at a local technical support and consulting company. I started off in tech support but was 
  quickly writing Sharepoint scripts as well as later some custom development for different clients. I later helped 
  optimize a process for installing new computers more efficiently.
* In 2016, I upgraded a local magazine from having a hand-coded PHP website that was regularly quit working to a 
  Wordpress site. In order to move 2400+ articles from their archives to WP, I had to write a variety of scripts that 
  not only automated the database imports, but rewrote the articles to go from BBCode to HTML, as well as insert 
  images in place on the articles. The owner of the magazine says the site is now easier to use, looks more modern, is 
  mobile-friendly, and easier to update. It doesn't crash anymore.
* From 2009-2012, I started my own business to provide technical support, website development, and web hosting to 
  people in my city.
* I wanted a developer reference tool that allowed me to compare languages I know and ones that I don't know side by 
  side so I could quickly learn or reference a new language. I haven't found a tool exactly like I want (though there's 
  tools along similar lines but they aren't helpful for what I need). I started designing the architecture behind the 
  tool and have built a mock-up of how it will work. During Hacktoberfest 2019, I finished an actual working mock-up of 
  it. I need to write some documentation, fix a couple more small issues, then I intend to tell the world about my open 
  source project! I will also keep adding more data sources to it, and keep encouraging others to contribute to it as 
  well.
* I was involved in a robot competition team in college. For the three years I was involved, I contributed to building 
  or coding four robots. I broke the culture of the team having only one super-overworked developer. I also broke the 
  culture of this develoepr never sleeping during competitions. I brought in multiple other students and formed a 
  team. This allowed us to work more reliably and also get some sleep.
* At a local homeless services and food kitchen organization, I took them from passing around Excel spreadsheets with 
  donor information on it to having a centralized web-based donor tracking system. This enabled much better record 
  keeping as well as made it easier to send out mailings and tax receipts at the end of the year. While there, I also 
  sometimes helped make and serve food and helped them open and staff a thrift store to raise money for the 
  organization.
* After my local PFLAG chapter's website was hacked, I managed to undo the damage, restore backups, then implemented a 
  firewall and security system within Wordpress to (hopefully) prevent future attacks.

While I have a wide breadth of other accomplishments (like conference speaking, being on different board of directors, 
and some awards), I wanted to focus this post specifically on coding, software design, and technological 
solutions I have implemented.
   
## Conclusion

This part of the post took a _really_ long time to write. And rightfully so: I've done a lot in my career so far. I 
think I have done a lot of good, creative work. I'm hoping that while it may not have been directly useful to you to 
look at this post, maybe you have picked up on some good vibes you can use to help write or speak about your own 
accomplishments.

I'd love to hear if anything about these posts resonated with you. Feel free to reach out!

~ Sarah
