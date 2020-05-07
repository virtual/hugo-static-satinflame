---
title: "Adding Bar Graphs using Highcharts in OU Campus"
date: 2018-09-02T18:47:58-06:00
banner: "img/banners/oucampus-highcharts-1024x585.png"
tags: ["oucampus"]
categories: ["portfolio"]
authors:
  - jeanine
excerpt: "If you find yourself often updating handfuls of bar chart images, look into this solution to save you time and to help deliver your information more semantically. Using the Highcharts JS library, OU Campus users can now easily modify the bar chart data as needed."
---

In this example, the HTML table is transformed using the [Highcharts library](https://www.highcharts.com/products/highcharts/)—it is free for non-profits, so [go grab a Highcharts Non-commercial license](https://shop.highsoft.com/highcharts/).

On your page, include the Highcharts library file as well as your customized JS—specific to this type of bar graph setup. In your file at `/_resources/ou/editor/wysiwyg.css` or similar, add the following CSS to show the table in edit mode only:

```css
#datatable.sr-only {
    display: block !important;
    position: relative;
    height: auto;
    width: auto;
    overflow: auto;
    clip: auto;
}
```

Here's an example of how the Highcharts table looks using page edit view within OU Campus:

Level    | Salary
--------|------
PGY—1     | 58109
PGY—2     | 61344
PGY—3     | 63319
PGY—4     | 65873 

A working sample of Highcharts using an HTML table and JS:

<p data-height="265" data-theme-id="0" data-slug-hash="yqYbJx" data-default-tab="html,result" data-user="virtual" data-pen-title="Bar Graph" class="codepen">See the Pen <a href="https://codepen.io/virtual/pen/yqYbJx/">Bar Graph</a> by Jeanine (<a href="https://codepen.io/virtual">@virtual</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

View a live version I implemented on [Morehouse School of Medicine's GME Salary webpage](https://www.msm.edu/Education/GME/OBGYNResidencyProgram/SalaryandBenefits.php).

__Additional customization notes:__

- I had to use an en dash (—) in the label with the numbers, otherwise Highcharts transformed this data into a date label
- With the non-commercial license, you can remove the Highcharts logo by setting `credits: { false }`
- For a variable number of columns, add an array of colors in the JavaScript file; it will loop through the colors as needed

----

Not quite sure how to implement this vertical bar graph on your own site? <a href="/contact/">Contact me to learn more</a>.