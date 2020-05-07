---
title: "Shoreline Community College Redesign"
date: 2019-02-27T10:23:38-07:00
banner: "img/posts/shoreline/shoreline.png"
tags: ["bootstrap4", "oucampus", "programming", "rwd", "Sass"]
categories: ["portfolio"]
authors:
  - jeanine
excerpt: "With user feedback from students, a comprehensive Identity Guideline, and a fresh web design, Shoreline Community College updated their website with new OU Campus templates and snippets." 
---

In January 2018, Shoreline unveiled an updated Identity Guideline which I implemented from the original PDF into an [interactive Identity Guidelines webpage](https://www.shoreline.edu/communications-marketing/identity-guidelines/). (As an reminder, it is a best practice—as [noted by Jakob Nielsen](https://www.nngroup.com/articles/pdf-unfit-for-human-consumption/)—to use HTML instead of PDF for online presentations.) In addition to structuring the content to be responsive regardless of device, I added hex codes to each color block and made them clickable so a user could easily copy the color codes to their clipboard. An interesting challenge developed in implementing similar functionality for the Outlook signature block. Unfortunately, browsers on Macs often failed to maintain the formatting of the text, so we decided to also add in an option to open it as Word's Rich Text Format (RTF) and copy the formatted text directly from Word into Outlook.
<div class="figstack">
<a data-fancybox="gallery" href="/img/posts/shoreline/identity1.png">
  {{< figure src="/img/posts/shoreline/identity1.png" title="Shoreline Community College Redesign Identity Guidelines" >}}
</a>
<a data-fancybox="gallery" href="/img/posts/shoreline/identity2.png">
  {{< figure src="/img/posts/shoreline/identity2.png" title="Showing the brand colors with the option to copy the hex color to the clipboard" >}}
</a>
<a data-fancybox="gallery" href="/img/posts/shoreline/identity3.png">
  {{< figure src="/img/posts/shoreline/identity3.png" title="An Outlook signature guideline with option to copy formatted text" >}}
</a> 
</div> 


With the school's updated guidelines launched, Shoreline Community College's team then worked with [Andy Fitzgerald for User Experience (UX)](https://www.andyfitzgeraldconsulting.com/) and [Joe Shoop for web design](http://joeshoop.com/). Months later, the design was ready for development. For the handoff, Joe exported his complex Sketch file into a service called Zeplin. This powerful tool lets a developer look at the typography, shapes and layout to immediately see the various style properties, e.g. font-family information, border radius and sizes.  


## Development

We decided to use Bootstrap 4 for development as it incorporates Sass (instead of LESS) and offered extensibility with its components out of the box. This was also the first project I developed using [Jigsaw](https://jigsaw.tighten.co). In addition to the modern conveniences of compiling Sass, viewing live changes during development, and being able to run the code locally using Vagrant, Jigsaw also offers small building blocks that mimic the transformations of snippets or components found in OU Campus. In turn, this similarity makes implementing the code more seemless as it shows the logic needed for the XSLT.


- [View demo](https://virtual.github.io/shoreline/) | [Snippets](https://virtual.github.io/shoreline/v3/)
- [View website](https://www.shoreline.edu)


> “We love working with you and are so happy that you have this opportunity. To all who don’t already know, Jeanine is the best web person you can find. Beyond the web skills, she’s got communication and project management skills. I don’t know what we would do without Jeanine.”  
> <small>Adam Staffa, Shoreline Community College</small>