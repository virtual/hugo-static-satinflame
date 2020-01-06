---
title: "Approving Pages in OU Campus"
date: 2020-01-06T12:42:18-07:00 
banner: "img/posts/approvals-oucampus/omniupdate-approve-submissions.jpg"
tags: ["oucampus", "administration"]
categories: ["blog"]
authors:
  - jeanine
excerpt: "If you’re new to using OmniUpdate's OU Campus for updating and approving pages for your school's web site, you may be wondering which items need to be checked when reviewing submissions. The following are some common issues that may need to be addressed before approving updates submitted by your content managers." 
draft: true
---


## Unsaved page history

When you first open up a submitted web page, you may be wondering what is different between the submission and the live version. During user training, encourage your content managers to write descriptions that outline what they've changed.

<figure style="text-align: center">
<img src="/img/posts/approvals-oucampus/submit-for-approval.jpg" alt="A submit for approval screen showing a complete description of the changes made">
<figcaption>Encourage content managers to write a clear subject and message detailing what content has changed.</figcaption>
</figure>


Before you begin reviewing, [first save a new version](https://support.omniupdate.com/learn-ou-campus/pages-files/review/versions.html) with a description "As submitted by *user*,"--this way, you can revert or compare your changes to the original submission.
 
<figure style="text-align: center">
<img src="/img/posts/approvals-oucampus/submit-for-approval-save-version.jpg" alt="Save version commit message screen">
<figcaption>Save a version prior to reviewing and fixing page errors.</figcaption>
</figure>


To identify the submitted changes, view the versions of the page and select *Compare to Live*. If you are comfortable with viewing code, it may be easier to identify the changes the user has made using code. Otherwise, try viewing the page differences as shown in OU Campus. These should give you a clear understanding of what content has changed.
<figure style="text-align: center">
<img src="/img/posts/approvals-oucampus/compare-live.jpg" alt="A list of recent versions next to a 'Compare to Live' button">
<figcaption>Once you've saved a version of the file, check the Compare to Live button to see the changes.</figcaption>
</figure>
<div class="row">
  <div class="col-sm-12 col-md-6"><figure style="text-align: center">
<a href="/img/posts/approvals-oucampus/compare-live1.jpg"><img src="/img/posts/approvals-oucampus/compare-live1.jpg" alt="figalt"></a>
<figcaption>The comparison is available as web content.</figcaption>
</figure></div>
  <div class="col-sm-12 col-md-6"><figure style="text-align: center">
<a href="/img/posts/approvals-oucampus/compare-live2.jpg"><img src="/img/posts/approvals-oucampus/compare-live2.jpg" alt="figalt"></a>
<figcaption>The comparison can also be viewed in source code.</figcaption>
</figure>
</div>
</div>
 

## Semantic issues

### Incorrect heading levels

Often, you might find text bolded, underlined, with text enlarged and the color changed. When this occurs, determine if this should be a header instead. If you aren't already familiar with headers, heading levels on the web work similar to heading levels in Microsoft Word and provide a hierarchy to your content. They are useful as they provide search engines a way to tell the important topics of each of your web pages. Headings also allow users using screen readers to directly jump to a heading level, similar to how a user might visually scan headers on a page to "jump" to the section they want to read more about. Headings should be in order without skipping levels, and you should always have one—and only one—H1 per page. 

If text should be a heading, remove any erroneous styles and then apply the correct heading level using the WYSIWYG toolbar. If you are not happy with the style of your headings, you should work with a developer to update your header styles globally to match your brand guidelines. This will encourage users to use the headings and ensure  headings look consistent throughout your website. 

<figure style="text-align: center">
<img src="/img/posts/approvals-oucampus/change-heading.jpg" alt="A list of headings are available in the WYSIWYG toolbar">
<figcaption>While the cursor is within your text, change the heading level using the toolbar.</figcaption>
</figure>

 
If the styled text should not be a heading, consider if the style is necessary. Having a brand guideline is helpful when determining if content managers should modifying the styles per page. To clean up styles on text, select the text on your page and then click the erase formatting icon. You can then bold and italicize using the Bold and Italics tool in the WYSIWYG toolbar as needed. 
 
<figure style="text-align: center">
<img src="/img/posts/approvals-oucampus/clear-formatting.jpg" alt="Selected text that will be acted upon using the 'Clear Formatting' button">
<figcaption>To clear formatting or inline styles, select the text you want to clean up and click the Clear Formatting button in the toolbar.</figcaption>
</figure>

The [OU Insights report tool](https://support.omniupdate.com/learn-ou-campus/modules/ou-insights.html)--a premium module available as an add-on to OU Campus--can be configured to check for correct heading levels. Also consider [reviewing toolbar settings for your users](https://support.omniupdate.com/learn-ou-campus/administration/setup/toolbars.html), and only allow admin users to update font families, colors and styles.

### Overused underlines

When reviewing text styles, be sure to avoid underlining in text. Underlines have denoted links for over 20 years, and the trend is not leaving anytime soon. [Keep underlined styling specific to links only](https://www.nngroup.com/articles/guidelines-for-visualizing-links/), and this will remove the cognitive load of users trying to understand if the text is linked or simply underlined. Instead of underlining for emphasis, consider using bold or italics text for important information.

### Too much space

Often you may find additional empty lines or content that includes handfuls of hard-coded space. Unfortunately, these empty spaces cause issues when viewing the same content on a mobile device.  Content that may line up well on desktop will look jumbled and disorganized on a phone. In these cases consider if you can align the content using a 2-, 3- or 4-column snippet that stacks content on mobile. If the information is table data that should be presented in a table format, insert a table and move the content into the cells accordingly. 

If you have access to the Source of the page, consider performing these actions prior to approving a page. 

1. Find & replace `<p>&nbsp;</p>` with an empty input—this will remove any empty lines.
2. Then find & replace `&nbsp;` with a single space—multiple spaces in HTML will only show one space, whereas multiple hard-coded spaces (`&nbsp;`) will display all hard-coded spaces.

## Spelling errors

In addition to the spell-checking functionality offered in OU Campus, consider installing the free Grammarly plugin. [Grammarly often finds spelling and grammar issues](https://app.grammarly.com/) that might otherwise get overlooked—such as duplicated words.


<figure style="text-align: center">
<img src="/img/posts/approvals-oucampus/publish-spellcheck2.jpg" alt="Publish undergraduate.pcf Final Check options include Spelling checks">
<figcaption>When submitting a page to be published, use the Spelling validation to check for misspellings.</figcaption>
</figure>

 

<figure style="text-align: center">
<img src="/img/posts/approvals-oucampus/publish-spellcheck3.jpg" alt="Grammarly showing the word 'fpr' should be 'for'">
<figcaption>Grammarly, an alternate tool for checking spelling and grammar, can identify misspellings and recommend corrections.</figcaption>
</figure>

## Broken or incorrect links 

Though the link-checker tool in OU Campus works well, sometimes new content managers may be unfamiliar with how it functions. Often, users may change the text of an email address for an update to a contact but not modify the link of the content itself. Be sure to check that all email links are pointing to the same address when you hover over the link in preview mode. If not, update the address in the link editor.
 
<figure style="text-align: center">
<img src="/img/posts/approvals-oucampus/link-difference.jpg" alt="Hovering over the text information actually links to the admissions department's email">
<figcaption>While in preview, hover over email links to ensure the link matches the text displayed.</figcaption>
</figure>

Similarly, sometimes users may add new links leading to external pages; it is important that these links include http or https at the beginning of the URL; otherwise they may be broken. When approving, run the link checker option on the menu to double-check the validity of links on the page.

## Unusable mobile views

Although content managers are often using their desktop computers to update pages, over 40% of of visits to your site may come through mobile or tablet devices. Resize your screen to see how the content wraps for smaller widths. If the content isn't designed to work responsively, consider adding new snippets to your OU Campus install—including 2-, 3- or 4-column snippet that stacks content on mobile.

## Accessibility issues

As you are aware, accessibility is an important part of sharing your information with your visitors. In addition to the updates to headings (above), there are often a couple of other high-level items that may need to be addressed. 

### Inaccessible or unnecessary PDFs

If a content manager adds a new PDF, consider if this PDF information could instead live on a web page. The content on HTML pages is better parsed by screen readers, search engines and easier to view on mobile devices. As a bonus, if there are small changes in the future, you will be able to easily modify text and also have a record of the changes in version control. 

If you determine that the information cannot be instead placed directly as web content, make sure that your PDF is accessible. These items include adding descriptions to all images (or marking them as decorative) and making sure all text is selectable and legible. If a table has been pasted as an image into a PDF, that information is inaccessible. Ask your designers to recreate the table within the PDF without using an inserted graphic.

### Missing or poor image descriptions

As always, double check your image alt (descriptions). Titles can be helpful when a user doesn't know what clicking a link will do, but otherwise, all alternative text should be placed in a description/alt field and not in the title tag for an image. When writing the text, think about what one might type to find this image in a Google search. If you're using text in the image, type out the text of the image in the description. Don't include the word "logo of" or "image of" in your alternative text. Screenreaders are smart enough to know that they are sharing a description of an image.

## In summary

- Save the submitted version and compare it to the live page
- Check the heading levels, ensure styles are semantic, and remove erroneous white-space
- Check that links are not broken or outdated, and remember displayed text does not necessarily match its link
- Resize your screen to preview what the content looks like on mobile; use responsive snippets for advanced layouts
- Check images and linked PDFs for accessibility—often, the content in a PDF can be moved into a new web page

If you're looking for help with approving pages (possibly while you're out taking that much-needed vacation), updating your global heading styles or developing responsive snippets for content layouts, [contact me](/contact/) and let's see if your project would be a good match.