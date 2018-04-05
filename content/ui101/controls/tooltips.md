---
title: "Tooltips"
date: '2015-12-16T11:00:00.000+00:00'
menu: menuui101
weight: 270
product: "UI Design 101"
parent: "controls"
aliases: /ui101/tooltips/
---

Tooltips are a common form of contextual help that leverage the "details on demand" UX pattern.<!--more-->

They are a great way to help novices without disrupting experienced users. A classic use case for tooltips is to show keyboard shortcuts when a user hovers over an action button.

In ["About Face: The Essentials of Interaction Design"](https://www.amazon.com/dp/1118766571/), Alan Cooper calls tooltips "one of the cleverest and most effective user-interface idioms we've ever seen."

## When to Use Tooltips

Tooltips are generally under-used, so when in doubt, use them (appropriately of course; the implementation details are critical, so make sure to read the [next section](#how-to-use-tooltips)).

The [Microsoft UWP Guidelines](https://docs.microsoft.com/en-us/windows/uwp/controls-and-patterns/tooltips) have a nice rule of thumb for tooltips: **"if the information is available elsewhere in the same experience, you do not need a tooltip."** This means that a button that contains an icon and text shouldn't have a tooltip, but a button with an icon alone should, as in the example below.

![](//media.balsamiq.com/img/support/tutorials/ui101/tooltips-whentouse.png)

[Here](https://docs.microsoft.com/en-us/windows/uwp/controls-and-patterns/tooltips#example) is a typical tooltip example:

![](//media.balsamiq.com/img/support/tutorials/ui101/bing-tooltips.png)

Tooltips are also useful when a longer explanation can be useful, but is impractical for space reasons. Another simple heuristic for using tooltips is when a control "benefits from a supplemental description or further information" [*(UX Planet)*](https://uxplanet.org/tooltips-in-ui-design-f63e117aa3d1). However, tooltips should never be used as a fallback for unclear icons or labels. Tooltips are supplementary information and should not be treated as a primary means of helping users understand the system.

Finally, tooltips are often not shown on mobile devices, so don't rely on them or assume that your user will read them.

---

## How to Use Tooltips

* Display tooltips only as the result of user interaction, [never display them on their own](https://docs.microsoft.com/en-us/windows/uwp/controls-and-patterns/tooltips "Microsoft UWP Guidelines"). 
* [Only show plain text in a tooltip.](https://material.io/guidelines/components/tooltips.html "Google Material Design guidelines") Avoid formatted text or pictures. 
* Don't use the HTML ["alt" attribute](https://www.w3schools.com/tags/att_alt.asp) for tooltips. This should only be used as alternative text for accessibility purposes. Use the ["title" attribute](https://www.w3schools.com/tags/att_title.asp) instead.
* Focus on the action a control initiates. [Start with a verb](https://developer.apple.com/macos/human-interface-guidelines/user-interaction/help/ "macOS Human Interface Guidelines") to tell users what will happen when they click.
* Keep them short. The [macOS Human Interface Guidelines](https://developer.apple.com/macos/human-interface-guidelines/user-interaction/help/) suggest a maximum of 60-75 characters.
* Tooltips should be placed near the object being hovered, but should [never be placed in a way that interferes with what the user is doing](https://uxplanet.org/tooltips-in-ui-design-f63e117aa3d1 "UX Planet") by obscuring the object of interest.
* If you want them to be available on mobile, [consider adding small informational buttons for touch screen use](https://community.kde.org/KDE_Visual_Design_Group/HIG/Tooltip "KDE Human Interface Guidelines") (see [variations below](#variations)). 
* Timing is critical. If you have control over it, follow these guidelines:
	* Delay the start of the tooltip so that they aren't constantly popping up as the user moves their mouse across the screen. [Wait until the user has stopped moving their cursor for about a second.](https://www.amazon.com/dp/1118766571/ "About Face: The Essentials of Interaction Design")
	* Show the tooltip for [about 10 seconds or until the pointer moves away from the control] (https://developer.apple.com/macos/human-interface-guidelines/user-interaction/help/ "macOS Human Interface Guidelines").
	* [Fade tooltips in and out over ~150ms.](https://material.io/guidelines/components/tooltips.html "Google Material Design guidelines")
* Most operating systems and platforms have built-in tooltip controls; use them rather than defining your own.




### Basic Usage

![](//media.balsamiq.com/img/support/tutorials/ui101/tooltips.png)

---

## Types of Tooltips

### States

Tooltip states are simple; they are either **on** or **off**. If they transition between those states, it should happen quickly (150ms or less).

### Variations

Tooltip styles vary greatly, although functional variations should be limited, since users expect them to behave in a standard way.

Some simple variations include:

* Adding a directional arrow pointing to the object the tooltip is describing.
* Using light formatting or visual elements for additional information (anything beyond this makes it an [overlay control](http://patternry.com/p=overlay/) with different rules for behavior).
* Adding an explicit tooltip icon or button. This can be helpful for complex or novel interfaces where you expect users to need help, or for adding touch behavior on mobile.

![](//media.balsamiq.com/img/support/tutorials/ui101/tooltips-variations.png)

---

## Related Controls

* [Validation](../validation/)
