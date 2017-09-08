---
title: 'Unable to Save Project to Draft Page in Confluence'
date: '2015-05-09T14:46:35.000+00:00'
weight: 200
menu:
  menuplugins:
    weight: 210
draft: ''

---

Seeing the following error message while trying to add a Balsamiq Wireframes project to your Confluence page?

![](//media.balsamiq.com/img/support/docs/atlassian/no_draft.png)

Since we don't want to restrict access to our plugin only for Confluence 6+ users, we decided to make Balsamiq Wireframes for Confluence Server compatible with Confluence version 5.9.

The only downside is that Confluence version 5.x (and previous versions) does not allow the Balsamiq Wireframes macro to be bonded correctly to its related BMPR attached to the Confluence page.

This is why we decided to block the creation of a project on a draft page on versions 5.x and below. We've added a warning that asks the user to save the draft before creating a project.

{{% alert info %}}**Note:** There is no such limitation in Confluence version 6 (and older versions) so creating projects on a draft page won't be an issue there.{{% /alert %}}
