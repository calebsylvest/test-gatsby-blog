---
title: "The Subtly Significant Difference of CSS Pseudo Selectors"
cover: ./covers/cover-pseudo-selector.jpg
date: "2018-04-28"
author: "caleb"
category: "code"
tags:
  - css
  - code
---

Did you know there is a slight difference in CSS pseudo selector syntax?

I didn't. And I've been writing CSS for the better part of 10 years. Turns out, I've been mis-using pseudo selectors for years. Does that matter? Well, let's find out.

## Pseudo Class vs Pseudo Element
Recently, while inspecting stylesheets for various third party code sources I noticed sometimes a single colon `:` would be used for pseudo selectors and sometimes double colons `::`. I thought (mistakenly) the double colon syntax was an outdated way to write styles. So, finally I scratched my head and searched for a reference.

Turns out I was wrong. The double colon syntax is the *new* syntax starting with CSS3. But, only for Pseudo Elements.

So, what's the difference between a Pseudo Class and Pseudo Element?


### CSS Pseudo Classes

Pseudo classes represent the *state* of an element.

Just like normal classes, pseudo classes can be stringed together. So you could string together many like `.button:last-child:hover:disabled`. There's no limit to how many pseudo classes can be applied to an element except your imagination!

##### Common Pseudo Classes
`:active` `:hover` `:focus` `:not()` `:nth-child()` `:checked` `:disabled`

### CSS Pseudo Elements

Pseudo elements represent a specific part of an element and are represented using a double colon.

##### Common Pseudo Elements
`::after` `::before` `::selection` `::first-letter` `::first-line` `::placeholder`

#### Wrap Up
The reason it took so long for me to figure out the difference is because the single colon syntax for Pseudo Elements is still valid today (except for pseudo elements added in CSS3 and beyond). And since *technically* the syntax was valid my web tools and compilers never threw an error.

But now I know, and *you* do too!

---

#### TL;DR

- Pseudo classes only use one colon. Ex: `:hover, :focus, :active`
- Pseudo elements are written with two colons. Ex: `::before, ::after`

---

### 📘 Reference

- [CSS Pseudo Elements →](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements)
- [CSS Pseudo Classes →](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes)
