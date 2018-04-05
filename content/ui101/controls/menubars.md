---
title: "Menu Bars"
date: '2015-12-16T11:00:00.000+00:00'
menu: menuui101
weight: 255
product: "UI Design 101"
parent: "controls"
aliases: /ui101/menubars/
---

Menu bars allow users to navigate using categories and sub-categories. They are persistent and unchanging across the app.<!--more-->

In a desktop application, menu bars are the items across the top of the application, a.k.a. the File menu. On the web, they reside in the header of the page. In both cases, they can support nested menus or work as stand-alone categories (also called ["monocline grouping"](http://blog.scnay.com/2009/09/10/monocline-grouping/) or flat structure).

## When to Use Menu Bars

Menu bars are used exclusively for **primary navigation** (unlike [vertical navigation](../verticalnavigation/) or [tabs](../tabs/), which can also be secondary navigation).

They should be used for categories of the application or site that are **meaningful across its entire use**, provided there are not too many categories. If there are too many categories to fit across the page, consider [vertical navigation](../verticalnavigation/) instead.

![](//media.balsamiq.com/img/support/tutorials/ui101/marinelayer-menubar.png)

The main advantage of menu bars is their persistence, i.e., the fact that they are always accessible. This is highlighted in ["About Face: The Essentials of Interaction Design"](https://www.amazon.com/About-Face-Essentials-Interaction-Design/dp/1118766571/):

> Well-designed Web sites make careful use of persistent objects that remain constant throughout the shopping experience, especially the top-level navigation bar along the top of the page. Not only do these areas provide clear navigational options, but their consistent presence and layout also help orient customers.

Menu bars can contain sub-menus (as shown above), but going any deeper than one level should be avoided if possible because it pushes users' mental models, whereas ["organizing things into a single layer of groups is extremely common and can be found everywhere in your home and office."](https://www.amazon.com/About-Face-Essentials-Interaction-Design/dp/1118766571/ "About Face")

---

## How to Use Menu Bars

The [macOS Human Interface Guidelines](https://developer.apple.com/macos/human-interface-guidelines/) provide a [comprehensive guide to using menus in desktop applications](https://developer.apple.com/macos/human-interface-guidelines/menus/menu-anatomy/) (many of which apply to websites as well). Some highlights:


* Make menu titles as short as possible without sacrificing clarity. Ideally they should be limited to one word.
* Use text, not icons, for menu titles. (One exception is that it is generally acceptable to use a logo or graphic in place of "home" text on the web, as shown in the [variations](#variations) below.)
* Disable, don't hide, unavailable menu items.
* Limit the use, depth, and length of submenus.
* Assign keyboard shortcuts and display them next to their associated menu items.
* Use separator lines to create visually distinct groups of related menu items.
* In general, place the most frequently used items at the top of a menu.
* Group menu items that initiate related actions.
* Use a checkmark to indicate that something is currently active.


Other important menu bar guidelines:

* [Don’t model your navigation after your agency’s org structure](https://standards.usa.gov/components/headers/ "U.S. Web Design Standards") (or your application's architectural model). Instead, **structure it according to the tasks and information your users most frequently need to access**.
* [Include skip navigation links](https://standards.usa.gov/components/headers/ "U.S. Web Design Standards") to allow users with screen readers to bypass long navigation lists. 
* Consider using a ["mega menu"](https://standards.usa.gov/components/headers/ "U.S. Web Design Standards") if you have more than six links or menu items within a menu. (See the [variations](#variations) below for more on mega menus.) 
* Use [nine or fewer top-level categories.](https://community.kde.org/KDE_Visual_Design_Group/HIG/Menu_Bar "KDE Human Interface Guidelines")
* For mobile sites and applications, menu bars can be collapsed to a slide-out or expandable "hamburger" menu.
* Make sure that the [menu items look interactive and have enough visual weight](https://www.nngroup.com/articles/menu-design/ "Nielsen Norman Group"). They should invite action. 
* [Make menu links big enough to be easily tapped or clicked.](https://www.nngroup.com/articles/menu-design/ "Nielsen Norman Group") Provide enough padding and spacing around them so that users don't accidentally click the wrong one. 
* [Choose consistency over "wow" factor.](https://www.nngroup.com/articles/menu-design/ "Nielsen Norman Group") Deviate from standards at your own risk. 


### Basic Usage

![](//media.balsamiq.com/img/support/tutorials/ui101/menubars.png)

---

## Types of Menu Bars

### States

![](//media.balsamiq.com/img/support/tutorials/ui101/menubar-states.png)

Like [tabs](../tabs/#types-of-tabs) and [vertical navigation](../verticalnavigation/), menu bars should have a clear selected state, usually indicated by high-contrast text (or inverting the unselected style) and possibly making it bold. A hover state should also be used.


### Variations

To keep the header compact, other functions can be merged into the menu bar area, such as a search box or important actions (e.g., sign in/out). One term for this is ["extended header"](https://standards.usa.gov/components/headers/#extended).

![](//media.balsamiq.com/img/support/tutorials/ui101/menubar-variations.png)

For more complex hierarchies, a "mega menu" overlay can be used, showing multiple columns of sub-categories (or even an additional level of nesting). When using them, pay close attention to the implementation details, especially around the timing of when the menu is triggered and hidden. The [Nielsen Norman Group](https://www.nngroup.com/) has an [in-depth article on mega menus here](https://www.nngroup.com/articles/mega-menus-work-well/).

---

## Related Controls

* [Tabs](../tabs/)
* [Vertical Navigation](../verticalnavigation/)
