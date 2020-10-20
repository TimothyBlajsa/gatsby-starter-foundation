---
template: blog-post
title: "Metamorphosis: CSS transforms "
slug: metamorphosis-css-transform-s
date: 2020-10-20 15:07
description: css transforms
featuredImage: /assets/markus-spiske-qtfaxp6z0wk-unsplash.jpg
---
# Ch-ch-ch-ch-changes

Props to you if you know where that is from!

The next spot on our CSS list brings us to the world that is always changing, LITERALLY!

It's time we dive into CSS transforms, a powerful property that can be used to produce some very impressive renders.

## The Property

Before we explore these creative transforms, first we must understand the property that began it all, this being the transform property. 

This property is one that allows the developer to physically alter the rendered appearance of an element, whether this be a shape or some sort of text. This being said, it is a powerful tool, and can be utilized to both 2D and 3D animations. 

But that's getting ahead of ourselves. After all, we need to understand some fundamental principles first!

## The Principles

![](/assets/glenn-carstens-peters-0ib6_gx7bxk-unsplash.jpg)

### Going on-grid

When dealing with some transforms, it is important to reconsider how the computer reads a webpage. Despite how it looks by default, elements can be read as having a coordinate on the Courtesan Plane.

This plane, or grid, has three values we need to be aware of:

x-axis: horizontal direction

y-axis: vertical direction

z-axis: depth

However, these axes behave slightly different than a grid in the traditional sense; this is due to the change of input data having an effect of the elements relative to space. 

The x-axis can also be looked at as a ray running from left to right, increasing in value the further right it travels

The y-axis can also be looked at as a ray running from bottom to top, increasing in value the further up it travels

The z-axis can also be looked at as a ray running from back to front, increasing in value the closer to the viewer it travels

Acceptable values include pixels!

Note: these axes all intersect at the Origin (0, 0, 0)

![](/assets/luis-eusebio-5sut9q8jqrq-unsplash-3-.jpg)

### The Unit Circle

The next principle to consider is the aspect of rotational or circular space. This exists in the form of the unit circle.

In terms of web development, this is not as much about the circle itself as it is the units of measurement, this mainly being degrees. The input value will translate as turning the element some fraction of a turn about the origin, in a clockwise manner, however, with some experimentation you will realize that certain values will have no effect, similar effect, or opposite counter-rotational effect. 

Acceptable values include deg, %, and turn!

![](/assets/sleep-music-v34e2uox5xq-unsplash-3-.jpg)

### The Perspective

The third fundamental principle to consider when using transforms is perspective. This is what can truly impact the way an otherwise flat design stands out on the page.

Note: This is extremely important when dealing with z-axis rotation as this is what creates the illusion of depth!

Overall, these principles can be applied to both 2D and 3D designs, however, the shorthand for writing changes slightly.

### The Guest Appearance!

Now it is time that I share with you all an explanation for understanding frame of reference, that is by far the best I have heard yet!

"Note that transformations all operate with respect to a *frame of reference*. To best understand this concept, visualize the following scenario:

1. A train is moving along a railroad. This train is moving north, *relative to the Earth*
2. A conductor sits inside the train and tosses an apple. This apple moves up and down, *relative to the train*. In the train’s frame of reference, there is no notion of “north”. With respect to the train, this apple is only moving up and down
3. However, *relative to the Earth*, the apple is actually moving north *and* up and down" (Alvin Wan)...

This explanation is courtesy of Alvin Wan, a CSS master and quite frankly wizard.

## Methods

Now that we know the gist, we can have some fun!

There are numerous methods we can use to achieve different effects, and even more when said methods are combined.

We will start with 2D transform methods:

### Translate()

This method moves an element along the axes based on the input values.

```
div {
  transform: translate(px, px);
  }
```

As a result, this div will move a number of pixels in both the x- and y-axis, or right and upward directions.

### Rotate()

This method rotates a given element, either in a clockwise or counterclockwise direction, based on the input values.

```
div {
  transform: rotate(deg);
  }
```

As a result, this div will be rotated a number of degrees around its origin.

Note: to achieve a counterclockwise rotation, input a negative degree

### Scale()

This method scales a given element, increasing or decreasing it in both horizontal and vertical directions.

```
div {
  transform: scale(X, Y);
  }
```

As a result, this div will be scaled in both horizontal and vertical directions based on the input values, relative to the original size.

Note: the input values can be in decimal, such as 3.5

Note: transform: scale takes care of both horizontal and vertical directions, however, transform: scaleX or scaleY will achieve the same effect for the individual parameters and axis

### Skew()

This method skews an element on either axis based on the input angle.

```
div {
  transform: skew(deg, deg);
  }
```



As a result, this div is skewed a number of degrees along both the x- and y-axis.

Note: transform: skew takes care of both horizontal and vertical directions, however, transform: scaleX or scaleY will achieve the same effect for the individual parameters and axis

### Matrix()

This method is the essential be all end all, as it combines every previously discussed method into one.

```
div {
  transform: matrix(scaleX, skewY, skewX, scaleY, translateX, translateY);
  }
```

As a result, this div is scaled, skewed, and translated in both the x- and y-axis.

Note: as of this example, this is a combination of 2D transforms

## 3D

In order to translate what has since been discussed into the third dimension, we must acknowledge two primary things:

1. The z-axis

2. Perspective

Acknowledging these things in combination with the keyframes rule can result in some truly spectacular 3D animations.

Overall, CSS transforms are really fun and intuitive to use, so get out there and develop!

-----------------------------------------------------------

###### Resources
[CSS Transform Property](https://www.w3schools.com/cssref/css3_pr_transform.asp) /
[CSS 2D Tranforms](https://www.w3schools.com/css/css3_2dtransforms.asp) /
[CSS Transitions and Transforms for Beginners](https://thoughtbot.com/blog/transitions-and-transforms) /
[The noob's guide by Alvin Wan](https://blog.logrocket.com/the-noobs-guide-to-3d-transforms-with-css-7370aafd9edf/)