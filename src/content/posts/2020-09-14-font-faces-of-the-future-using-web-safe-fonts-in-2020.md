---
template: blog-post
title: "Font-faces of the Future: Using web-safe fonts in 2020"
slug: text and typography best practices
date: 2020-09-14 16:24
description: text and typography
featuredImage: /assets/markus-spiske-yxr8igwm4e0-unsplash.jpg
---
# **Web-fonts and Faces**

**The year is currently 2020:**

While this year has been far from normal, things are consistently changing, and anything could happen at any point. However, these are no excuses for best practices of text and typography.

**Font-families, Faces, and Use:**

First of all, what is a font-family? A font-family is the main category that the particular font comes from. These are based on general text appearance and include five families: Cursive, Fantasy,Serif, Sans-serif, and Monospace.  

Each family has its own variations of subtext, or font-faces. This is where writers can get creative in their choices. 

Now that you know a little bit about fonts, how do you use them? This is as easy as modifying your html. Simply use the style attribute within your paragraph <p> tags: 

```
<p style = "font-family:courier,arial,helvetica;">
Insert Text
</p>
```

In the above example, the multiple font-families from left to right, are the order in which the user machine will parse the various fonts. In the event one font is not available, the machine knows to move to the next one. 

**What Is A Web-safe Font:**

A web-safe font is simply any font that has a high chance of already being pre-installed on most computer devices.

**Why Do We Need Web-safe Fonts:**

There are multiple reasons why these fonts are valuable to include in any piece of development. 

For starters, the very nature of a web-safe font adds security to your webpage. In the event that your chosen font is not available or complete, the computer will be able to choose a backup font in its place. This also allows users to have some creative control in this event, they can have backups prepared that are similar enough that the whole design will not be interrupted. 

The other good reason is that these fonts are most likely pre-installed to the user device. Thus, when a machine loads your work, it will take less time to render and take up less bandwidth. 

**Should I Use Web-Safe:**

If you were to ask me, I would say most definitely yes. These are great practices even if it ends up not being the main font on your page. 

However, while these fonts are good to use, there is far more creativity with some of the new fonts that have been created.

Some popular fonts include:

1. Arial

![Arial Font](/assets/download.png)

2. Courier New

![Courier New Font](/assets/download-1.png)

3. Times New Roman

![Times New Roman Font](/assets/download-2.png)

4. Georgia

![](/assets/download-11.png)

###### Resources: 

<https://www.hostinger.com/tutorials/best-html-web-fonts>

<https://www.guru99.com/web-safe-fonts-html-css.html>

<https://www.webfx.com/blog/web-design/why-we-still-need-web-safe-fonts/>