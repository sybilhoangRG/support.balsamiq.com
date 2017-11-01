---
title: User Testing Your iPad Wireframes
date: '2015-12-16T11:00:00.000+00:00'
weight: 155
menu: "menututorials"
draft: ''
product: "Tutorials & Videos"
---

When you're designing wireframes using Balsamiq you don't need to sweat the details, but _some_ of the details become more important when you start testing your wireframes. On an iPad, in particular, the wireframes have a much more immersive feel when they fit the viewport exactly, like in the example below.

![insitu.jpg](https://media.balsamiq.com/img/support/tutorials/ipad/insitu.jpg)

This tutorial will help you ensure that your iPad wireframes are designed so that they fit nicely on an iPad when exported as images or a PDF.

* * *

## Step 1 - Add the iPad Control

First, add an iPad control to the canvas. Click on the iPad control to bring up the [Property Inspector](https://docs.balsamiq.com/desktop/inspector/). Exporting to the right dimensions works best with the **Top Bar off**, so turn it off in the Property Inspector. In the examples below we'll also turn the transparent background on, but you can leave it white if you prefer.

![PI-ipad.png](https://media.balsamiq.com/img/support/tutorials/ipad/PI-ipad.png)

This tutorial also assumes that you haven't resized the iPad control, so try to leave it as the default size (or you'll have to do some math in step 2!).

Next, click the lock icon in the [toolbar](https://docs.balsamiq.com/desktop/overview/#the-toolbar) or from the right-click menu to lock the control into place. This step isn't necessary, but it makes it easier to keep it in place when adding other controls on top of it.

Finally, right-click on the iPad control and select "Treat As Markup", as shown below. The reason for this will be explained later.

![markup.png](https://media.balsamiq.com/img/support/tutorials/ipad/markup.png)

* * *

## Step 2 - Add a Rectangle Control

Now that we've added the iPad control, we want to make sure that what we put inside it is going to get exported in the same proportions as an actual iPad screen (not the same _dimensions_, but the same _aspect ratio_, which is **4:3** for the iPad).

To do this, add a **Rectangle control** to the canvas. Now, select it and set the following properties in the Property Inspector:

1.  Set the **Size** to **549x732** (you can click inside the box to edit the numbers)
2.  Set the **Border Style** to **No Border** (the first option)

These settings are highlighted below:

![PI-rectangle.png](https://media.balsamiq.com/img/support/tutorials/ipad/PI-rectangle.png)

Next, move the rectangle over the iPad until both the vertical and horizontal center alignment guides appear over the iPad, like the image below. This will ensure that it is lined up with the iPad viewport.

![snap-rectangle.png](https://media.balsamiq.com/img/support/tutorials/ipad/snap-rectangle.png)

Finally, click on the rectangle and lock it, just as we did with the iPad control. This will prevent it from moving around when you're adding new controls. You shouldn't be able to select either control at this point (you can always unlock a control by right-clicking on it and selecting "Unlock").

* * *

## Step 3 - Create Your Wireframe

Now, the fun part. Create your wireframe, making sure that all of your controls fit inside the viewport/window of the iPad device (the alignment guides at the edges should help with this).

Here's an example:

![bmockups-sketch.png](https://media.balsamiq.com/img/support/tutorials/ipad/bmockups-sketch.png)

* * *

## Step 4 - Export Your Wireframe

Now that the wireframe is done, you're almost ready to export. Since you don't want to view the iPad device control inside the iPad itself, we need to get rid of the iPad device in Balsamiq. Instead of deleting it, we can hide it using the [Show/Hide Markup](https://docs.balsamiq.com/desktop/markup/) feature.

We've already set the iPad device as markup in step 1, now we just need to toggle the markup layer to hide it. Go to **View > Markup and uncheck it**. Or, click the hide markup button in the toolbar (next to the zoom icon). The iPad device should disappear.

Now, export your wireframe as an [image](https://docs.balsamiq.com/desktop/exporting/#exporting-to-an-image) or [PDF](https://docs.balsamiq.com/desktop/exporting/#exporting-to-pdf) via the File menu.

If you are exporting as PDF make sure that any other wireframes you have open are also iPad wireframes and have been treated similarly (so that all the PDF pages will be the same size). Also, set the Export Options to "Optimize for viewing" with no margins, as shown below.

![pdf-export.png](https://media.balsamiq.com/img/support/tutorials/ipad/pdf-export.png)

* * *

## Step 5 - Send to Your iPad

You can transfer your exported wireframes to your iPad via email, Dropbox, or a variety of other methods. There are also several applications that you can use to view them on your iPad (these will usually be listed in the "Open in..." menu when you have the image or PDF selected).

We've found that the Apple **Photos** application works well for viewing wireframes saved as images and the Apple **iBooks** application (free in the App Store) works well for viewing wireframes saved as PDFs. The rectangle control we added in step 2 should ensure that your wireframes are sized correctly in either of these applications.

If you've exported a wireframe with links to a PDF the link targets should work, allowing you to interact with your wireframes like a real product. This is great for user testing or informal review while the design is in progress!
