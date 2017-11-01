---
title: '"Project Archive Not Supported" Error After Uploading a Project to Atlassian Cloud'
date: '2015-05-09T14:46:35.000+00:00'
weight: 200
menu:
  menuplugins:
    weight: 200
draft: ''

---

If you upload an existing project to one of our Atlassian Cloud plugins, you may run into this error.

![](https://media.balsamiq.com/img/support/docs/atlassian/bmpr2_not_supported.png)

So what can you do to fix that?

### Let Us Convert the Project for You

The easiest way to fix this compatability error is to [send us the .bmpr file](mailto:support@balsamiq.com). We can convert it quickly, and send it back to you.

### Export the Project as a Zip File

If you prefer to convert the file yourself (or are unable to send it to us for privacy reasons), you can do it by opening the project (.bmpr file) in Mockups 3 for Desktop. You can download a free 30-day trial for Mockups 3 from Desktop [here](https://balsamiq.com/download).

When the project is open, you can export it as a BMML Zip file by selecting **Project > Export > Project to BMMLs Zip...**.

![](https://media.balsamiq.com/img/support/docs/atlassian/export_to_zip.png)

Once you have the exported zip file, create a new Balsamiq project in your Atlassian Cloud instance. When the Mockups editor loads, you can import the zip file by selecting **Project > Import > Project from BMMLs Zip**.

![](https://media.balsamiq.com/img/support/docs/atlassian/import_from_zip.png)

Browse to the .zip file that you exported earlier and select it. The file will be uploaded and converted to a proper project file.

![](https://media.balsamiq.com/img/support/docs/atlassian/import_successful.png)

That's it! The file has been converted.

## Will It Be like This Forever?

Absolutely not, and we are really sorry that there has been a hiccup in BMPR compatability. The reason for it is BMPRs created by our Desktop and Balsamiq Wireframe applications have support for upcoming features baked into them. Unfortunately, our Atlassian Cloud plugins don't know how to handle these new features yet, and cannot open the new project files.

The good news is that we have an update in the works to bring these features to our Atlassian Cloud plugins. Keep an eye on [our blog](http://blog.balsamiq.com/) for release announcements. Once we have the update ready, we will announce it there!
