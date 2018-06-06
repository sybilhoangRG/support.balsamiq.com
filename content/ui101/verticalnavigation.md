---
title: Vertical Navigation
date: '2015-12-16T11:00:00.000+00:00'
menu: menuui101
weight: 50
product: "UI Design 101"
---

Vertical (a.k.a. "Sidebar") navigation is a way of showing a persistent site or application structure along one side of the product.<!--more-->

The [macOS Human Interface Guidelines](https://developer.apple.com/macos/human-interface-guidelines/windows-and-views/sidebars/) define it by saying "a sidebar typically consists of a table view or outline view that lets people navigate and select items to act upon in the main portion of the window."

Vertical navigation is used extensively on the web and is becoming much more common, almost standard, on mobile via the [slide-out "drawer" pattern](https://material.io/guidelines/patterns/navigation-drawer.html).


---

## When to Use Vertical Navigation

Vertical navigation, like [tabs](../tabs/), is a member of [Master/Detail family of patterns](http://designingwebinterfaces.com/designing-web-interfaces-12-screen-patterns), which is described as "ideal for creating an efficient user experience by allowing the user to stay in the same screen while navigating between items."

[![](//media.balsamiq.com/img/support/tutorials/ui101/finder-verticalnavigation.png)](https://developer.apple.com/macos/human-interface-guidelines/windows-and-views/sidebars/)


Unlike [tabs](../tabs/), vertical navigation is appropriate when the number of categories is  not small, or is user-customizable (such as folders or tags in an email client). It is considered a "safe" navigation pattern because it is familiar, flexible, and doesn't take up much space. It is often used when there is no other obvious choice.


One primary reason *not* to use it is when horizontal space is constrained. This is why many websites (including this page) remove the vertical navigation for small screen sizes, replacing it with either [breadcrumbs](../breadcrumbs/) or the popular "hamburger" menu navigation pattern. The [Material Design guidelines](https://material.io/guidelines/) differentiate between [four distinct variants](https://material.io/guidelines/patterns/navigation-drawer.html#navigation-drawer-behavior), based on screen size: permanent, persistent, mini, and temporary.

---

## How to Use Vertical Navigation

* Highlight the selected page/item in the list. It should not be styled as clickable like the other items (even if it behaves the same).
* Use titles to form logical groupings of related items. [*(macOS Human Interface Guidelines)*](https://developer.apple.com/macos/human-interface-guidelines/windows-and-views/sidebars/)
* Clicking or tapping on category labels should expand or collapse that category rather than linking to its own page.
* Keep the navigation links short. They can be shorter derivatives of page titles themselves. [*(U.S. Web Design Standards)*](https://standards.usa.gov/components/sidenav/)
* Order the list according to what is most useful for the users of your application. [*(GNOME Human Interface Guidelines)*](https://developer.gnome.org/hig/stable/sidebar-lists.html.en)
* Having hierarchical data doesn't mean that you must use a tree view. Very often a list view is a simpler, yet more powerful choice. [*(Microsoft Windows Desktop Guidelines)*](https://msdn.microsoft.com/en-us/library/windows/desktop/dn742445(v=vs.85).aspx)
* In general, refrain from exposing more than two levels of hierarchy within a sidebar. [*(macOS Human Interface Guidelines)*](https://developer.apple.com/macos/human-interface-guidelines/windows-and-views/sidebars/)
* The sidebar can be on the left or right side of the page, but it should be consistent across the application.
* Consider what happens when the sidebar content is longer (taller) than the page content. Ensure that users can still access the entire list (i.e., scroll beyond the page contents).
* Consider replacing the navigation panel with a slide-out panel on small screens (i.e., the ["temporary" variant here](https://material.io/guidelines/patterns/navigation-drawer.html#navigation-drawer-behavior)) or [breadcrumbs](../breadcrumbs/) on desktop displays.

You can find [some good web examples here](https://www.webdesignerdepot.com/2017/06/10-sites-doing-vertical-navigation-right/).

### Basic Usage

![](//media.balsamiq.com/img/support/tutorials/ui101/verticalnavigation.png)

---

## Types of Vertical Navigation

### States

![](//media.balsamiq.com/img/support/tutorials/ui101/verticalnavigation-states.png)

Like [tabs](../tabs/#types-of-tabs), vertical navigation should have a clear selected state, usually achieved by making the selected item bold and/or highlighted. A hover state can also be useful.


### Variations

![](//media.balsamiq.com/img/support/tutorials/ui101/verticalnavigation-variations.png)

---

## Related Controls

* [Tabs](../tabs/)
* [Menu Bars](../menubars/)
