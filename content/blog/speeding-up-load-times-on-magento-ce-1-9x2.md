---
title: "Speeding Up Load Times on Magento CE 1.9x"
date: 2016-07-21T19:37:25-06:00
banner: "/img/banners/speed-james-cawley.jpg"
tags: ["programming", "magento"]
categories: ["blog"]
authors:
  - jeanine
excerpt: "Learn many of the ways to speed up Magento 1.9x website’s performance!"
---
 

While this entry could also be aptly named _OMG How Do I Make Pages Load Faster in Magento?,_ I’ve finally found a solution to speeding up my Magento website that makes me so much less bitter, I can now even think semi-straight. If you’re searching for answers as well–and perhaps not finding adequate solutions–I hope this post will be of value for learning all the different ways to increase your Magento website’s performance!

First, let’s go over the items I did try and what worked. Many of the first items deal with configuring your server install, so be prepared!

If you haven’t yet become versed in Linux and are joining the ranks of well-rounded web developers, check out “[How Linux Works](https://www.amazon.com/dp/1593275676/ref=as_li_ss_tl?pf_rd_p=1944687562&pf_rd_s=lpo-top-stripe-1&pf_rd_t=201&pf_rd_i=0470467010&pf_rd_m=ATVPDKIKX0DER&pf_rd_r=TQF8G6DYXPW9JW1004DV&linkCode=ll1&tag=satinflamedes-20&linkId=a05e6d75dd2a0666c1a3f3a2017034c0),” a guide that covers every useful feature you need to know–gain confidence in the command line!

## The Run Around

Here is a list of all the items I tried. Some may be useful, but many seemed to not even make a dent in site performance.

*   **Grab a Page Load Extension**–Want to know if your page is loading any faster? Check out [Page load time](https://chrome.google.com/webstore/detail/page-load-time/fploionmjgeclbkemipmkogoaohcdbig?hl=en) on Chrome and see how long your page takes each time you load it! The goal is to see those numbers dwindle.
*   **Optimize your images**–Photoshop has the ability to optimize your images for the web. Try it out and save some bandwidth. There are also online tools for optimizing your images such as [TinyPNG](https://tinypng.com/) or [Image Compressor which offers higher limits](https://www.websiteplanet.com/webtools/imagecompressor/)—thanks Lily W. for sharing. Large images do make a big impact on your page load time and may strain your server.
*   **Merge ALL the things**–Can you combine it any further? Can you remove any unused CSS? Yes, you probably can work on cleanup for hours and it still only saves 50kB. Congrats! Your load speed is still the same. (Although, if you’re wondering, merge your JS and CSS files using: System > Configuration > Advanced > Developer)
*   **Compress ALL the things**–If you do a search on “gzip” or “deflate” for Magento, you will find all sorts of walkthroughs. After hours of playing with your Apache modules and .htaccess files, you’ll be an expert in server settings. (However your site will probably be only nanoseconds faster.)
*   **Cache ALL the things?**—_Okay, so this is getting ridiculous now._ Go enable some more modules and check the expiry on your images and files. All good to go? Great job.
*   **Research more**–Check your server memory. Read about Varnish. Research Magento optimization companies and start crying when you realize their own sites don’t load under three seconds either.

At this point, if you are still here, you may be wondering if I actually found some solution to my slow Magento site.

## My Answer: [Full Page Cache](https://mirasvit.com/magento-extensions/full-page-cache.html)

Did you hear the musical echoes of the clouds parting?

This plugin from Magento Connect places magical kittens on your site to remember the queries your users make and keep the results for next time. It installed perfectly for me, and within 15 minutes, [my pages were loading under three seconds](http://optechusa.com/) (down from the 7-9 seconds from before.) On subsequent pageloads, some pages are even loading as fast as .92 seconds. I am by far stunned by this extension–for $149.00 it is worth your time, sanity and development–as well as customer retention–to make this investment in your site. I’m sure you won’t regret it.

I hope to come back in the next few months and share the rise in customer traffic that results from these lower pageload times! Until then, just know that I will be dancing around my website, zipping from page to page, all thanks to Magento’s [Full Page Cache](https://mirasvit.com/magento-extensions/full-page-cache.html).

* * *

Are you struggling with your own Magento Community Edition 1x installation? Do you need updates to your plugins or new features added? [Contact me](/contact/) and let’s chat about your website goals!

* * *

Have you found another method that worked for speeding up your Magento install? Please share!
 