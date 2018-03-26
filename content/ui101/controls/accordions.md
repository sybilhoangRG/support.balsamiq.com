---
title: "Accordions"
date: '2015-12-16T11:00:00.000+00:00'
menu: menuui101
weight: 260
product: "UI Design 101"
parent: "controls"
aliases: /ui101/accordions/
---

Accordions are stacked containers with nested items that expand and collapse when clicked or tapped.<!--more-->

Accordions are an attractive control because they allow a lot of links to be shown in a compact space. But they can be less familiar or even intuitive, so be careful not to overuse them. They can be used either for navigation or for content, in contrast to [vertical navigation](../verticalnavigation/).

Other names include expansion panel and expand/collapse control.


## When to Use Accordions

The book ["Designing Web Interfaces"](https://www.amazon.com/Designing-Web-Interfaces-Principles-Interactions/dp/0596516258/) says that accordions are "good for collapsed modules of content. However, they should be used sparingly, as they have as strong visual style."

Part of that visual style frequently involves animating the panels as they open and close, which can seem like a "cool" effect, but often adds unnecessary [interaction cost](https://www.nngroup.com/articles/interaction-cost-definition/) that can be avoided by using a simpler control. In that way they are similar to [carousel](http://ui-patterns.com/patterns/Carousel) controls, which have fallen out of favor for that reason.

While accordions are often *not* the best choice for desktop screens, they are [more likely to be appropriate on mobile](https://www.nngroup.com/articles/mobile-accordions/), like this mobile navigation menu from [UX Mastery](https://uxmastery.com/):

![](//media.balsamiq.com/img/support/tutorials/ui101/uxmastery-accordions.png)

A good reason to use accordions for navigation is when the user may want to see the whole, as well as the parts, of the navigation hierarchy. One use case is where users may want to explore the site contents before committing to a particular section or link. In that way, they are similar to hierarchical [vertical navigation](../verticalnavigation/).

Accordion (😉) to the site [UI Patterns](http://ui-patterns.com/patterns/AccordionMenu), accordions should only be used for navigation when there are:

* more than 2 main sections on a website each with 2 or more subsections.
* less than 10 main sections
* only have two levels to show in the main navigation.

As for using accordions for in-page content, the [U.S. Web Design Standards](https://standards.usa.gov/components/accordions/) suggests that if there is not a lot of content, or if users will want to see all content at once, *don't* use an accordion control. One valid use case example is a FAQ help page. However, don't use them *only* because there is a lot of content. The idea that [desktop users don't like long pages is considered a myth by many](https://www.nngroup.com/articles/accordions-complex-content/).

![](//media.balsamiq.com/img/support/tutorials/ui101/uswebdesignstandards-accordions.png)

In all cases, avoid horizontal accordions (where panels are "stacked" horizontally). They are unfamiliar and almost always inferior to another kind of control.


---

## How to Use Accordions

The following are general guidelines that apply to most cases.

* When one panel is clicked it is expanded, while other panels are collapsed. Only one panel should be open at a time. [*(UI Patterns)*](http://ui-patterns.com/patterns/AccordionMenu)
* Don't open accordion containers on hover. Use click or touch behavior instead. [*("Designing Web Interfaces")*](https://www.amazon.com/Designing-Web-Interfaces-Principles-Interactions/dp/0596516258/)
* Allow users to click anywhere in the header area to expand or collapse the content; a larger target is easier to manipulate. [*(U.S. Web Design Standards)*](https://standards.usa.gov/components/accordions/)
* Start with the first section open. Don't default all to closed.
* Highlight the current panel so the user can distinguish open panel headers form closed panel headers. [*(Welie.com)*](http://www.welie.com/patterns/showPattern.php?patternID=accordion)
* If animating panels, "the animation should be subtle which means that it should last no more than 250ms." [*(Welie.com)*](http://www.welie.com/patterns/showPattern.php?patternID=accordion)
* Do not mix the accordion with other types of navigation on the same level. [*(KDE Human Interface Guidelines)*](https://community.kde.org/KDE_Visual_Design_Group/HIG/Accordion)
* If the content of a section won't fit on the page vertically, scroll within the panel rather than scrolling the entire control. [*(KDE Human Interface Guidelines)*](https://community.kde.org/KDE_Visual_Design_Group/HIG/Accordion)

### Basic Usage

![](//media.balsamiq.com/img/support/tutorials/ui101/accordions.png)

---

## Types of Accordions

### States

Accordions should have a clear selected state for the open panel and, if applicable, for the selected item within. A hover state should also be applied to both.


### Variations

Variations should be minimized in order to keep consistent with standards. One common option is the addition of icons. The + and - icons are the most identifiable and familiar. Pointed triangles or chevrons can also be used.

![](//media.balsamiq.com/img/support/tutorials/ui101/accordions-variations.png)

The icon states should tell the user what will happen when they click, i.e., the plus or expand icon should be shown on collapsed panels rather than indicating that an open panel has been expanded [*(Smashing Magazine)*](https://www.smashingmagazine.com/2017/06/designing-perfect-accordion-checklist/).

---

## Related Controls

* [Tabs](../tabs/)
* [Vertical Navigation](../verticalnavigation/)
