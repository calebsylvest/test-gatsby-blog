---
title: "Beanstalk"
cover: "https://unsplash.com/photos/kRaH720CCRE"
date: "2014-01-07"
author: "caleb"
category: "code"
tags:
  - development
  - github
  - mobile
  - responsive web design
---

<h1>Beanstalk Demo</h1>

<p>A flexible, responsive grid system built with attitude using Sass. Beanstalk is a simple grid solution innately created as a Sass partial for easy addition to any project. Beanstalk is powerful and customizable, but not overly complicated. It offers easy to use and edit classes for building a mobile first, 100% responsive website.</p>

<p>Beanstalk was loosely based off the grid system used by Zurb's Foundation, but available for addition to any project. So if you like working with Foundation and want a similar grid system to add to other project, Beanstalk is for you.</p>

<h2>Getting Started</h2>

<p>Getting started with Beanstalk is super simple, after all the only necessity is adding the <code>_grid.scss</code> file to your Sass based project.</p>

<ul>

<li>Download or Clone the Beanstalk project from Github (or just the <code>_grid.scss</code> file)</li>
<li>Add the <code>_grid.scss</code> partial to you Sass based project, and reference in the parent .scss file</li>
<li>Compile code (I'm using Compass)</li>
<li>Check the compiled CSS file, all Beanstalk grid classes should be available</li>
</ul>

<h2>How To Use</h2>

<p>Beanstalk uses a <code>.row</code> and <code>.col-#</code> syntax to build a flexible grid.</p>

<h3>Variables</h3>

<p>Beanstalk dynamically builds a grid based on customizable variables. The <code>_grid.scss</code> file includes basic variable defaults that can be modified or overwritten in a <code>_vars.scss</code> partial (or whatever method you prefer to handle variables).</p>

<p>The <code>$row-width</code> variable controls the max-width of a responsive site. The <code>$column-gutter</code> variable controls the gutter between grid columns. The <code>$total-columns</code> variable controls the number of columns generated in the grid. By default Beanstalk is a 12 column grid system, but changing the number of columns is easy.</p>

<pre><code>$row-width: 960px !default;
$column-gutter: 0.9375em !default;
$total-columns: 12 !default;</code></pre>

<h3>Grid Building</h3>

<p>Beanstalk uses a <code>.row</code> and <code>.col-#</code> syntax to build a flexible grid, where all columns are contained within a parent <code>.row</code>.</p>

<pre><code>&lt;div class=&quot;row&quot;&gt;

  &lt;div class=&quot;col-8 column&quot;&gt;
    This is the main content area.
  &lt;/div&gt;

  &lt;div class=&quot;col-4 column&quot;&gt;
    This is the sidebar area.
  &lt;/div&gt;

&lt;/div&gt;</code></pre>

<h4>Working Mobile First</h4>

<p>The Beanstalk grid system works with a mobile first mentality, meaning the bare minimum of code is loaded on mobile devices (with the least amount of bandwidth) and built upon for desktop browsers (typically higher bandwidth).</p>

<p>By default all <code>.column</code> grid containers are 100% full-width on mobile, defined by the <code>.column</code> class. The <code>.col-#</code> grid styles kick in on larger viewports through the use of a @media-query calling a <code>$small-screen</code> variable (you can change the variable to whatever your want, or just a number).</p>

<p>Beanstalk also offers extra mobile styles to minutely control the display of content specifically on mobile devices. Add the mobile class <code>.small-col-#</code> on top of other grid classes for specific positioning on mobile.</p>

<pre><code>&lt;div class=&quot;row&quot;&gt;

  &lt;div class&quot;small-col-6 col-4 column&quot;&gt;
    On mobile, will be a two column grid and on desktop will be four column
  &lt;/div&gt;

  &lt;div class&quot;small-col-6 col-4 column&quot;&gt;
    On mobile, will be a two column grid and on desktop will be four column
  &lt;/div&gt;

  &lt;div class&quot;small-col-6 col-4 column&quot;&gt;
    On mobile, will be a two column grid and on desktop will be four column
  &lt;/div&gt;

  &lt;div class&quot;small-col-6 col-4 column&quot;&gt;
    On mobile, will be a two column grid and on desktop will be four column
  &lt;/div&gt;

&lt;/div&gt;</code></pre>

<h3>Modifiers</h3>

<p>Beanstalk offers several types of grid modifiers allow the right amount of control of a website layout.</p>

<h4>Push</h4>

<p>Adding a <code>.push-#</code> class offers a way to bump content to the right.</p>

<pre><code>&lt;div class=&quot;row&quot;&gt;

  &lt;div class=&quot;col-4 push-2 column&quot;&gt;
    A four column container that is pushed two column widths to the right.
  &lt;/div&gt;
  &lt;div class=&quot;col-6 column&quot;&gt;
    A six column container.
  &lt;/div&gt;
&lt;/div&gt;</code></pre>

<h4>Pull</h4>

<p>Adding a <code>.pull-#</code> class offers a way to pull content to the left.</p>

<pre><code>&lt;div class=&quot;row&quot;&gt;

  &lt;div class=&quot;col-6 column&quot;&gt;
    A six column container.
  &lt;/div&gt;
  &lt;div class=&quot;col-4 pull-2 column&quot;&gt;
    A four column container that is pulled two column widths to the left.
  &lt;/div&gt;
&lt;/div&gt;</code></pre>

<h4>Collapse</h4>

<p>Adding <code>.collapse</code> along with a <code>.row</code> will zero out the gutters of all children columns.</p>

<pre><code>&lt;div class=&quot;row collapse&quot;&gt;

  &lt;div class=&quot;col-8 column&quot;&gt;
    A main content section that no longer has gutters.
  &lt;/div&gt;
  &lt;div class=&quot;col-4 column&quot;&gt;
    A secondary content section that no longer has gutters.
  &lt;/div&gt;

&lt;/div&gt;</code></pre>

<h4>Collapse-outer</h4>

<p>Adding <code>.collapse-outer</code> along with a <code>.row</code> will zero out the left gutter of the first column and the right gutter of the last column. This allows a way to align content if needed.</p>

<pre><code>&lt;div class=&quot;row collapse-outer&quot;&gt;

  &lt;div class=&quot;col-8 column&quot;&gt;
    A main content section that has a right gutter but the left gutter has been zeroed out.
  &lt;/div&gt;
  &lt;div class=&quot;col-4 column&quot;&gt;
    A secondary content section that has a left gutter but the right gutter has been zeroed out.
  &lt;/div&gt;

&lt;/div&gt;</code></pre>

<h2>Support, Questions, &amp; Suggestions</h2>

<p>If you have a question or issue:</p>

<ol>

<li>[Log an Issue] (<a href="https://github.com/calebsylvest/beanstalk/issues">https://github.com/calebsylvest/beanstalk/issues</a> &quot;Log an Issue for Beanstalk&quot;)</li>
<li>Send me an email at [<a href="mailto:caleb.sylvest@gmail.com">caleb.sylvest@gmail.com</a>] (<a href="mailto:caleb.sylvest@gmail.com">mailto:caleb.sylvest@gmail.com</a>)</li>
<li>Find me on Twitter at <a href="https://twitter.com/sylvezine">@sylvezine</a></li>

</ol>
