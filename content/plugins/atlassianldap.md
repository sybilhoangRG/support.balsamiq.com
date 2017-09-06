---
title: How to Use Both the Confluence Server and JIRA Server Plugins and Manage My Users
  via LDAP
date: '2015-05-09T14:46:35.000+00:00'
weight: 100
menu:
  menuplugins:
    weight: 100
draft: ''

---

This article is for IT administrators whose companies:

*   bought both Balsamiq for Confluence Server and Balsamiq for JIRA Server
*   do not use the built-in user management of Confluence and JIRA

## How Does Plugin Authentication Work in General?

As specified in our [Confluence Server Admin Guide](https://docs.balsamiq.com/confluence/server/wireframes/admin-guide/) and in our [JIRA Server Admin Guide](https://docs.balsamiq.com/JIRA/server/wireframes/admin-guide/) the plugin looks for a user group called _balsamiq-wireframes-editors_ to decide which users should have access to create and edit wireframes.

{{% alert info %}}**Note:** If you are using an older version of Mockups for Atlassian Server, the group name will be _balsamiq-mockups-editors_ {{% /alert %}}

## What If I Want My JIRA Server Editor Group and My Confluence Server Editor Group to Be Separate?

Say you bought a 10-editor license of Balsamiq for Confluence Server and a 3-editor license of Balsamiq for JIRA Server.

If you added your 10 wiki editors to the balsamiq-wireframes-editors group, the JIRA Server plugin would complain that you're going over your 3-user limit.

There is a solution to this tricky problem!

1.  Delete the _balsamiq-wireframes-editors_ group
2.  Create a new _balsamiq-wireframes-editors-confluence_ group and add your chosen wiki editors to it
3.  Create a new _balsamiq-wireframes-editors-jira_ group and add your chosen bug tracker editors to it

That's it! Each plugin will now look at its own group, and live happily ever after. :)
