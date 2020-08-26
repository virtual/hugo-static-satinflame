---
title: "Creating Responsive Images in OU Campus"
date: 2020-08-25T19:18:22-06:00 
banner: "img/posts/responsive-images/rwd-images.png"
tags: ["oucampus", "programming", "rwd"]
categories: ["blog"]
authors:
  - jeanine
excerpt: "Responsive images allow you to deliver an optimally sized image to each device--preventing unnecessarily large downloads and potentially speeding up your webpage. In this article, discover how responsive images work and how they can be set up in OU Campus." 
draft: true
---

It's no secret: these past years have seen ever-increasing sizes of images to feature on your school's homepage. Though some designs are now implementing smaller images (and thankfully taking a step back from large carousels), these pages can still pack a punch on your visitor's bandwidth. With over 30% of users likely visiting from mobile devices, it would be ideal that a 480px-wide mobile device only downloads a 480px-wide image instead of the 1200px-wide image that would display for a desktop monitor.

## How responsive images work

Let's take a look at page speed for a site loading a large hero image. 

<figure style="text-align: center">
<img src="/img/posts/responsive-images/network-xl.png" alt="image of network tab desktop loading images">
<figcaption>Load time on desktop: the large hero image (explore-xxl.jpg) takes 1.65 seconds to load.</figcaption>
</figure>


Check image download speeds on your site by using Chrome's Inspect Element > Network tab filtered by Img. With a regular image tag, your visitors will need to download the largest image regardless of which device they're on. Large hero images are typically 300kb-1mb! 

Instead, if provided a <picture> tag using alternative sizes, the webpage can deliver the most appropriate image for each device. For example: a 1200px-wide image (420kb) for desktop or a 480px-wide image (46kb) for mobile.

<figure style="text-align: center">
<img src="/img/posts/responsive-images/network-sm.png" alt="image of network tab desktop loading images">
<figcaption>Load time on mobile: the responsive small hero image (explore-sm.jpg) takes 232 ms (0.23 seconds) to load.</figcaption>
</figure>

Delivering the optimized image can shave off seconds on page load time. Considering that "[forty percent of web users abandon a website if it takes more than three seconds to load](https://omniupdate.com/blog/posts/2018/powerful-seo-for-higher-ed-websites.html)," the time saved could also potentially increase conversions and lower bounce rates!

## Testing responsive images for your next project

Now you know *why* they're great; next, let's go through *how* they are set up!

First, let's look at typical HTML for a `<picture>` element:

```html
<picture>
  <source srcset="image-xl.jpg" media="(min-width: 992px)" />
  <source srcset="image-lg.jpg" media="(min-width: 768px)" />
  <source srcset="image-md.jpg" media="(min-width: 480px)" />
  <img src="image-sm.jpg" alt="the small image defaults for mobile and older devices" width="400" height="380" />
</picture>
```

### The fallback: `<img>`

In the above example, only one of the four images will load--depending on the size of the user's device. It's important to note that the `<img>` element is still present (last) in the list of images. Since this example is designed to be mobile-first, the `<img>` will be shown on mobile devices. It also allows for a fallback for older browsers including Internet Explorer 11. (Yes, it might be a bit blurry, but IE users aren't looking for optimal experiences, are they?) 

Another important reason for including the `<img>` tag is that it will be able to pull in the alt tag description as well as the width and height of the image. Image widths and heights might seem arbitrary, but they're becoming quite important again as we try to address issues of [cumulative layout shift (CLS)](https://web.dev/cls/). The unexpected jumpiness of loading elements on your page may contribute to overall CLS. By ensuring your image has its height and width set, the browser has an idea of how much layout space to save for each image, helping to prevent delayed movement of content or unintended clicks.

### Choosing alternative sizes

Though the `<img>` loads for the smallest device, as device screens get larger, the <picture> element will automatically choose the image that meets the minimum width set in the media query.

For your project, first, determine the optimal sizes for your responsive `<picture>` tag. I would recommend using an [image placeholder API](https://placeholder.com/) that shows image dimensions to better understand when each image is loaded. 

<iframe height="442" style="width: 100%;" scrolling="no" title="Layered Banner with Offset Overlay" src="https://codepen.io/virtual/embed/XWXPVMR?height=442&theme-id=dark&default-tab=html,result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/virtual/pen/XWXPVMR'>Layered Banner with Offset Overlay</a> by Jeanine
  (<a href='https://codepen.io/virtual'>@virtual</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

In the example above, click the zoom factor (1x, 0.5x, and 0.25x) to simulate different devices. Test out your code by resizing your browser window. 

## How to create responsive `<picture>` elements in OU Campus

With the recent addition of Image Size Sets within OU Campus, the ability to create a set of appropriately sized images is easier than ever! 

- Review and set up [image set sizes in OU Campus](https://vimeo.com/353812283) using consistent extension naming (reference the example below)
- [Update XSL](https://github.com/virtual/ou-picture-tag/tree/master/_resources/xsl/_shared) in snippets.xsl and functions.xsl
- [Implement snippet](https://github.com/virtual/ou-picture-tag/blob/master/snippets/ou-build-picture.html) in Editable Region
- Confirm the media queries work for your images
 
### Image size setup

This example uses the following image size set with "crop" setting (note: you can use different resolutions):

| Size   | Suffix | Width  | Height |
|--------|--------|--------|--------|
| Small  | `-sm`  | 480    | 300    |
| Medium | `-md`  | 768    | 480    |
| Large  | `-lg`  | 800    | 1200   |
| XL     | `-xl`  | 1200   | 1200   |

### Snippet usage

Given a normal image placed within the snippet:

```html
<img src="/_resources/images/hero/students-under-trees-sm.jpg" alt="students under trees" width="480" height="300">
```

Using the code provided this example, the picture is set up using Bootstrap's viewports (`992px`, `768px`, `480px`) and outputs the following HTML:

```html
<picture>
  <source srcset="/_resources/images/hero/students-under-trees-xl.jpg" media="(min-width: 992px)">
  <source srcset="/_resources/images/hero/students-under-trees-lg.jpg" media="(min-width: 768px)">
  <source srcset="/_resources/images/hero/students-under-trees-md.jpg" media="(min-width: 480px)">
  <img src="/_resources/images/hero/students-under-trees-sm.jpg" alt="students under trees" width="480" height="300">
</picture>
```

Interested in using image sets to create responsive images using the `<picture>` tag in your OU Campus site? [View my complete code for setting up responsive images in OU Campus](https://github.com/virtual/ou-picture-tag)! If you're not a web developer, [contact me for assistance with implementing snippets or other OU Campus updates](/contact).

&nbsp;

<p class="text-center"><a class="btn btn-template-main" href="https://github.com/virtual/ou-picture-tag"><span class="fab fa-github" aria-hidden="true"><span class="sr-only">GitHub</span></span> View this project on GitHub</a></p>