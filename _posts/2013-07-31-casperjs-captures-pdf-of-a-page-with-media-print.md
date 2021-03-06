---
title: CasperJS captures PDF of a page with @media print
layout: post
date: '2013-07-31 00:00:27 -0700'
type: post
parent_id: 0
published: true
status: publish
categories:
- Web Development
tags: []
meta:
  _edit_last: 1393113
  _publicize_pending: 1
  publicize_twitter_user: zocoi
  _wpas_done_31552: 1
  _publicize_done_external: a:1:{s:7:"twitter";a:1:{i:19440333;b:1;}}
  geo_public: 0
  _wpas_skip_1907398: 1
  _wpas_skip_31552: 1
author:
  login: mephis1987
  email: mephis1987@gmail.com
  display_name: Hung Dao
  first_name: ''
  last_name: ''
---

> TL;DR: Unlike capturing screenshot, the way CasperJS renders PDF of a page is similar to "Cmd+P" printing out as PDF. It takes consideration of @media print. You can take the advantage to have different look and feel for your PDF by tweaking the CSS.

So I have a feature-rich one page web app built with Backbone rendering beautiful info-graphics and reports. I got a bigger challenge of capturing those graphics and send them to customers.

I don't want to use our minimal backend for generating PDF since it does almost nothing beside serving the assets. Also the second reason is to reuse complex Backbone views and templates already written for the frontend.

This sounds like a perfect job for headless Webkit engine, PhantomJS and CasperJS. CasperJS renders the page (or partially), waits for DOM and JS successfully executed and finally generates the PDF.

I got 2 problems with this approach.

At first I got a weird PDF which CSS wasn't loaded. It turns out that there is no equivalent CSS for print media and PhantomJS uses it to print as PDF

The second problem is some graphs was cut in half between pages. Thanks to @media print, I can set different look and feel for the PDF including

```
@media print  
{  
section {page-break-before:always}  
}  
```

which breaks every section onto a new page.
