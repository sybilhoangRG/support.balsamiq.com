---
title: Updating from Old Versions of Confluence Server
date: '2015-05-09T14:46:00+00:00'
weight: '150'
menu:
  menuplugins:
    weight: 150
draft: ''

---

Due to changes Atassian made to macro handling, updating versions of Confluence prior to 3.5.7 is not a cut-and-dry process (as much as we wish it were!)

{{% alert info %}}**Note:** In order to update to the latest version of Balsamiq for Confluence Server, you'll need to make sure your license has an [active maintenance period](/sales/maintenance/).{{% /alert %}}

Here are the steps for updating your Confluence server to ensure that Balsamiq for Confluence updates smoothly:

1. Update your Confluence server to 3.5.7 (if you have already updated past this, you'll have to downgrade to 3.5.7 temporarily)
2. Then, update your Confluence server to 4.3.7 (this should update your macros correctly)
3. Install Mockups for Confluence Server version 2.2.10 which you can [download here](https://marketplace.atlassian.com/apps/256/balsamiq-wireframes-confluence-server/versions).
4. Once Mockups 2.2.10 is installed, you can safely update your Confluence server to the latest version.
5. After your Confluence server has been updated, you can also update Balsamiq for Confluence to the latest version.

Following these steps should allow you to gracefully update your Confluence server, and ensure that Balsamiq continues to function properly.
