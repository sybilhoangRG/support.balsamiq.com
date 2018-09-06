---
date: 2016-07-12T12:59:45-07:00
draft: false
title: "BMPR File Format Reference"
menu: "menuresources"
weight: 120
product: "Resources"
---

## Overview

At the heart of all Balsamiq projects are BMPR files. BMPR files (short for <strong>B</strong>alsamiq <strong>M</strong>ockups <strong>PR</strong>ojects) are a type of BAR file. BAR files, or <strong>B</strong>alsamiq <strong>Ar</strong>chive files, provide a way a storing different kinds of content while also providing a consistent set of tools for reading and writing that content.

BAR is a format for files that have resources of various types, branches, and thumbnails. For instance, one could build the next Keynote, Visio, or Photoshop using BAR as its file format. Our hope is that some day someone might want to adopt the format. If not, we'll probably adopt it ourselves for our next product.

In other words, BMPR files are a kind of BAR file. All BAR files share similar APIs describing what kind of content the archive contains.

In the case of BMPR files that content contains everthing there is to know about a Balsamiq project.

### Getting a BMPR File

If you want to get your hands on a BMPR file, create a new wireframe using Balsamiq app and save the file somewhere. That's a BMPR file. Or <a href="https://media.balsamiq.com/files/bank.bmpr">download the example</a> used for creating some of the documentation that follows.

The BMPR format isn't the first format we've used for Balsamiq. For example, in the past we've used <a href="https://docs.balsamiq.com/desktop/exporting/#exporting-for-use-in-a-previous-version">BMML</a>. A Mockups 2 project requires multiple BMML files making them a little more cumbersome to manage. A single BMPR file contains everything for a project. This single file approach makes sharing projects much easier.

### Who Is This For?

It's for you and for all the other people who are making tools that integrate with Balsamiq!

Maybe you're curious about how your projects are stored. Maybe you want to make tools that can read the files or even generate BMPR files programmatically. Maybe you want to teach a <a href="http://makezine.com/projects/building-a-doodle-bot-kit/">robot</a> how to draw your wireframes using chalk on sidewalks. We hope that happens!

### Versions

The current version of the BMPR file format is 1.2.

We use <a href="http://semver.org/">Semantic Versioning</a> (SemVar for short) for the BMPR file format. This means, among other things, that the API for version 1.2 of the file format won't change. New minor versions can change the API but will remain backwards compatible with previous versions. Major versions such as a 2.0 release will be incompatible with previous major versions.

Version 2.0 of the BMPR file format is already being worked on and will not be compatible with previous major versions. 2.0 might be the same in some ways, but it's best to assume it's not 100% compatible with 1.x versions. When version 2.0 of the format is released we'll update this reference to make the differences between versions clear.

When writing tools for the BMPR file format it's a good idea to ensure that your tools are aware of version differences. BMPR files are a type of BAR file, and all BAR files contain both the file format type (such as bmpr) and the version (1.2) that file format uses. Examples of how those details are stored can be found in the <a href="#info">INFO</a> section below.

## Details

A BMPR file is a humble SQLite database file that stores both scalar values (single numbers, strings, etc) and JSON data that describes every detail of a Balsamiq project. Using SQLite enables BMPR files to take advantage of the huge amount of historical experience, tools, and libraries for reading and writing to relational databases while also being very portable and embeddable.

Here's what a BMPR file looks like when opened using the free <a href="https://github.com/sqlitebrowser/sqlitebrowser">DB Browser for SQLite</a> app:

