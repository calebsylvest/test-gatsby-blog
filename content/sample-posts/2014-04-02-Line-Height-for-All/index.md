---
title: Line Height for All
date: '2014-04-02 09:00:55'
tags:
- css
- development
- development
- line-height
- web-typography
---

Line height is one of the small things that can make or break your design. A little detail that is often overlooked or not properly massaged to perfection. This is going to be a short-and-sweet post outlining the best method for declaring line-heights, and there is a group discussion question at the end!
<!--more-->

<h2>Kill All The Units</h2>

The line-height property controls the vertical rhythm of typography on the web. The property accepts values with several type of units, including:

<ul>
<li><strong>Number.</strong> A number without an appended unit.</li>
<li><strong>Percent.</strong> Percent multiplies the font-size by the defined percent. </li>
<li><strong>Value.</strong> A number can be added to the line-height appended with a unit, such as px, pt, cm, and more.</li>
</ul>

In the past you may have done something like this:

<pre><code>p {
  font-size: 14px;
  line-height: 20px;
}
</code></pre>

And that will work, but if you decide to change something simple like the font-size to 22px (get on the big font trend!) then suddenly stuff starts to look wonky!

[caption id="attachment_308" align="alignnone" width="2163"]<img src="http://calebsylvest.com/blog/wp-content/uploads/2014/04/line-height-01.png" alt="Example of line-height declared with pixels" width="2163" height="601" class="size-full wp-image-308" /> Example of line-height declared with pixels[/caption]

That's why I always say go with <em>unitless</em> line-height declarations. We can take the same example, but instead of using a pixel base line-height, make the styles awesome and future proof by using unitless inputs, like this:

<pre><code>p {
  font-size: 14px;
  line-height: 1.4;
}
</code></pre>

Looks good right, not much different than than the earlier example. But let's see what happens if we change the font-size. Unitless declarations are awesome because they are relative to the element instead of specifically declaring the line-height with pixels. So even if we bump the font-size way up the vertical rhythm of our typography still looks great!

[caption id="attachment_310" align="alignnone" width="2163"]<img src="http://calebsylvest.com/blog/wp-content/uploads/2014/04/line-height-02.png" alt="Example of line-height declared with a unitless number" width="2163" height="804" class="size-full wp-image-310" /> Example of line-height declared with a unitless number[/caption]

So I hope we can all agree that Unitless line-height values are the best way to go, right? Friends don't let friends use pixel line-heights, and if I find out you are I'll kick your puppy. There, nuff said.

<h2>Is This A Good Idea?</h2>

So, I seriously am asking a question here, and diverging from a lesson to turn this into a request. The easiest way to handle line-height throughout a website and ensure consistency for all elements is to apply a global line-height to the body, like this:

<pre><code>body {
  line-height: 1.4;
}
</code></pre>

This ensures the line-height of all paragraphs, buttons, input fields, even text people forget to wrap in a tag all have a consistent line-height applied. My one concern with this method is I typically try to stay away from any one thing that affects the entirety of my site build (except border-box) so in a way I'm torn. Honestly, it feels so right I don't care if it's wrong.

But I really do care, so if you have any input please leave a comment or tweet me at <a href="https://twitter.com/calebsylvest">@calebsylvest</a>.
