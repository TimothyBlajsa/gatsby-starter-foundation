---
template: blog-post
title: "CSS Photo Booth: Fun With Filters"
slug: css_photo_booth_fun_with_filters
date: 2020-10-12 14:38
description: CSS Filters
featuredImage: /assets/peter-stumpf-fhzepxtti_y-unsplash.jpg
---
# Greetings!

We have finally made it to the end of our path of text and typography (for now) and have thus entered a new journey of CSS trickery and fun!

Get ready for in-text movie magic! I'll explain what I mean in a little bit.

# CSS Filters:

![](/assets/peter-stumpf-fhzepxtti_y-unsplash.jpg)

First of all, we have to discuss the pure essence of this topic; CSS filters. 

WHAT IS A CSS FILTER? you may ask

A CSS filter is a relatively new, and highly useful property for things such as images and graphics. In a non-developer language, this allows essentially in-text filters overlayed on top of our images similar to how you can apply a filter on your phone or in an image editor like Photoshop.

But we ARE developers, so let's dive deeper into how to achieve such effects.

# Types of Filters:

Prior to playing in the land of CSS, we should discuss the variations of the filter property and what exactly it does. 

The property itself is not tampering with the original image, but rather influencing the way the image is rendered, its background, the borders of the image, etc. FOR THE SAKE OF SANITY AND READER ATTENTION WE WILL NOT BE DISCUSSING INTERPOLATION IN THIS ARTICLE, but in cliffnotes fashion, it is the guessing of a new value based on two predetermined values.

Here is a quick example of syntax:

```
HTML
<img width="250" class="name" src="http://sourcename.com
" />



CSS
.name {
    filter:...
    }
```

It's that easy!

But what can you put in the filter property? I am glad you asked!

## Blur:

My favorite of the bunch is the application of a Gaussian blur to an image.

```
filter: blur(px);
```

This form of filter depends on a radial effect, meaning the larger radius, or pixel size, the more blurred the final render will be. If you play around, you may be able to achieve a depth of field look (perhaps a topic for another article).

## Brightness:

This variation can make an image appear brighter or darker via the application of a linear multiplier to said image. 

```
filter: brightness(% or 0-1);
```

The percentage range spans from 0 to 100 or in decimal 0 to 1: darkest to unchanged.

To make the image brighter, simply input a value over 100.

## Drop-Shadow:

This variation of filter applies a shadow underneath the image, giving a lifted or multidimensional effect to the image.

```
filter: drop-shadow(px px);
```

The two values specify the offset of the shadow in both X and Y directions.

Alternatively, you can also input a blur-radius and spread-radius in px alongside a shadow-color.

## Grayscale:

![](/assets/renee-zernitsky-clutoqqyaf4-unsplash.jpg)

Is it grey or gray?

```
filter: grayscale(0 - 1 or 0 - 100%);
```

This variation of the filter allows the image to appear in various degrees of "grayness" either in decimal or percentage (0 - 1 or 0 - 100: no change to complete grayscale).

## Contrast:

Similar to grayscale, you can also adjust levels of contrast within the image. 

```
filter: contrast(%);
```

Input ranges from a percentage of 0 to 100, translating between decreased contrast to no change and increased contrast.

## Opacity:

This variation of the filter changes the transparency level of the original image, ranging from not visible to solid. 

```
filter: opacity(0 - 1 or %);
```

The higher the value inputted the more solid the image is.

## Saturation:

This method of filtering allows for the adjustment of the image saturation or intensity.

```
filter: saturate(0 - 1 or %);
```

The range spans from desaturation to saturation; however, any value exceeding this range can be supersaturated.

## Hue:

The filter property also allows for the adjustment of hues in an image.

This is achieved by presenting a degree of rotation in reference to the color wheel.

```
filter: hue-rotate(# turns or deg);
```

There is technically no range in which you can input whatever you want, however, knowledge of the circle shows that you will eventually just return to a previous value in terms of final effect, thus you truly only have 360deg to play with.

## Inversion:

If you want to invert the colors of an image, you can do that too!

```
filter: invert(%);
```

The range for input spans from 0 to 100: unchanged to complete color inversion.

## Sepia:

![](/assets/ajeet-mestry-ubhpoihnazm-unsplash.jpg)

SEPIA SEPIA SEPIA

This is by far my favorite of all of these filters! It even trumps blur.

```
filter: sepia(%);
```

This range spans from no change to the original image to complete sepia glory!

That sure was alot of filters! I'm sure you noticed a trend in input types, mainly percentage values.

# Use Case:

As always, we have arrived at the big question, WHY would I use CSS filters?

At face-value, the application seems fairly subjective. However, the applications are quite vast.

1. SVG FILTERS

The first and prominent use case for the filter property is with SVG files. 

This can be a quick way to add an effect or invoke a tone with a visual while not losing any detail due to the scalability of the Vector Image.

2. CUSTOMIZATION

The most obvious of the two, is the wide expansion of customization that comes alongside these tools. If you haven't guessed by now, you can apply multiple filters at the same time, yielding truly unique and spectacular effects!

An example of an old-timey, out of focused cat image would look something like this:

```
filter: sepia(1) grayscale(.4) blur(1px);
```

![](/assets/screen-shot-2020-10-12-at-4.02.21-pm.png)

The applications are endless! Now it is time for you to go and experiment, the best way to increase your CSS skills is to practice what you know!

\*Note that this is considered an unofficial specification and only has support from certain browsers

- - -

###### Resources:

Check out these cool sources!

[MDN Web Docs: filter](https://developer.mozilla.org/en-US/docs/Web/CSS/filter) /
[CSS-Tricks: filter](https://css-tricks.com/almanac/properties/f/filter/) /
[CSS Filters Examples and Quick Demos](https://alligator.io/css/css-filter-examples/) /
[CSS3 Filters](http://css3.bradshawenterprises.com/filters/)