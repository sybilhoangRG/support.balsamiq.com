---
title: Links
date: '2015-12-16T11:00:00.000+00:00'
menu: menuui101
weight: 235
product: "UI Design 101"
---

Hyperlinks continue to be central to navigation on the web, such that not adhering to best practices can break the usability of your site or app. <!--more-->


## When to Use Links

Links (originally called ["hypertext links"](https://www.w3.org/MarkUp/HTMLPlus/htmlplus_14.html), then shortened to ["hyperlinks"](https://www.w3.org/MarkUp/html-spec/html-spec_7.html#SEC7), and now typically referred to just as "links") are the original way of navigating from one page to another on the web. They are ubiquitous on the web and common in web applications and web-like desktop apps.

Their strength lies in their simplicity. They can be embedded within blocks of regular text, allowing them to be read in context without interrupting the user's flow, while also indicating that content related to the linked text is available.

Additionally, as long as they are implemented correctly, they offer the advantage that they don't need much decoration to invite action (like buttons do). This is because they are so standard that users expect to be able to click on text that has a distinct color and/or is underlined.

[Wikipedia](https://en.wikipedia.org/) is a showcase for the use of links:

![](//media.balsamiq.com/img/support/tutorials/ui101/wikipedia-links.png)

Links can be used within chunks of text to indicate the presence of related content, but can also stand on their own to attract more attention, such as for primary or secondary navigation, as in [breadcrumbs](../breadcrumbs/), [menu bars](../menubars/) or [vertical navigation](../verticalnavigation/).

Hyperlinks, when used to navigate between or within pages or screens, are familiar and easy to use (with a mouse or keyboard, at least), so they can be used liberally. Although having [too many redundant links on a page can reduce usability](https://www.nngroup.com/articles/duplicate-links/).

---

## How to Use Links

* Links should be visually distinct from other items on the page (preferably using color and underlining; see the referenced article for exceptions to this rule) and don't use that style for non-clickable items. [*(Nielsen Norman Group)*](https://www.nngroup.com/articles/guidelines-for-visualizing-links/)
* More than one link style on a page is OK, but should done purposefully (e.g., one style for body text, another for header or footer text).
* Use the correct link markup for text that links to another page (i.e., the [HTML &lt;a&gt; tag](https://www.w3schools.com/tags/tag_a.asp)). Don't use javascript to perform an action on click.
* Use a different color for visited links. [*(Nielsen Norman Group)*](https://www.nngroup.com/articles/change-the-color-of-visited-links/)
* Link text should make sense without context (i.e., don't write "click here"). [*(Nielsen Norman Group)*](https://www.nngroup.com/articles/writing-links/)
* Link text should be as succinct as possible. [*(Moz)*](https://moz.com/learn/seo/anchor-text)
* Use link titles (via the HTML "title" attribute) to help users predict where a link will lead before they click it, unless it's obvious. [*(Nielsen Norman Group)*](http://www.nngroup.com/articles/using-link-titles-to-help-users-predict-where-they-are-going/)
* Consider using an outgoing (external) link indicator when linking to pages outside of your domain (see [variations](#variations) below for an example). [*(Welie.com)*](http://www.welie.com/patterns/showPattern.php?patternID=outgoing-links)
* Avoid using text links to trigger actions. They should be primarily used for navigation. [*(KDE Human Interface Guidelines)*](https://community.kde.org/KDE_Visual_Design_Group/HIG/Command_Link)
* Ensure sufficient contrast between link colors and their background. [*(U.S. Web Design Standards)*](https://standards.usa.gov/components/colors/)
* For hyperlinks that open a new tab or page using "target='_blank'", add "rel='noopener'" for security reasons. [*(JitBit Founder's blog)*](https://www.jitbit.com/alexblog/256-targetblank---the-most-underestimated-vulnerability-ever/)


### Basic Usage

![](//media.balsamiq.com/img/support/tutorials/ui101/links.png)

---

## Types of Links

### States

![](//media.balsamiq.com/img/support/tutorials/ui101/links-states.png)

As [described above](#how-to-use-links), it is important to have a distinct default link style and a separate style for visited links. The other link states are "active" and "hover". [*(W3Schools)*](https://www.w3schools.com/css/css_link.asp)


### Variations

In addition to the variations described above, links can be styled as [buttons](../buttons/) when used for navigation purposes.

![](//media.balsamiq.com/img/support/tutorials/ui101/links-variations.png)

---

## Related Controls

* [Buttons](../buttons/)
* [Breadcrumbs](../breadcrumbs/)
