---
title: "OU Campus Components vs. Snippets"
date: 2019-07-03T11:20:06-06:00 
banner: "img/posts/component-snippet/blog-components-snippets.jpg"
tags: ["bootstrap4", "omniupdate", "programming", "rwd"]
categories: ["portfolio", "blog"]
authors:
  - jeanine
excerpt: "Components and snippets can often be used interchangeably for the same purpose, however there are number of difference between the two. When should you choose a component over a snippet, or vice versa? Where can each be used and how are they managed?" 
draft: true
---

For years, managing advanced features within OU Campus has been handled using a variety of snippets and assets. As a reminder, snippets come in two versions: 1) an inserted chunk of code or text that will be manually edited and managed and 2) table-transformations, which will be the majority of the examples for this article. Assets, similarly, can be used to manage a chunk of code, text, form, or collection of photos within a page; however, since each asset is centrally updated, every instance of one asset points to one source. 

If you had wanted to customize a feature specific for each use, previously you would have only had snippets as an option. Recently, though, OmniUpdate released a feature called components. Components and snippets can often be used interchangeably for the same purpose, however there are number of difference between the two. When should you choose a component over a snippet, or vice versa? Where can each be used and how are they managed? 

In this article, we will dive into specific use cases for both components and snippets, so you can identify which feature will be more suited to your needs within OU Campus.


## Inserting and Modifying Content

### User Interface Examples
Let's start out by comparing the typical view of snippets and components for your end-users.

**Snippet**

![Editing snippet](/img/posts/component-snippet/edit-snippet.jpg)

**Component**

![Editing component](/img/posts/component-snippet/editing-component-no-preview.jpg)

![Editing component](/img/posts/component-snippet/edit-component.jpg)

It might be worth mentioning that if you have preview turned off, it may prove difficult to figure out which component you want to edit when you're using multiple in the same edit region:

![Editing component](/img/posts/component-snippet/editing-component-no-preview-multi.jpg)

Further, if you do have preview component turned on, users may be confused by the preview. There are options users may attempt to edit when in the Edit Region mode (instead of the Edit Component view)--such as editing the image source or formatting text from the WYSIWYG toolbar--which won't save when completed. 

![Editing component](/img/posts/component-snippet/editing-component-table-transform.jpg)
 
 
> Components may be best for standalone environments; however snippets are preferable when users need to access features of the editable region--such as referencing link anchors, applying classes or inserting an additional snippet.

### Linking Capabilities

One tool that is often useful is the link tool in OU Campus. It allows you to link to a page or anchor. However, snippets and components work quite differently.

When editing a snippet, you'll see options to add links and anchors that are available in the same Edit Region your snippet was placed in. In this example, `#schedule` is an available anchor as shown in the Link tool.

![Editing component](/img/posts/component-snippet/link-anchor-snippet.jpg)

Components, on the other hand, are edited in a separate modal window. They do not have the option to link to anchors within the region it was placed. However, you can still use the less-powerful link options of the minimal WYSIWYG (often found in the MultiEdit regions).

![Editing component](/img/posts/component-snippet/link-anchor-component.jpg)
 
### Page Preview

On save, both components and snippets should show indentical to how they will publish (unless your snippet/component rely on server-side code to run).


**Snippet**

![Editing component](/img/posts/component-snippet/preview-snippet.jpg)

**Component** 

![Editing component](/img/posts/component-snippet/preview-component.jpg)



### How does it show in source code? 

**Snippet:**

```html
<table class="ou-alert-default">
<thead><tr><th>Alert (Blue)</th></tr></thead>
<tbody><tr><td>
<p>The campus will be closed due to extreme weather conditions.</p>
</td></tr></tbody>
</table>
```
**Component:**

```js
~[com[2460 1 2{ "version": 2, "data": {"ca2ee8508fabe92a74fe08ca0f0b9018":"info","7cf226fac04bfa4a7b6ce21f6d58f80a":"&lt;p&gt;The campus will be closed due to extreme weather conditions.&lt;/p&gt;"}}]]~ 
```

As you can see from the examples above, if you were to do a content inventory, or need to do a Find/Replace, components are a bit more obfuscated than snippets.

That being said, there seems to be some information in these component calls:
```js
~[com[<COMPONENTID> <NUMBER OF ELEMENTS> <LAUNCH VERSION>{ "version": 2, "data": {"ca2ee8508fabe92a74fe08ca0f0b9018":"info","7cf226fac04bfa4a7b6ce21f6d58f80a":"&lt;p&gt;The campus will be closed due to extreme weather conditions.&lt;/p&gt;"}}]]~
```




## Maintainability and Creating Changes

Both snippets (using table-transformations) and components can use XSLT to create different designs based on logic. Often, this will mean adding a new section or modifying selected features in XSLT as well as within the snippet or component itself. Now, what happens when you make these changes to related XSLT? Unlike pages using assets, pages using snippets and components will need to be manually republished for the XSLT-based changes to reflect on your website. 

**Snippet:**

![Editing component](/img/posts/component-snippet/modify-snippet.jpg)

**Component:**

![Editing component](/img/posts/component-snippet/modify-component.jpg)

OU Campus documentation shares the following:

*"If an existing component is launched with changes that are significantly different from how it exists on pages (i.e., adding a new required element), then the extant instances of the component will not change until the next time someone edits the component content on a page. Then, the newest version will be used. For minor changes (such as changes in helper text), the components will be updated automatically on launch."* 

## Where can each be used?

Knowing the limitations of the functionalities is one piece, but there is another important aspect of understanding if a component works for your situation: where will it be placed? Currently, assets and MultiEdit WYSIWYG regions do not include the option to insert a component.

Region | Snippets | Components 
--- | --- | ---
Page Editable Region | x | x
MultiEdit WYSIWYG Region | x 
Source Code Asset | x  

![Editing component](/img/posts/component-snippet/asset-use-snippet.jpg)

## Permissions

Follow permissions? Folder links?

Add to page?
Edit in page?

Components: 

*"For the File and Image Chooser elements, select whether the user cannot navigate out of the current folder to look for files."*

*"Access lets you select which group the component is available to. This restricts which users can place the component on a page, but doesn't affect who can edit the component on a page."*


Snippets
Image embedded

## Considerations

* Where will your feature be used?
* Who will need access to it?
