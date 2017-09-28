---
title: Accordions
date: '2015-12-16T11:00:00.000+00:00'
menu: menuui101
weight: 75
product: "UI Design 101"
draft: 'true'
---

Accordions are stacked containers with nested items that expand and collapse when clicked or tapped.<!--more-->

Accordions are an attractive control because they allow a lot of links to be shown in a compact space. But they are often overused.

the animation looks cool. kind of like carousels, which have fallen out of favor on websites.

people don't like to explore.

can seem like a catch-all or silver bullet

lack of standards and encourages laziness

sometimes used on their own, other times embedded (in a table of other control)


https://www.smashingmagazine.com/2017/06/designing-perfect-accordion-checklist/

A questionable accordion here: https://www.smashingmagazine.com/wp-content/uploads/2017/06/sony-accordion-large-opt.png

> If one section is already expanded, and the user clicks on another section, should the first one collapse or stay as is? ...Both options seem to have reasonable use cases.
> 
> The nature of an accordion would call for automatic collapsing, but it might not be the best option in terms of usability.

You probably shouldn't nest accordions.

Related control: tabs

kind of like vertical tabs?

don't use an accordion if there's not a lot of content.

don't do it on hover.

with accordions, there are more rules about when *not* to use them.

start with the first section open. don't default all to closed. except...

---

In a desktop application, menu bars are the items across the top of the application, a.k.a. the File menu. On the web, they reside in the header of the page. In both cases, they can support nested menus or work as stand-alone categories (also called ["monocline grouping"](http://blog.scnay.com/2009/09/10/monocline-grouping/) or flat structure).

## When to Use Accordions

Menu bars are used exclusively for **primary navigation** (unlike [vertical navigation](../verticalnavigation/) or [tabs](../tabs/), which can also be secondary navigation).

They should be used for categories of the application or site that are **meaningful across its entire use**, provided there are not too many categories. If there are too many categories to fit across the page, consider [vertical navigation](../verticalnavigation/) instead.

![](//media.balsamiq.com/img/support/tutorials/ui101/marinelayer-menubar.png)

The main advantage of menu bars is their persistence, i.e., the fact that they are always accessible. This is highlighted in ["About Face: The Essentials of Interaction Design"](https://www.amazon.com/About-Face-Essentials-Interaction-Design/dp/1118766571/):

> Well-designed Web sites make careful use of persistent objects that remain constant throughout the shopping experience, especially the top-level navigation bar along the top of the page. Not only do these areas provide clear navigational options, but their consistent presence and layout also help orient customers.

Menu bars can contain sub-menus (as shown above), but going any deeper than one level should be avoided if possible because it pushes users' mental models, whereas "organizing things into a single layer of groups is extremely common and can be found everywhere in your home and office." ([*About Face*](https://www.amazon.com/About-Face-Essentials-Interaction-Design/dp/1118766571/))

---

## How to Use Accordions

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

* Don’t model your navigation after your agency’s org structure (or your application's architectural model). Instead, **structure it according to the tasks and information your users most frequently need to access**. [(*U.S. Web Design Standards*)](https://standards.usa.gov/components/headers/)
* Include skip navigation links to allow users with screen readers to bypass long navigation lists. [(*U.S. Web Design Standards*)](https://standards.usa.gov/components/headers/)
* Consider using a "mega menu" if you have more than six links or menu items within a menu. (See the [variations](#variations) below for more on mega menus.) [(*U.S. Web Design Standards*)](https://standards.usa.gov/components/headers/)
* Use nine or fewer top-level categories. ([*KDE Human Interface Guidelines*](https://community.kde.org/KDE_Visual_Design_Group/HIG/Menu_Bar))
* For mobile sites and applications, menu bars can be collapsed to a slide-out or expandable "hamburger" menu.
* Make sure that the menu items look interactive and have enough visual weight. They should invite action. [(*Nielsen Norman Group*)](https://www.nngroup.com/articles/menu-design/)
* Make menu links big enough to be easily tapped or clicked. Provide enough padding and spacing around them so that users don't accidentally click the wrong one. [(*Nielsen Norman Group*)](https://www.nngroup.com/articles/menu-design/)
* Choose consistency over "wow" factor. Deviate from standards at your own risk. [(*Nielsen Norman Group*)](https://www.nngroup.com/articles/menu-design/)


### Basic Usage

![](//media.balsamiq.com/img/support/tutorials/ui101/menubars.png)

---

## Types of Accordions

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
