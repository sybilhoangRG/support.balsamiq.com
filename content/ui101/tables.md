---
title: Data Tables
date: '2015-12-16T11:00:00.000+00:00'
menu: menuui101
weight: 80
product: "UI Design 101"
draft: true
---

Data tables, also called Table views, tables, and data grids use columns and rows to display related information in a grid.<!--more-->

| this | is | a |
| ---- |--- | --- |
| basic | data | table |

For very simple tables the guidelines are easy to follow. The trouble comes about when you have too much data to parse at a glance. When you start thinking about ways to filter, sort, search, and act on the data the waters get a lot muddier. 



## When to Use Data Tables

* Use an outline view instead of a table view to present hierarchical data ([apple](https://developer.apple.com/macos/human-interface-guidelines/windows-and-views/table-views/))
* Use when you have Three or more columns of data (google)

![](//media.balsamiq.com/img/support/tutorials/ui101/uxmastery-accordions.png)


![](//media.balsamiq.com/img/support/tutorials/ui101/uswebdesignstandards-accordions.png)




---

## How to Use Data Tables

* Let people click column headings to sort a table view if it provides value. ([apple](https://developer.apple.com/macos/human-interface-guidelines/windows-and-views/table-views/))
* Consider using alternating row colors in multi-column table views (apple)
* Use a header row with descriptive titles
* Checkboxes should accompany each row if the user needs to select or manipulate data. ([google](https://material.io/guidelines/components/data-tables.html))
* Toggle on options and text when row(s) are selected (look at balsamiq cloud as an example?)
* Pay attention to display density (maybe offer a choice, but better to default to the best one)
* How to do pagination...
* hover actions or check + buttons?
* inline editing vs. new page (or modal)
* multiple filters
* can use some icons or colors for important things only
* right align numbers, left align text
* sticky headers?
* Use a TH for headers for accessibility and styling purposes

add a description to the table

look at google sheets tools and gmail

infinite scroll - yes or no?

like multi-column (two dimensional) lists (related control?)

view/edit mode? (KDE)


row / zebra striping (look at designing interfaces book)

nested / tree table

links (use breadcrumbs to get back)

can add buttons or checkboxes



### Basic Usage

![](//media.balsamiq.com/img/support/tutorials/ui101/tables.png)

---

## Types of Data Tables

### States

* Hover state on each row
* Selected state for each row (different color from hover)
* Sorted icon

editable?

### Variations

Variations should be minimized in order to keep consistent with standards. One common option is the addition of icons. The + and - icons are the most identifiable and familiar. Pointed triangles or chevrons can also be used.

![](//media.balsamiq.com/img/support/tutorials/ui101/accordions-variations.png)

The icon states should tell the user what will happen when they click, i.e., the plus or expand icon should be shown on collapsed panels rather than indicating that an open panel has been expanded [*(Smashing Magazine)*](https://www.smashingmagazine.com/2017/06/designing-perfect-accordion-checklist/).

---

## Related Controls

* Lists?