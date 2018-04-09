---
title: "You May Be Using @font-face Incorrectly"
cover: "https://unsplash.com/photos/random"
author: "caleb"
date: "2013-12-18"
category: "typography"
tags:
  - css
  - typography
  - web-typography
published: true
---

When I discovered that I had been using the [@font-face](http://www.font-face.com/) rule incorrectly (for quite a long time actually) I was floored. How could this have happened? I was working off of numerous tutorials and suggestions online and they were all saying the same thing. Just goes to show that the internet is not always right.

Anyway, there are two basic methods for using the `@font-face` rule, they both work but the first (that I was using and most people on the internet are also using) is like showing up to a volleyball game with a cast on your leg and the sun in your eye.

## Declaring the @font-face Rule

I’m only going to show the <em>correct</em> way to work with `@font-face`, with code examples, and then explain the why. Below we are loading three Open Sans files - the regular, bold, and bold italic typefaces.

```css
<span class="citation">@font-face</span> {
  font-family: 'Open Sans';
    src: url('OpenSans.eot');
    src: url('OpenSans.eot?#iefix') format('embedded-opentype'),
 url('OpenSans.woff') format('woff'),
 url('OpenSans.ttf') format('truetype'),
 url('OpenSans.svg#OpenSans') format('svg');
  font-weight: normal;
  font-style: normal;
}

<span class="citation">@font-face</span> {
 font-family: 'Open Sans';
    src: url('OpenSansBold.eot');
    src: url('OpenSansBold.eot?#iefix') format('embedded-opentype'),
 url('OpenSansBold.woff') format('woff'),
 url('OpenSansBold.ttf') format('truetype'),
 url('OpenSansBold.svg#OpenSansBold') format('svg');
 font-weight: bold;
 font-style: normal;
}

<span class="citation">@font-face</span> {
  font-family: 'Open Sans';
    src: url('OpenSansBoldItalic.eot');
    src: url('OpenSansBoldItalic.eot?#iefix') format('embedded-opentype'),
 url('OpenSansBoldItalic.woff') format('woff'),
 url('OpenSansBoldItalic.ttf') format('truetype'),
 url('OpenSansBoldItalic.svg#OpenSansBoldItalic') format('svg');
  font-weight: bold;
  font-style: italic;
}
```

### The Difference

- The first thing to notice is that for each file instance we are naming the font-family to be `Open Sans`, this is different than the typical methodology you may have seen where each font weight has a specific font-family name, such as `Open Sans`, `Open Sans Bold`, and `Open Sans Bold Italic`, which is wrong (it’s not your fault you’ve been doing it the wrong way, I mean dang, even [Font-Squirrel](http://www.fontsquirrel.com/) is packaging our web-type incorrectly).
  - Did you know you could actually name the font-family anything you want, heck, you could call it `booger` if you want.
- Instead of setting the font-weight and font-style to `normal` for each instance, as we did with the old, broken methodology, set them according to what font style you are referencing. For instance, for `Open Sans Bold` files we name the font-family to be `Open Sans` the font-weight to be `bold` and the font-style to be `normal`. For `Open Sans Bold Italic` the font-family name is `Open Sans`, the font-weight is `bold` and the font-style is `italic`.

### How Do We Use This?

There is nothing really different about using this method in your stylesheets, we already covered the main issue of how to properly *load* your font files. Anytime a typographic element should be the imported typeface set the font-family to (in this case) Open Sans. If we want the element to have a certain styling add the appropriate font-weight or font-style attributes. Let’s look at some examples:

```css
// we want paragraph text to be the standard font weight
p {
  font-family: "Open Sans", sans-serif;
}

// let’s make a users name bold
.avatar-name {
  font-family: "Open Sans", sans-serif;
  font-weight: bold;
}
```

## Why Does It Matter?

Following this methodology when using `@font-face` is the best and most natural way to work with typography on the web. Doing so will set up a website for easier management and future extensibility. Here’s the roundup:

- **Natural Typography**. Relate using the `@font-face` file imports to using classic web-safe font stacks. When referencing an Arial font stack you don’t have to specify the font-family as `Arial Bold` or `Arial Italic` each time you wanted to style type, you style using font-weight and font-style accordingly.
- **Fallback**. Using this natural method of web typography with `@font-face` creates a simpler to work with typographic system for a website. Suppose the primary font did not load properly or you later decide to change the primary typeface, with the old methodology you would have to search through all your stylesheets to ensure all instances of the typeface are updated correctly. But following the Natural method, if the font files do not load the site will still hold to the base typographic style originally intended. If you later decide to change the primary typography, migrating to a new typeface will be infinitely easier.

Typography is the base of a website, the back bone, so it makes sense that the typographic system we build a website on should be properly constructed, flexible, and able to be extended over time. If you have questions or comments feel free to leave a note in the comment area below, or find me on Twitter at <a href="https://twitter.com/calebsylvest" target="_blank">@calebsylvest</a>.
