---
title: "Writing Useful Github Issues"
cover: "https://unsplash.com/photos/kRaH720CCRE"
date: "2014-02-05"
author: "caleb"
category: "code"
tags:
  - development
  - github
  - issues
  - management
  - team
---

Finding out there is something wrong with the work you did on a project is bad enough, but when reading through issues is like deciphering Latin, well it’s no wonder so many developers <a href="http://en.wikipedia.org/wiki/Going_postal">go postal</a>. Writing detailed, thorough, and transparent issues should be the goal of everyone on your team, because we most often write issue request for someone other than ourselves. So let’s follow the Golden Rule of issue request, “Write issue request for others as you would like them written for you (or better).”

Writing good issue request, and teaching a team the same, will save everyone time, money, and confusion in the long run. It’s really a no-brainer. I’m talking specifically about Github, because I use it most of the time for code management and I know many other developers do as well, but what I cover can be applied to any issue management tool.

<h2>What An Issue Should Accomplish</h2>

When a person reviews an Issue Request there should be enough information that they have a good handle of what is being discussed, they don’t need to know or come up with a solution instantly, but nothing about the issue should be mystery meat.

<h3>The Perfect Problem</h3>

Writing the <em>perfect</em> issue probably isn’t possible, because we are all different and have subjective views on what makes sense or how a task should be handled. But we can create a general “good faith” guideline that if we all attempt to follow will make projects run smoothly, better our relationship with coworkers, and put a smile on your grumpy boss’s face. Let’s cover the basic anatomy of an Issue Request and how we can be awesome:

<strong>Relevant Subject Line.</strong> The subject should be specific but not lengthy. You have 40-60 characters to give a clear and concise summation of the issue. For more about writing subject lines, check out <a href="http://www.nngroup.com/articles/microcontent-how-to-write-headlines-page-titles-and-subject-lines/">Microcontent: How to Write Headlines, Page Titles, and Subject Lines</a>.

<strong>URL.</strong> Please, please, please, I’m begging you. If you make me wonder which page of a 1500 page website an issue is related to, I swear I will hunt you down and kick your puppy.

<strong>Full Description.</strong> The meat of an issue should describe in detail the specifics of a problem. Better to over-communicate than be vague. Be clear in your writing and re-read the content from someone else’s perspective, coming at it knowing nothing about the situation.

Bug reports require a more specialized attention to detail and procedure, I’m not going to cover that in detail here but do suggest reading <a href="https://github.com/textmate/textmate/wiki/Writing-Bug-Reports">Writing Bug Reports</a>.

<strong>Situation.</strong> Once again over-communication is better than not mentioning specifics. Whether you believe it’s relevant or not listing the Browser, Operating System, on a Mobile device, in Incognito Mode, or has Javascript disabled could be relevant The more specific the better. I once had an issue from a customer that made zero sense until (after getting screenshots via email from him) I deduced he was using Incognito Mode, which wrecks havoc on Icon Fonts.

<div style="background-color:#eee; padding:1em; font-size:.7em; color:#626055; margin-bottom:1.6em;"><strong>Update:</strong> Use <a href="http://supportdetails.com/" title="Support Details" target="_blank">Support Details</a> to quickly get the important settings from your machine or a customers machine!</div>

<strong>Screenshots.</strong> Screenshots are a developers best friend. If you can add a screenshot, do. It can’t hurt and may actually clarify. One thing, if there is an issue with a button at the bottom of the screen, take a shot of that one button and its surrounding area. Please don’t send a full desktop screenshot on your 27” iMac. P.S. Screenshots with annotated drawings and notes are awesome!

<strong>More.</strong> There are always more things you can do, such as tags. Each situation is unique and has its own challenges. Do what is best to fully and clearly describe an issue.

<figure><img class="alignnone size-full wp-image-205" alt="An example of a poorly formated issue in Github" src="http://calebsylvest.com/blog/wp-content/uploads/2014/02/bad-github-issue.jpg" width="2094" height="1131" />

<figcaption>An example of a poorly documented issue in Github.</figcaption>

</figure><figure><img class="alignnone size-full wp-image-206" alt="An example of a well documented issue in Github" src="http://calebsylvest.com/blog/wp-content/uploads/2014/02/good-github-issue.jpg" width="2094" height="1752" />

<figcaption>An example of a well documented issue in Github. The title is descriptive, a URL links to where the problem can be found, the body of the message thoroughly describes the issue, information relating to the software and hardware is added, and a screenshot tops it all off!</figcaption>

</figure>

<h2>Shake Things Up</h2>

Let’s face it, capturing peoples attention is tough. And since we can’t hire a marketing firm to make our issue request more appealing we need to do the best we can with the tools at our disposal. Using simple styles highlights the most important aspects of an issue. Github makes this super simple to achieve with <a href="https://help.github.com/articles/github-flavored-markdown">Github Flavored Markdown</a>, and dang, they have a cheat-sheet button available! Thanks Github!

<ol>
    <li><strong>Lists Are Awesome.</strong> List are easy for humans to parse through and organize information.</li>
    <li><strong>Style Key Words.</strong> Don’t be afraid to <em>italicize</em> or <strong>bold</strong> words if it helps point out important aspects to note.</li>
    <li><strong>Link the friggin’ URLs.</strong> If URLs are not automatically linked and I find out you didn’t link a URL, I swear I will hunt you down and kick your puppy!</li>
</ol>

<h2>What Not To Do</h2>

Well heck, this is the easy part.

<ol>
    <li><strong>Assume the Solution.</strong> Unless you <em>really</em> know what the solution is, and you are expertly familiar with the situation, do not assume you know how to fix something and tell the Assignee what the problem is and how to fix it.</li>
    <li><strong>Don’t Be Vague.</strong> “Something is wrong with the slider” is not a good description of the problem. Don’t assume someone can go look at something and automatically figure out exactly what was meant.</li>
    <li><strong>Don’t Be A Puppy Kicker.</strong> Be Courteous. We can all be emotional beings, and being told we did something wrong can really stir the pot. So be kind and courteous, please. Remember the other Golden Rule, “Treat others the way that you want to be treated.”</li>
</ol>

<h2>A Little Bit More</h2>

While writing my thoughts I did a bit of research as well to see what others say about writing Issues. Two articles I found useful are <a href="http://wiredcraft.com/posts/2014/01/08/how-we-write-our-github-issues.html">How We Write Github Issues</a> by Wiredcraft, and <a href="http://www.defmacro.org/2013/04/03/issue-etiquette.html">Github Issue Etiquette</a> by Slava Akhmechet. Both make good points, some I agree with and some I don’t, but it’s up to each person individually (or team) to determine a method that makes sense and is helpful.

If you have questions or comments feel free to leave a note in the comment area below, or find me on Twitter at <a href="https://twitter.com/calebsylvest">@calebsylvest</a>.
