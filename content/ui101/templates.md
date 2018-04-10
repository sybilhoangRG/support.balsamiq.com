---
title: "Chapter 5: Templates"
date: '2015-12-16T11:00:00.000+00:00'
menu: menuui101
weight: 501
product: "UI Design 101"
---

You've probably used file templates before. A common type is an office document template, like a cover letter template in a text editing application.

Templates can be great because they provide a starting point for a document with some preset attributes. They help you go faster by starting your project form ready-made screens that you can edit.

There are a few types of templates for interface design that you might use:

*   **Solution-Specific**  
    Templates may be specific to a type of problem you're solving, and provide pages (screens) laid out with a Symbol library of controls for typical solutions. One example might be a Template for creating a Search feature, or our previously mentioned E-Commerce Shopping Cart Solution.
*   **System/Framework Specific**  
    A template may provide standardized screen layout and Symbols for a particular design framework. Some example templates may be for the Bootstrap framework or a design system like Material Design.
*   **Corporate/Product Specific**  
    You may find it useful to create templates that are very specific to your use, like a template for your product with Symbols for your style guide.

Let's start by seeing how to modify a template. By the end of this section, you should be able to create your own.

- - -

## Importing Templates

In Balsamiq, a Template is simply a starter project file that you import. If you're using Balsamiq Cloud, add a template via the menu _Project > Import Controls From Wireframes to Go..._ Browse for templates use the import button to add it into your own projects.

![](//media.balsamiq.com/img/support/ui101/templates/Import%20From%20WTG.png)

- - -

## Selecting the screens you need

Continuing our example of an online shop, let's use an [E-Commerce template](https://wireframestogo.com/3cf8-E-Commerce-Template/) to design more of the shopping experience. Obviously, we'll want to flesh out our shopping cart flow all the way through confirming the transaction.

Below is an overview of the screens that come in this template. Your solution may not require all of them. You'll likely have unique user expectations to consider and business rules to meet, so you'll modify the experience as necessary, pick out the ones you need and discard the rest.

For our example, let's say we want to flesh out the the pre-purchase experience on screens like the landing pages. Let's use the template to create a landing page for a fictional smartphone app.

<div id="filterlist" class="row gallery">

<div class="fitem col-xs-12 col-sm-6 col-md-4">
<div class="gallery-item">
	<a href="//media.balsamiq.com/img/support/ui101/templates/Home%20Page.png"><img src="//media.balsamiq.com/img/support/ui101/templates/Home%20Page.png"></a>
</div></div>

<div class="fitem col-xs-12 col-sm-6 col-md-4">
<div class="gallery-item">
	<img src="//media.balsamiq.com/img/support/ui101/templates/Landing%20Page.png">
</div></div>

<div class="fitem col-xs-12 col-sm-6 col-md-4">
<div class="gallery-item">
	<img src="//media.balsamiq.com/img/support/ui101/templates/Product%20Page.png">
</div></div>

<div class="fitem col-xs-12 col-sm-6 col-md-4">
<div class="gallery-item">
	<img src="//media.balsamiq.com/img/support/ui101/templates/Product%20Page%20-%20Add%20To%20Cart.png">
</div></div>

<div class="fitem col-xs-12 col-sm-6 col-md-4">
<div class="gallery-item">
	<img src="//media.balsamiq.com/img/support/ui101/templates/Cart.png">
</div></div>

<div class="fitem col-xs-12 col-sm-6 col-md-4">
<div class="gallery-item">
	<img src="//media.balsamiq.com/img/support/ui101/templates/Checkout%20-%20Customer%20Info.png">
</div></div>

<div class="fitem col-xs-12 col-sm-6 col-md-4">
<div class="gallery-item">
	<img src="//media.balsamiq.com/img/support/ui101/templates/Checkout%20-%20Shipping.png">
</div></div>

<div class="fitem col-xs-12 col-sm-6 col-md-4">
<div class="gallery-item">
	<img src="//media.balsamiq.com/img/support/ui101/templates/Checkout%20-%20Payment.png">
</div></div>

<div class="fitem col-xs-12 col-sm-6 col-md-4">
<div class="gallery-item">
	<img src="//media.balsamiq.com/img/support/ui101/templates/Checkout%20-%20Success.png">
</div></div>

<div class="fitem col-xs-12 col-sm-6 col-md-4">
<div class="gallery-item">
	<img src="//media.balsamiq.com/img/support/ui101/templates/Email%20Confirmation.png">
</div></div>

</div>


- - -

## Modifying Pre-Made Screens

For this example, we'll modify the generic Landing Page template using our own copy and add some elements for our fictional smartphone app.

When you open a template you'll probably see some placeholder copy as in the example on the left below. Simply select and edit each of the place holders.

In the wireframe on the right, we've modified the text, we added some wireframed elements to illustrate our product, and using our new knowledge of design principles we laid out some of the parts to fit better with our new illustrations and copy.

<table>
<tr>
<th>Template with starting suggestions to design a landing page</th>
<th>Edit placeholders to customize the screen.</th>
</tr>
<tr>
<td><img src="//media.balsamiq.com/img/support/ui101/templates/Landing%20Page%20-%20Blank.png"></td>
<td><img src="//media.balsamiq.com/img/support/ui101/templates/Landing%20Page%20-%20Modified.png"></td>
</tr>
</table>

Pretty simple! Hopefully, editing a template should seem much faster than laying out all of the components from scratch. You'll want to tweak it to suit your needs, but it's a good way to start the design discussion with your team.

### A note about Symbols Libraries

Some templates may also contain Symbols Libraries. Our E-Commerce template has Symbols for the components used on the screens above.

The idea behind using Symbols is that you can easily drop in these re-usable components that are made specifically for this type of project. You can find out more about Symbols in the [Balsamiq docs](https://docs.balsamiq.com/).

- - -

## Closing Thoughts

Like design patterns, templates serve as a starting point and are usually built on an understanding of what typically works well for a common problem. Templates differ from design patterns in that they usually propose a plan for solving a broader scope of problem.

Interface designers are known for building systems to make their work efficient. Templates are one example of that. Once you've become adept at working with templates you can start to set up your own systems to make your work go faster. If you work in-house on a product team, create templates that reflect your organizational style. If you work in an agency or design/development shop, create templates for the repeatable types of client projects you work on.

{{% alert info %}}

**The Cooking Analogy:**

Let's step back for a moment and put templates under the lens of our cooking analogy. In cooking, the orchestration of dishes that work well together create a meal—a complete culinary experience. Templates are like that. Pieces of user interface often go well together to create an entire experience.

As you explore your users and problem more deeply, you'll begin to see what parts of the template work for your needs and swap out what doesn't, just as you would deviate from a recipe to make it your own.

{{% /alert %}}  

- - -

### Learn More about this Topic

*   Download the template used in this section: [E-Commerce Template from Wireframes To Go](https://wireframestogo.com/3cf8-E-Commerce-Template/)
*   Landing Page Template and [Designing a Landing Page](https://support.balsamiq.com/tutorials/landingpages/) tutorial