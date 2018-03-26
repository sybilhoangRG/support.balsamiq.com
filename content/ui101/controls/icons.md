---
title: "Icons"
date: '2015-12-16T11:00:00.000+00:00'
menu: menuui101
weight: 285
product: "UI Design 101"
parent: "controls"
aliases: /ui101/icons/
---

Icons are everywhere, both in software and outside of it. The power of an image helps users identify things quickly and accurately.<!--more-->

The [KDE visual design group](https://community.kde.org/KDE_Visual_Design_Group/HIG/IconDesign) calls icons "a shorthand for conveying meaning that users perceive almost instantaneously." They can be also useful for internationalization and when concepts are hard to describe in words.


## When to Use Icons

It is rare that icon use is actively discouraged. The biggest danger when using icons is the use of ambiguous or unclear icons, which can either mislead the user or conflict with their adjacent label, resulting in a slower and/or more frustrating experience with your product. In short, [bad icons are costly.](https://www.nngroup.com/articles/bad-icons/)

The [GNOME developer guidelines](https://developer.gnome.org/hig/stable/icons-and-artwork.html.en) state that choosing the correct icon for each purpose is "vital to making sure that your application is usable." They go on to encourage their use, though, calling them "an essential part of any application" and "a crucial part of its identity."

Icons are also a great way to provide redundancy, especially for important messages. In the following example, there are three ways that the error state is conveyed: the text itself, the color, and the icon. The icon reinforces the severity of the message.

![](//media.balsamiq.com/img/support/tutorials/ui101/usweb-icon.png)

When used correctly, icons can speed up a user's interaction with your product, enhance its usability, and reinforce your brand identity.

![](//media.balsamiq.com/img/support/tutorials/ui101/tripadvisor-icons.png)


---

## How to Use Icons

{{% alert info %}}**Note:** The [Google Material Design Guidelines](https://material.io/guidelines/style/icons.html) differentiate between **product icons** and **system icons**. Product icons are primarily for branding and visual identity purposes. An example of a product icon is an application icon on the task bar or home screen. The guidelines below apply mostly to system icons, which are identifiers for actions or commands.{{% /alert %}}

The [KDE Human Interface Guidelines](https://community.kde.org/KDE_Visual_Design_Group/HIG/IconDesign) have some good rules for icon design. Here are a few:

* Adjust the degree of abstractness according to familiarity of the metaphor.
* Apply metaphors only once (e.g. do not use a brush twice for different options).
* Use arrows only if they can easily be related to spatial features such as Previous/Next in a sequence or Up/Down in a hierarchy. Avoid using arrows metaphorically (such as for Reply/Forward or Undo/Redo).
* Use consistent rules for placing text next to icons ([see examples here](https://community.kde.org/KDE_Visual_Design_Group/HIG/IconsAndText)).
* Icons that lose details when shrunk may need a special version that preserves meaning even at smaller sizes. Critical details may become unrecognizable when scaled down.
* Avoid using text in icon designs; it may not scale well to smaller sizes.

Here are a few other recommended best practices:

* Follow conventions. Don't create new metaphors when familiar ones exist. [*(GNOME Human Interface Guidelines)*](https://developer.gnome.org/hig/stable/icons-and-artwork.html.en)
* Always accompany icons with text labels unless the icon metaphors are nearly universally recognized (e.g., home, print, search), which is rare. [*(Nielsen Norman Group)*](https://www.nngroup.com/articles/icon-usability/), [*(Axess Lab)*](https://axesslab.com/icons-ruining-interfaces/)
* Don't use icons that are commonly associated with a different meaning. [*(Nielsen Norman Group)*](https://www.nngroup.com/articles/bad-icons/)
* Establish color and design rules for icons and apply them consistently. See the [Google Material Design guidelines](https://material.io/guidelines/style/icons.html) for a good example.
* Apply [tooltips](../tooltips/) for additional information or when labels aren't used.

Lastly, [this article on different ways of mapping icons to the ideas you want to convey](https://www.nngroup.com/articles/classifying-icons/) is another useful resource.

### Basic Usage

![](//media.balsamiq.com/img/support/tutorials/ui101/icons.png)

---

## Types of Icons

### States

![](//media.balsamiq.com/img/support/tutorials/ui101/icons-states.png)

Icons often have "on" and "off" variants that are used to indicate those respective states. Clicking or tapping will toggle them. A common example is switching between "liking" and "unliking" something. [Badges](https://docs.microsoft.com/en-us/windows/uwp/design/style/icons#badges) can also be overlaid on top of icons to indicate a more complex state.


### Variations

Aside from a simpler version of icons, called [badges](https://docs.microsoft.com/en-us/windows/uwp/design/style/icons#badges), most variations in icons come from their look and feel. Some are monochromatic and simple, others are bright and intricate. They can use a ["filled" or "outline/hollow" style](https://twolfson.com/2016-03-22-design-theory-filled-vs-hollow-icons). The most important thing is that they are consistently styled and quick to grasp.

---

## Related Controls

* [Buttons](../buttons/)
* [Tooltips](../tooltips/)
