---
title: "Approving Pages in OU Campus"
date: 2020-01-06T12:42:18-07:00 
banner: "img/posts/approvals-oucampus/omniupdate-approve-submissions.jpg"
tags: ["oucampus", "administration"]
categories: ["blog"]
authors:
  - jeanine
excerpt: "If you’re new to using OmniUpdate's OU Campus for updating and approving pages for your school's web site, you may be wondering which items need to be checked when reviewing submissions. Learn tips for identifying changes as well as eight common issues that may occur in submitted web pages." 
draft: true
---


## Getting started

When you first open up a submitted web page, you may be wondering what is different between the submission and the live versions. During user training, encourage your content managers to write descriptions that outline what they've changed.

<figure style="text-align: center">
<img src="/img/posts/approvals-oucampus/submit-for-approval.jpg" alt="A submit for approval screen showing a complete description of the changes made">
<figcaption>Encourage content managers to write a clear subject and message detailing what content has changed.</figcaption>
</figure>


Before you begin reviewing, [save a new version of the staged page](https://support.omniupdate.com/learn-ou-campus/pages-files/review/versions.html) with a description "As submitted by *user*,"--this way, you can revert or compare your changes to the original submission.
 
<figure style="text-align: center">
<img src="/img/posts/approvals-oucampus/submit-for-approval-save-version.jpg" alt="Save version commit message screen">
<figcaption>Save a version prior to reviewing and fixing page errors.</figcaption>
</figure>


To identify the submitted changes, view the versions of the page and select *Compare to Live*. If you are comfortable with viewing code, it may be easier to identify changes using the Source view. Otherwise, try viewing the page differences as shown in the Page view to get a clearer understanding of what content has changed.
<figure style="text-align: center">
<img src="/img/posts/approvals-oucampus/compare-live.jpg" alt="A list of recent versions next to a 'Compare to Live' button">
<figcaption>Once you've saved a version of the file, check the Compare to Live button to see the changes.</figcaption>
</figure>
<div class="row">
  <div class="col-sm-12 col-md-6"><figure style="text-align: center">
<a href="/img/posts/approvals-oucampus/compare-live1.jpg"><img src="/img/posts/approvals-oucampus/compare-live1.jpg" alt="A preview of the web page showing green text for additions"></a>
<figcaption>The comparison is available as web content.</figcaption>
</figure></div>
  <div class="col-sm-12 col-md-6"><figure style="text-align: center">
<a href="/img/posts/approvals-oucampus/compare-live2.jpg"><img src="/img/posts/approvals-oucampus/compare-live2.jpg" alt="A preview of the source code changes showing green text for additions"></a>
<figcaption>The comparison can also be viewed in source code.</figcaption>
</figure>
</div>
</div>

--------

The following are some common issues that may need to be addressed before approving updates submitted by your content managers. 

## Semantic issues

### Incorrect heading levels

Sometimes you may find text styled to look different from its original appearance. When this occurs, determine if this styled text should be using a heading tag instead. Heading levels on the web work similarly to heading levels in Microsoft Word and provide a hierarchy to your content. They are useful as they provide search engines a way to tell the important topics of each of your web pages. Screen readers can also help visitors navigate by jumping directly to a heading level. Headings should be used without skipping levels, and you should always have one—and only one—Heading 1 per page. 

If text should be a heading, remove any erroneous styles and then apply the correct heading level using the WYSIWYG toolbar. If you need additional configuration to the default styles of headings, work with a developer to update your heading styles globally to match your brand guidelines. This will encourage content managers to use the default headings, and it will ensure they look consistent throughout your website. 

<figure style="text-align: center">
<img src="/img/posts/approvals-oucampus/change-heading.jpg" alt="A list of headings are available in the WYSIWYG toolbar">
<figcaption>While the cursor is within your text, change the heading level using the toolbar.</figcaption>
</figure>

 
If the styled text should not be a heading, consider if the style is necessary. Having a brand guideline is helpful when determining if content managers should modify any styles on a page. To clean up styles on content, select the areas on the page and click the Clear Formatting icon. You can then bold and italicize as needed using buttons in the WYSIWYG toolbar. 
 
<figure style="text-align: center">
<img src="/img/posts/approvals-oucampus/clear-formatting.jpg" alt="Selected text that will be acted upon using the 'Clear Formatting' button">
<figcaption>To clear formatting or inline styles, select the text you want to clean up and click the Clear Formatting button in the toolbar.</figcaption>
</figure>

The [OU Insights report tool](https://support.omniupdate.com/learn-ou-campus/modules/ou-insights.html)--a premium module available as an add-on to OU Campus--can be configured to check for correct heading levels. 

Consider [reviewing toolbar settings for your users](https://support.omniupdate.com/learn-ou-campus/administration/setup/toolbars.html), and only allow admin users to update font families, colors and styles.

### Overused underlines

When reviewing text styles, be sure to avoid underlined text. [Keep underlined styling specific to links only](https://www.nngroup.com/articles/guidelines-for-visualizing-links/), and this will remove the cognitive load of users trying to understand if the text is linked or simply underlined. Instead of underlining for emphasis, consider using bold or italics text for important information.

### Too much space

Often you may find additional empty lines or content that includes handfuls of hard-coded space. Unfortunately, these empty spaces cause issues when viewing this content on a mobile device.  Content that may line-up well on a large monitor may look jumbled and disorganized on a phone. In these cases, consider if you should align the content using a 2-, 3- or 4-column snippet that automatically stacks content on mobile. If the information is table data and should be presented in a table format, insert a table and move the content into the cells accordingly. 

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

Though the link-checker tool in OU Campus works well, sometimes new content managers may be unfamiliar with how it functions. Often, users may change the text of a contact's email address but not know they need to modify the link as well. Be sure to check that all email links are pointing to the correct address by hovering over the link in preview mode. If the link is incorrect or outdated, update the address in the link editor.
 
<figure style="text-align: center">
<img src="/img/posts/approvals-oucampus/link-difference.jpg" alt="Hovering over the text information actually links to the admissions department's email">
<figcaption>While in preview, hover over email links to ensure the link matches the text displayed.</figcaption>
</figure>

Similarly, sometimes users may add new links leading to external pages; these links must begin with 'http' or 'https'; otherwise, they will be broken. When approving, run the link-checker option on the menu to validate page links.

## Unusable mobile views

Although content managers are often using their desktop computers to update pages, over 40% of visits to your site may come through mobile or tablet devices. Resize your screen to see how the content wraps for smaller screen widths. If the content isn't designed to work responsively, consider adding new snippets to your OU Campus install—including 2-, 3- or 4-column snippet that stacks content on mobile.

## Accessibility issues

As you are aware, accessibility is an important part of sharing your information with your visitors. In addition to the updates to headings (above), there are often a couple of other important items that may need to be addressed:

### Inaccessible or unnecessary PDFs

If a content manager adds a link to a new PDF, consider if the information within the PDF could instead reside on a web page. HTML content on web pages can be better parsed by screen readers and search engines, and it is typically easier to view on mobile devices. As a bonus, if small changes are needed in the future, HTML content can be easily modified; these changes can then be tracked using version control. 

If you determine that the information cannot be converted to web content, make sure that the PDF is accessible. Add descriptions to all images (or mark them as decorative) and ensure text is selectable and legible. For example, if a table has been pasted as an image into a PDF, that information is inaccessible. Ask your designers to recreate the table within the PDF without using an inserted graphic.

### Missing or poor image descriptions

As always, review the alt (description) field for each image. Image titles can be helpful when a user doesn't know what clicking a link will do, but otherwise, all alternative text should be placed in an alt field. When developing description content, consider what one might type to find this image using a Google search. If the image contains important text, type it out in the description. Don't include the words "logo of" or "image of" in alternative text. Screen readers can automatically detect when they share a description of an image.

## In summary

- Save the submitted version and compare it to the live page
- Check the heading levels, ensure styles are semantic, and remove erroneous white-space
- Check that links are not broken and remember displayed text does not necessarily match its link
- Resize your screen to preview what the content looks like on mobile devices; use responsive snippets for advanced layouts
- Check images and linked PDFs for accessibility—often, the content in a PDF can be moved into a new web page

If you're looking for help with approving pages (possibly while you're out taking that much-needed vacation!), updating your global heading styles or developing responsive snippets for content layouts, [contact me](/contact/) and let's see if your project would be a good match.