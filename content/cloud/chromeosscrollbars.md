---
title: Is there a problem with scrollbars on ChromeOS?
date: '2015-05-09T14:46:35.000+00:00'
weight: 30
menu: menucloud
product: "Balsamiq Cloud"
draft: ''
---

Yes! But there are workarounds.
* * *

## The problem

An update to ChromeOS in August last year changed the default behavior of scrollbars. The new behavior is to hide them by default and expand them only when the mouse moves over them or when scrolling using the mouse wheel or two-finger scrolling on devices with a trackpad.

The problem is made worse by reports of different behavior on different hardware. You can read the full background of the issue in this discussion: [My scroll bar disappears](https://bugs.chromium.org/p/chromium/issues/detail?id=761237).

* * *

## Solutions and workarounds

The Google product forums have provided some help and 4 methods to workaround the issue. The full document is: [New Scrollbars in Version 60](New Scrollbars in Version 60)

1. Switch to using a touchpad rather than an external mouse. This may be an impractical option at best for some users. Two-finger scrolling in both Mac OSX and Windows involves swiping up and down the pad with two fingers instead of the usual one to move the mouse cursor.

2. Via the keyboard

	![keys for scrolling](https://lh6.googleusercontent.com/56ZwJV4LeUot2Wu-Fj1S7oshCC14sFLafYdaGN-MqA0XcPbvUU5PW9ERdVT_307QRPJP7fpBxiZZtLvWV9iEK0t2FH5e081dZANq7BEQC7ceqYSbFyTW0IXcUYOkC4H9oh-9mvUv)

3. Change scrollbar behavior using an extension: [chrome webstore search: scrollbars](https://chrome.google.com/webstore/search/scrollbars?_category=extensions)

4. Change scrollbar behavior using a flag

	Paste `chrome://flags/#overlay-scrollbars` into the Chrome address bar. Set to ‘Disable’ and then click ‘Restart Now’.
	
	Note this approach is not recommended as the flag in question may be removed at any time, making this an unreliable option.

* * *

We hope that these tips will resolve any issues you are having with scrollbars while using Cloud. However, don't hesitate to reach out to us via [support@balsamiq.com](mailto:support@balsamiq.com) if needed. We're here to help! :)
