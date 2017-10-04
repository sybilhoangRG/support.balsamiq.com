---
title: Why Does It Look I'm Signing Into Auth0 And Not Balsamiq Cloud?
date: '2015-05-09T14:46:35.000+00:00'
weight: 10
menu:
  menucloud:
    weight: 10
draft: ''

---
When logging into Balsamiq Cloud, you might notice that the sign in screen mentions Auth0, not Balsamiq cloud.

![](https://media.balsamiq.com/img/support/docs/cloud/auth0.png)

The (short) reason for this is because we use Auth0.com to provide authentication for our Balsamiq Cloud customers.

The longer reason is that authentication and login security are really hard! Rather than split our resources to handle it, we have decided to entrust Auth0 with it because authentication is the only thing that they do. They have become the industry standard when it comes to authentication libraries and they authenticate more than one billion logins a month. They have invested way more than what we could do on our own.

We would like Google to allow us to specify balsamiq.cloud on that dialog boss but, at the moment, that [is not possible](https://community.auth0.com/questions/3724/in-social-registration-is-there-any-way-to-change).

If you have _any_ questions or concerns about this, please don't hesitate to [get in touch](mailto:support@balsamiq.com). We take security very seriously and want to make sure you feel secure in Balsamiq Cloud!
