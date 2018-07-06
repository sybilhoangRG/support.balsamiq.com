---
title: Data Tables
date: '2015-12-16T11:00:00.000+00:00'
menu: menuui101
weight: 80
product: "UI Design 101"
---

Data tables, also called table views, tables, and data grids use columns and rows to **display related information in a grid**.<!--more-->

<table style="border: 1px solid black; width: auto; display:table;width:320px;">
<thead>
<tr>
<th style="border: 1px solid black; padding: 10px;">this</th>
<th style="border: 1px solid black; padding: 10px;">is</th>
<th style="border: 1px solid black; padding: 10px;">a</th>
<th style="border: 1px solid black; padding: 10px;">very</th>
</tr>
</thead>
<tbody>
<tr>
<td style="border: 1px solid black; padding: 10px;">basic</td>
<td style="border: 1px solid black; padding: 10px;">HTML</td>
<td style="border: 1px solid black; padding: 10px;">data</td>
<td style="border: 1px solid black; padding: 10px;">table</td>
</tr>
</tbody>
</table>

Tables are readable and familiar when designed appropriately.

For very simple tables the guidelines are easy to follow. The challenge comes as the data becomes too much to parse at a glance. When you start adding ways to filter, sort, search, and act on the data the waters get a lot muddier.


## When to Use Data Tables

Data tables are best used for **numerical data and lists of objects of the same type**.

Here is a typical numerical data table:

![](//media.balsamiq.com/img/support/tutorials/ui101/espn-tables.png)

Tables like the one below with actions, links, and buttons are common in enterprise, CRM, and other business applications *([image source](https://uxdesign.cc/designing-better-tables-for-enterprise-applications-f9ef545e9fbd))*:

![](//media.balsamiq.com/img/support/tutorials/ui101/enterprise-tables.png)

The [Google Material Design guidelines](https://material.io/guidelines/components/data-tables.html) suggest that tables should only be used when there are **three or more columns**. Side-by-side lists or any other text control can be used for a simple two-column comparison.

[Apple](https://developer.apple.com/macos/human-interface-guidelines/windows-and-views/table-views/) mentions that an outline (a.k.a. Tree) view should be used instead of a table view for hierarchical data. One variation for this scenario is a tree table ([described below](#variations)).

---

## How to Use Data Tables

* Use a header row with descriptive titles. *([macOS Human Interface Guidelines](https://developer.apple.com/macos/human-interface-guidelines/windows-and-views/table-views/))*
* Let people click column headings to sort a table view if it provides value. *([macOS Human Interface Guidelines](https://developer.apple.com/macos/human-interface-guidelines/windows-and-views/table-views/))*
* Clicking once on a column heading should apply "natural" sort order (e.g., alphabetical, smallest number first, earliest date first, checked items first) and show a *down* arrow. Clicking again should reverse the order and show an *up* arrow. *([GNOME Human Interface Guidelines](https://developer.gnome.org/hig/stable/lists.html.en))*
* Alternate row colors for large tables. This is often referred to as "zebra striping". *([macOS Human Interface Guidelines](https://developer.apple.com/macos/human-interface-guidelines/windows-and-views/table-views/))*
* Checkboxes should accompany each row if the user needs to select or manipulate data. *([Google Material Design guidelines](https://material.io/guidelines/components/data-tables.html))*
* For actions that can only be applied to one row at a time (e.g., edit, view details), standard practice is to provide a link or icon in the last column of the table.
* Use the [&lt;THEAD&gt; and &lt;TH&gt; HTML tags](https://www.w3schools.com/tags/tag_thead.asp) for header rows for accessibility and easier visual styling.
* Left-align text and right-align numbers.
* If you have numeric data, keep the level of precision appropriate. The fewer decimals, the less time it takes to scan and understand the data.
* Show only the information that users really need to see, but provide the ability to dig deeper into details if needed. Use Inlays, Overlays, and tooltips for showing details on the same page with the table to maintain user’s flow.
* Consider using floating (i.e., "sticky") header rows for long tables.
* Provide the ability to search within long tables. *([GNOME Human Interface Guidelines](https://developer.gnome.org/hig/stable/lists.html.en))*
* Pay attention to display density. Having the data too close together makes it hard to read, yet using too much spacing means more scrolling (and more time to find what the reader is looking for).  The [Google Material Design guidelines](https://material.io/guidelines/components/data-tables.html#data-tables-specs) offer some specifications for padding and spacing within tables. You can give users the option to change the display density ([as shown here](https://uxdesign.cc/design-better-data-tables-4ecc99d23356#f194)), but don't use this an an excuse not to pick a good default.
* Pagination is useful for large data sets, but don't immediately assume that it's needed. Studies have shown that [users don't mind scrolling](http://uxmyths.com/post/654047943/myth-people-dont-scroll) in many cases and showing all the information on one page means that users can search and sort more easily to find what they're looking for.
* If you use pagination, make sure to show the total number of pages or results. The ability to choose how many rows to show on a page is also useful.
* Actions that users can perform on the data should be placed around the edges of the table (as shown in the [example below](#basic-usage)). Pagination is usually placed at the bottom, while filtering, sorting, and multi-row actions are often placed in the top-left and/or top-right.
* If you provide a way to filter or otherwise limit the data, make sure to clearly indicate that a subset of the data is being shown. You can see some [table filter examples here](http://ui-patterns.com/patterns/TableFilter).
* Use color and decoration sparingly. It can be useful to highlight unexpected data (such as extreme/outlying values or failed actions), but can detract from overall readability. *([A List Apart](https://alistapart.com/article/web-typography-tables))*

More useful guidelines and examples can be found in [this article on designing better data tables](https://uxdesign.cc/design-better-data-tables-4ecc99d23356) and [this article on designing tables to be readable](https://alistapart.com/article/web-typography-tables).


### Basic Usage

![](//media.balsamiq.com/img/support/tutorials/ui101/tables.png)

---

## Types of Data Tables

### States

Tables don't have states like other UI controls, but some have cells which can be changed from read-only to editable. In the case of editable cells, they should be visually distinct through a lowered bevel or thicker border *([KDE Human Interface Guidelines](https://community.kde.org/KDE_Visual_Design_Group/HIG/TableView))*.

### Variations

Most table variations exist for the purposes of showing additional data for a specific row. This is done to avoid forcing the user to visit a new page and losing context.

[This article on designing better data tables](https://uxdesign.cc/design-better-data-tables-4ecc99d23356) shows examples of this variation, including:

* [Expandable Rows](https://uxdesign.cc/design-better-data-tables-4ecc99d23356#a1a4) (a.k.a. Tree Table or [Outline View](https://developer.apple.com/macos/human-interface-guidelines/windows-and-views/outline-views/))
* [Quick View](https://uxdesign.cc/design-better-data-tables-4ecc99d23356#4731)
* [Modal](https://uxdesign.cc/design-better-data-tables-4ecc99d23356#ecb6)

![](//media.balsamiq.com/img/support/tutorials/ui101/tables-variations.png)

These details-on-demand variations should be reserved for complex data tables. It is overkill for cases where the user is primarily browsing. A better choice is to carefully consider which information the user needs to see and provide only that data.

---

## Related Controls

* Lists
