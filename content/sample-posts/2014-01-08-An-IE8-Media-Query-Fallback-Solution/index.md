---
title: An IE8 Media Query Fallback Solution
date: '2014-01-08 09:00:26'
tags:
- development
- ie8
- media-queries
- mobile
- rwd
---

With Responsive Web Design building a site Mobile First is an excellent way to build site infrastructure, serving the least amount of code to devices that often have less bandwidth and building up from there.

A problem is that IE8 and below do not support media-queries, thus when users visit a Mobile First site using IE8 they are served only a mobile site on a desktop browser. Whomp whomp! Personally I’m all for dropping support of IE8 and not worrying about it (which is usually what I do) but sometimes you <em>must</em> support IE8 whether you want to or not. <a href="http://zurb.com/article/1265/ie8-is-going-the-way-of-the-dodo-so-why-s" target="_blank">Microsoft will no longer support IE8 as of April 2014</a>, and while that’s great to hear it does not mean IE8 users will be upgrading.

<!--more-->

I hate IE8, don’t want to support it or spend too much time making sure it works. Plus it already has one foot in the grave, so why should I? Normally I wouldn’t give IE8 a second thought, but the other day I came up with a simple solution to make sure IE8 plays nice with your RWD site and requires practically no effort.

<h2>Things Are Breaking</h2>

When building Mobile First containing elements are typically set to 100% width of the viewport (or something similar) to take advantage of the small screen until a certain breakpoint is reached. This is where things can get funky, and fast. Some aspects of a site may appear fine, but others can quickly get screwy - paragraph widths, mobile images scaling up, layout issues.

<figure><img class="alignnone size-full wp-image-142" alt="ie8-media-query-01" src="http://calebsylvest.com/blog/wp-content/uploads/2014/01/ie8-media-query-01.jpg" width="1000" height="586" />

<figcaption>An example from my personal portfolio site viewed in IE8. You can see the Mobile version of my site is displayed in a browser and the content width is set to 95%. Now, that's not too bad, but the line-length is way too long. And if I had more going on with my site things would be screwy. Screenshots taken with <a title="BrowserStack" href="http://www.browserstack.com/" target="_blank">BrowserStack</a>.</figcaption>

</figure>

<h2>What If A Ton of Customers Use IE8?</h2>

I mentioned sometimes you <em>must</em> support IE8; an example in my career where supporting IE8 was a must was when I was building sites in the music industry (2012 &amp; 2013). Surprisingly (or not), the percentage of users visiting client sites with IE8 accounted for about <em>35% of all traffic</em>, particularly in the country music arena. And I’m not talking about small time music artist you’ve never heard of, I’m talking about internationally known artist such as Brad Paisley, Third Day, The Band Perry, and Alice Cooper. An artist like Third Day could have <em>1,000,000+ unique visitors</em> every month, that means <em>350,000 users</em> are visiting using IE8. Sounds like we need a solution, and a good one.

<h2>The Options</h2>

We can agree that in a case where a large percentage of customers use IE8 something must be done to provide a useable version of a site. There are two basic ways to tackle the IE8 issue:

<ol>
    <li><strong>Create an IE8 specific stylesheet.</strong>A new stylesheet is a common method that has been used for years. But dang, that can be a lot of work with not much return. In the case of the music sites, we created separate stylesheets specifically for IE8. First we would build the entire site Mobile First, once everything was completed we copied the styles for desktop over into an IE8- stylesheet and modified CSS3 properties (probably not the best method, but whatever). Separate stylesheets are also difficult to maintain. If there was a bug or additional feature added later you would have to remember to also copy the new code over to the IE8 stylesheet. Yuck.</li>
    <li><strong>The Super-Secret-Awesome Method.</strong>Forget creating extra stylesheets, copy-pasting code, and all that junk. For mobile your containing elements and/or columns (depending on your method and if you are using a grid system) are probably set to be 100% width, and above a specified breakpoint (600px in our example below) the containers rearrange into Main Content and Sidebar areas, etc. If the width is set to 100% we are going to have problems when the mobile site is loaded on a desktop IE8 browser, but if we add a max-width we gain some control over the unruley IE8! I suggest adding a max-width around 600-700px, that way the site is large enough to not look like a mistake on desktop but not too large to get screwy (remember we are serving mobile styles, images, etc.).</li>
</ol>

<pre><code>
// styles will be applied to mobile
.feature-container, 
.feature-sidebar { 
  width: 100%; 
  max-width: 650px; 
} 

// styles will be applied and overwrite the above code above 600px
@media screen and (min-width: 600px) { 

  .feature-container { 
    width: 70%; 
  }

  .feature-sidebar { 
    width: 30%; 
  } 
}
</code></pre>

<small><em>note: remember this is a Mobile First website, so all code written outside of a media query applies to mobile and up, while desktop specific styles are written in media queries</em></small>

<figure><img class="alignnone size-full wp-image-144" alt="ie8-media-query-02" src="http://calebsylvest.com/blog/wp-content/uploads/2014/01/ie8-media-query-02.jpg" width="1000" height="586" />

<figcaption>After adding one line of CSS my Mobile First site now looks decent and usable in IE8. Screenshots taken with <a title="BrowserStack" href="http://www.browserstack.com/" target="_blank">BrowserStack</a>.</figcaption>

</figure>

<h2>Wrap Up</h2>

Talk about a simple method to corral the fiasco of IE8 media queries. While IE8 is on the way out, there are still circumstances where you may need to pay attention to it. If so, I hope this helps. If you have question or comments add them below or find me on Twitter at <a href="https://twitter.com/calebsylvest" target="_blank">@calebsylvest</a>

<strong>Update: has anyone used this method or found it helpful? I'd be interested to hear thoughts or concerns.</strong>
