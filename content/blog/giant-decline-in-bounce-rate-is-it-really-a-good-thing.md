---
title: "Giant Decline in Bounce Rate: Is it Really a Good Thing?"
date: 2016-06-12T19:57:25-06:00
banner: "img/posts/bounce.png"
tags: ["analytics"]
categories: ["blog"]
authors:
  - jeanine
excerpt: "After a redesign website, Google Analytics showed a huge drop in bounce rate. The cause? Duplicating GA tags within my website’s code!"
---

Is it Really a Good Thing? 

**No, probably not.**

In April 2016, I updated a website with a fresh, responsive Magento design in collaboration with Social Ruckus in Bozeman, Montana. There was a noticeable slowing of the websites as most features used AJAX and dynamic loading. Even so, I noticed a huge drop (~50% to 3%) in bounce rate.
<blockquote class="twitter-tweet" data-lang="en">
<p dir="ltr" lang="en">Bounce dropped after releasing RWD--I'm a bit nervous. What other metrics should I look at? <a href="https://twitter.com/hashtag/GoogleAnalytics?src=hash">#GoogleAnalytics</a> <a href="https://t.co/7n2t20kEZE">pic.twitter.com/7n2t20kEZE</a></p>
— Jeanine Schoessler (@satinflame) <a href="https://twitter.com/satinflame/status/731177443826925569">May 13, 2016</a></blockquote>
<script src="//platform.twitter.com/widgets.js" async="" charset="utf-8"></script>

I looked around a bit but couldn’t find any definitive ideas about redesigns correlating to changes in bounce rates. I knew that having a mobile design should actually help but was nervous of such a dramatic change.

Was something set up incorrectly? **Yes—tag implementation!**

Thanks to help from [UI Designer Krista Lacida](https://dribbble.com/kristalacida) I was able to target a second Google Analytics tag being loaded into my code which caused issues with my statistics.

Since removing the second tag, all is back to “normal.” (Though I’d much rather keep the 3% bounce rate!)

* * *

Are you having problems with your Google Analytics, or do you know if you are even tracking your visitors’ actions on your website? Contact me to learn more about implementing Google Analytics, viewing dashboards and setting up recurring reports for your website!