[![](https://media.balsamiq.com/img/support/docs/bmpr/tables.png)](https://media.balsamiq.com/img/support/docs/bmpr/tables.png)

There are 4 tables in a BMPR file:

<ul class="list-group">
  <li class="list-group-item"><a href="#info">INFO</a> contains details about what kind of resources an archive contains</li>
  <li class="list-group-item"><a href="#resources">RESOURCES</a> is where most of the content found in a project lives</li>
  <li class="list-group-item"><a href="#branches">BRANCHES</a> contains information about branches in a project</li>
  <li class="list-group-item"><a href="#thumbnails">THUMBNAILS</a> has entries for wireframe thumbnails</li>
</ul>

---

## The INFO Table

The INFO table describes what kind of data, or resources, our file contains. BMPR files are a kind of BAR file, and BAR files use the INFO table to describe what kind of data they contain. It allows developers to inspect an archive file so they can make informed decisions about how to handle the content within.

<div class="panel panel-default">
  <div class="panel-heading">Table Fields</div>
  <table class="table">
    <tbody>
      <tr>
        <th>Field</th>
        <th>Datatype</th>
        <th>Description</th>
      </tr>
      <tr>
        <td>NAME</td>
        <td>TEXT</td>
        <td>The unique name of the kind of meta data for this row. Think of this as a you would a key in structure or hash.</td>
      </tr>
      <tr>
        <td>VALUE</td>
        <td>TEXT</td>
        <td>The value for this meta data entry</td>
      </tr>
    </tbody>
  </table>
</div>

<div class="panel panel-info">
  <div class="panel-heading">Example Data</div>
  <table class="table">
    <tbody>
      <tr>
        <th>NAME</th>
        <th>VALUE</th>
      </tr>
      <tr>
        <td>SchemaVersion</td>
        <td>1.2</td>
      </tr>
      <tr>
        <td>ArchiveRevision</td>
        <td>44</td>
      </tr>
      <tr>
        <td>ArchiveRevisionUUID</td>
        <td>007F035B-6147-D643-C5CC-2871D9DA1C43</td>
      </tr>
      <tr>
        <td>ArchiveFormat</td>
        <td>bmpr</td>
      </tr>
      <tr>
        <td>ArchiveAttributes</td>
        <td>
          <div class="json-example">
{{< highlight json >}}
{
  "creationDate":1467124505618, // the date this archive file was created
  "name":"banking_interface"    // the name of the resource
}
{{< /highlight >}}
          </div>
        </td>
      </tr>
    </tbody>
  </table>
</div>

<div class="list-group">
  <div class="list-group-item">
    <h5 class="list-group-item-heading">SchemaVersion</h5>
    <p class="list-group-item-text">This is the file format version number for the kind of resource this archive contains.</p>
  </div>
  <div class="list-group-item">
    <h5 class="list-group-item-heading">ArchiveRevision</h5>
    <p class="list-group-item-text">This contains a count of how many times this archive file has been changed.</p>
  </div>
  <div class="list-group-item">
    <h5 class="list-group-item-heading">ArchiveRevisionUUID</h5>
    <p class="list-group-item-text">This is a unique ID that identifies the latest revision of this archive.</p>
  </div>
  <div class="list-group-item">
    <h5 class="list-group-item-heading">ArchiveFormat</h5>
    <p class="list-group-item-text">This indicates what kind of data this archive contains (for example, <em>bmpr</em>).</p>
  </div>
  <div class="list-group-item">
    <h5 class="list-group-item-heading">ArchiveAttributes</h5>
    <p class="list-group-item-text">This is a JSON hash containing the creation date of the file as well as a name for the contents of this archive.</p>
  </div>
</div>

---

## The RESOURCES Table

Details about wireframes, assets, and symbols are stored here. Each row in this table contains details (coordinates, shape, and size, etc.) about every element in a project.

<div class="panel panel-default">
  <div class="panel-heading">Table Fields</div>
  <table class="table">
    <tbody>
      <tr>
        <th>Field</th>
        <th>Datatype</th>
        <th>Description</th>
        <th class="example">Example</th>
      </tr>
      <tr>
        <td>ID</td>
        <td>TEXT</td>
        <td><p>A unique id for a resource</p></td>
        <td><code>ADC6E183-B52E-038A-1BBC-DAEDBAE75554</code></td>
      </tr>

      <tr>
        <td>BRANCHID</td>
        <td>TEXT</td>
        <td><p>The branch this resource belongs to</p></td>
        <td><code>Master</code></td>
      </tr>
      <tr>
        <td>ATTRIBUTES</td>
        <td>TEXT</td>
        <td colspan="2">
          <p>JSON data with keys for <em>creationDate</em>, <em>thumbnailID</em>, <em>kind</em>, <em>modifiedBy</em>, <em>notes</em>, <em>mimeType</em>, <em>order</em>, <em>name</em>, <em>importedFrom</em>, <em>parentID</em>, and <em>trashed</em></p>
        </td>
      </tr>
      <tr>
        <td colspan=4 class="json-example">
          <p><strong>Example:</strong></p>
{{< highlight json >}}
{
  "creationDate": 0,                    // the date this resource was created
  "importedFrom": "",                   // for imported resources this will be the original file name of that resource
  "parentID": "",                       // a unique ID that, when present, associates this resource with another resource
  "kind": "mockup",                     // the kind of resource this row describes
  "mimeType": "text/vnd.balsamiq.bmml", // the mime type for this resource
  "modifiedBy": null,                   // who (or what) last modified this resource
  "name": "Banking Website",            // the name of this resource
  "notes": "",                          // notes for this resource
  "order": 2445916,                     // an absolute integer representing this resource's position
  "thumbnailID": "[UUID]",              // the unique ID of the thumbnail for this wireframe
  "trashed": false                      // a boolean flag indicating if this is a trashed resource
}
{{< /highlight >}}

        {{% alert info %}}The _order_ key is only present when the resource is a **mockup**.{{% /alert %}}
        </td>
      </tr>
      <tr>
        <td>DATA</td>
        <td>TEXT</td>
        <td>
          <p>JSON data with keys for wireframe data. See below for more details.</p>
          <p>If the resource is a kind of <strong>otherAsset</strong> or <strong>asset</strong> the data stored for this resource will be the Base64 encoded representation of the asset.</p>
        </td>
        <td>&nbsp;</td>
      </tr>
      <tr>
        <td colspan=4 class="json-example">
          <p><strong>Example:</strong></p>
{{< highlight json >}}
{
  "mockup": {
    "controls": {        // an array containing each element (see more about this below)
      "control": ["..."] // JSON data with properties unique to the control type
    },
    "measuredH": "600",  // the pixel height of the wireframe
    "measuredW": "800",  // the pixel width of the wireframe
    "version": "1.0"     // the version for this particular resource
  }
}
{{< /highlight >}}
        </td>
      </tr>
    </tbody>
  </table>
</div>

<p>Stored resources share some common keys. The first 10 keys in the following example will be the same for any kind of <strong>mockup</strong> or <strong>symbol</strong> resource.</p>

<div class="json-example">
{{< highlight json >}}
{
  "typeID": "DataGrid", // the type of element this is (ie. DataGrid, or TabBar)
  "ID": "2",            // a unique integer for this resource
  "h": "319",           // the pixel height of this resource
  "w": "739",           // the pixel width of this resource
  "x": "30",            // the x position of this resource
  "y": "257",           // the y position of this resource
  "zOrder": "17",       // the position of this resource, front to back
  "properties": {       // resource type specific properties
    "hLines": "false",
    "selectedIndex": "0",
    "size": "14",
    "text": "[CSV formatted data for this DataGrid]",
    "vLines": "true",
    "verticalScrollbar": "true"
  }
}
{{< /highlight >}}
</div>

<p>Each different kind of resource will have properties that are specific to that kind of resource. Note how the highlighted keys within <em>properties</em> differ between the example above and below:</p>

<div class="json-example">
{{< highlight json "hl_lines=12 13 14 15 16">}}
{
  "typeID": "TabBar",
  "ID": "7",
  "h": "535",
  "w": "769",
  "x": "15",
  "y": "52",
  "measuredH": "100",
  "measuredW": "241",
  "zOrder": "2",
  "properties": {
    "borderStyle": "square",
    "color": "15658734",
    "selectedIndex": "0",
    "tabHPosition": "center",
    "text": "[Comma separated list of tab names]"
  }
}
{{< /highlight >}}
</div>

<p>Each Symbol Library that's been added to a project has its own RESOURCE record with JSON data describing all of the controls that that library makes available. Each instance of a control used in a wireframe is described in the JSON within the DATA column for a wireframe's RESOURCE record.</p>

<p>Documenting each different kind of resources, each with their own set of properties, is well beyond the scope of this reference. Knowing the purpose of their common keys should at least provide a foundation for understanding each different kind.</p>

---

## The BRANCHES Table

The branches table contains records for each branch in a project. A typical project will contain a "Master" branch at the very least.

<div class="panel panel-default">
  <div class="panel-heading">Table Fields</div>
    <table class="table">
      <tbody>
      <tr>
        <th>Field</th>
        <th>Datatype</th>
        <th>Description</th>
      </tr>
      <tr>
        <td>ID</td>
        <td>TEXT</td>
        <td>A unique id for a branch</td>
      </tr>
      <tr>
        <td>ATTRIBUTES</td>
        <td>TEXT</td>
        <td>JSON data. Keys depend on whether the record is for a Master branch or alternate branch.</td>
      </tr>
      <tr>
        <td colspan=3 class="json-example">
          <p><strong>Master branch example:</strong></p>
{{< highlight json >}}
{
  "branchDescription":"",       // this is here for possible future use
  "creationDate":1467124505618, // the date this branch was created
  "fontFace":"Chalkboard",      // the name of the font that will be used throughout the project
  "fontSize":16,                // the size of the font that will be used throughout the project
  "linkColor":545684,           // the color used for links throughout the project
  "modifiedBy":[],              // what populates this?
  "projectDescription":"",      // the description for the project
  "selectionColor":9813234,     // the color used for selections throughout the project
  "skinName":"sketch",          // the name of the skin to use throughout the project
  "symbolLibraryID":""          // a unique id for the symbol library used throughout the project
}
{{< /highlight >}}

          <p><strong>An alternate branch example:</strong></p>
{{< highlight json >}}
{
  "branchName":"alt" // the name of an alternate branch
}
{{< /highlight >}}
        </td>
      </tr>
    </tbody>
  </table>
</div>

<div class="panel panel-info">

  <div class="panel-heading">
    <h3 class="panel-title">Things to know about branches and alternates:</h3>
  </div>

  <div class="panel-body">
    <p>Balsamiq doesn't use terms like "branchName" - it uses alternate versions. You can read more about <a href="https://docs.balsamiq.com/desktop/alternates/" class="alert-link">alternate versions here</a>.</p>
    <div class="row">
      <div class="col-sm-6 col-md-4">
        <div class="thumbnail">
          [![](https://media.balsamiq.com/img/support/docs/bmpr/alternate_1_thumbnail.png)](https://media.balsamiq.com/img/support/docs/bmpr/alternate_1.png)
          <div class="caption">
            This is the "master" alternate. Its ID in the <em>BRANCHES</em> table is "master", but it has no "branchName" key or value in the ATTRIBUTES column. That's because the master branch name can't be changed. Balsamiq will always refer to it as "Official Version".
          </div>
        </div>
      </div>
      <div class="col-sm-6 col-md-4">
        <div class="thumbnail">
          [![](https://media.balsamiq.com/img/support/docs/bmpr/alternate_2_thumbnail.png)](https://media.balsamiq.com/img/support/docs/bmpr/alternate_2.png)
          <div class="caption">
            This an alternate of the official version. Its ID is an automatically generated UUID and its "branchName" in the ATTRIBUTES column is "Unofficial Version" - its name is editable since it's not the master branch.
          </div>
        </div>
      </div>
      <div class="col-sm-6 col-md-4">
        <div class="thumbnail">
          [![](https://media.balsamiq.com/img/support/docs/bmpr/alternate_3_thumbnail.png)](https://media.balsamiq.com/img/support/docs/bmpr/alternate_3.png)
          <div class="caption">
            This is another alternate. Its ID is an automatically generated UUID and its "branchName" in the ATTRIBUTES column is "Work in Progress Version".
          </div>
        </div>
      </div>
    </div>
    <p>Changes made to things like fonts, link colors, project descriptions on an alternative branch are actually made to the **Master** branch. Alternative branches inherit these properties from the **Master** branch, which is why alternative branches only contain a **branchName**.</p>
    <div class="row">
      <div class="col-sm-6 col-md-6">
        <div class="thumbnail">
          [![](https://media.balsamiq.com/img/support/docs/bmpr/master_with_new_font_changes_thumbnail.png)](https://media.balsamiq.com/img/support/docs/bmpr/master_with_new_font_changes.png)
          <div class="caption">
            In this screenshot of Balsamiq we're picking a new font and changing the link colors to red on one alternate.
          </div>
        </div>
      </div>
      <div class="col-sm-6 col-md-6">
        <div class="thumbnail">
          [![](https://media.balsamiq.com/img/support/docs/bmpr/alternate_showing_font_changes_thumbnail.png)](https://media.balsamiq.com/img/support/docs/bmpr/alternate_showing_font_changes.png)
          <div class="caption">
            Those font changes apply to both the original alternate as well as all other alternates.
          </div>
        </div>
      </div>
    </div>
    <p>Here what the data looks like when the font is changed for an alternate:</p>
    <img src="https://media.balsamiq.com/img/support/docs/bmpr/sqlite_master_branch_attributes_highlighted.png" />
    <p>That font setting is applied to the master branch, as seen here:</p>
    <img src="https://media.balsamiq.com/img/support/docs/bmpr/sqlite_branches_table.png" />
  </div>
</div>

---


## The THUMBNAILS Table

<p>Every Balsamiq project has thumbnails of the wireframes within the project. The <em>THUMBNAILS</em> table keeps track of those thumbnails.</p>

<div class="panel panel-default">
  <div class="panel-heading">Table Fields</div>
  <table class="table">
    <tbody>
      <tr>
        <th>Field</th>
        <th>Datatype</th>
        <th>Description</th>
        <th class="example">Example</th>
      </tr>
      <tr>
        <td>ID</td>
        <td>TEXT</td>
        <td>
          <p>A unique id for a thumbnail.</p>
        </td>
        <td><code>4B16F0EB-CAD0-5E34-0BD3-DAEDBAF4CAF6</code></td>
      </tr>
      <tr>
        <td>ATTRIBUTES</td>
        <td>TEXT</td>
        <td>
          <p>JSON data with keys for <em>image</em>, <em>resourceID</em>, and <em>branchID</em></p>
        </td>
        <td>&nbsp;</td>
      </tr>
      <tr>
        <td colspan=4 class="json-example">
          <p><strong>Example:</strong></p>

{{< highlight json >}}
{
  "branchID":"Master",    // this is the name of the branch this thumbnail is associated with
  "image":"[Image Data]", // contains Base64 encoded data for the thumbnail image.
  "resourceID":"[UUID]"   // this is the UUID of the wireframe this thumbnail is a snapshot of
}
{{< /highlight >}}
        </td>
      </tr>
    </tbody>
  </table>
</div>


## Summary

<p>We hope this reference is useful. If you can think of ways that would help us make it more useful for you <a href="https://balsamiq.com/company/#contact">we want to hear about it</a> and make it better. If you build a tool that supports BMPR let us know so we can tell people about it!</p>
