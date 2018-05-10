---
title: How Can I Display My Project Wireframes on Multiple Confluence Pages?
date: '2015-05-09T14:46:35.000+00:00'
weight: 240
menu:
  menuplugins:
    weight: 240
draft: ''

---

{{% alert info %}}**Note:** This FAQ is for our most up-to-date Atlassian Add-Ons {{% /alert %}}

You may need to display wireframes on different Confluence pages. While there is no direct way to do this (for now), we've created this page to describe a workaround that will help you with this.

* * *

## Displaying a Wireframe on Multiple Confluence Pages

### 1. Grab the Wireframe Image Link From the Attachments

Once you have identified the wireframe you want to use on different pages, open the Confluence page attachments.

![](//media.balsamiq.com/img/support/prodfaqs/attachments.png)

From there, right-click on the image file generated from your wireframe (PNG) and copy the link address. The corresponding image will display the wireframe name in the **Comment** section, as shown below.

![](//media.balsamiq.com/img/support/prodfaqs/link-address.png)

### 2. Use the Link in Your Other Confluence Page

Once you have copied the link, please open the other Confluence page and **insert an image**. From the insert dialog, select **images from the web** and copy the link there. You now have your wireframe displayed on the Confluence page.

![gif](//media.balsamiq.com/img/support/prodfaqs/link-image.png)

{{% alert info %}}**Note:** Since this is only the image of your wireframe, you will need to go back to the original Confluence page to update the wireframe but changes will be reflected on both pages.{{% /alert %}}

* * *

## Including a Page Containing a Wireframe in Another Page

There are two ways to do this, both using Confluence macros:  

* [Include Page Macro](https://confluence.atlassian.com/doc/include-page-macro-139514.html)  
* [Excerpt Include Macro](https://confluence.atlassian.com/doc/excerpt-include-macro-148067.html)  
* [Excerpt Macro](https://confluence.atlassian.com/doc/excerpt-macro-148062.html)

### 1. Including the Full Page

To include a full page containing a Balsamiq Wireframe within another page, use the `Include Page Macro`:

![](//media.balsamiq.com/img/support/prodfaqs/include-page-macro.png)  
![](//media.balsamiq.com/img/support/prodfaqs/full-page-include.png)

### 2. Including Only Part of the Page

To include part of a page containing a Balsamiq Wireframe withing in another page, first define the partial page using the `Excerpt Macro` then use the `Excerpt Include Macro`:

![](//media.balsamiq.com/img/support/prodfaqs/excerpt-include-macro.png)  
![](//media.balsamiq.com/img/support/prodfaqs/partial-include.png)

***

We hope this is helpful but please [get in touch](https://balsamiq.com/company/contact/#/t/m4c) if you need any further help to set it up. We're here to help! :)
