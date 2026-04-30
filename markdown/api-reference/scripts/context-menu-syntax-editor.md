---
title: Context menu in the syntax editor
description: View the context menu for script includes, Glide APIs, and tables in the JavaScript syntax editor.
locale: en-US
release: xanadu
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [JavaScript syntax editor, Scripting, API implementation, API implementation and reference]
---

# Context menu in the syntax editor

View the context menu for script includes, Glide APIs, and tables in the JavaScript syntax editor.

With the context menu options, your users can navigate to:

-   Script include definitions
-   Glide API documentation
-   System and custom table definitions and data

In the syntax editor, bold font is used for tokens that have a context menu. Right-click the token to view context menu options. If you use a Mac, you can use the Command-click shortcut.

<table id="table_cwh_4xj_fhb"><thead><tr><th>

Token type

</th><th>

Context menu option

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="2">

Script include

</td><td>

Open Definition

</td><td>

Definition of the script include in a new window.

</td></tr><tr><td>

Find References

</td><td>

List of files referencing the script include.**Note:**

-   To view the preview of the file, click the preview script icon ![Preview script icon](../image/preview-script.png).

To open the file in a new window, click **Open File**.

-   To view all files that reference the script include, click **Show All Files**.

</td></tr><tr><td>

Glide API

</td><td>

Show Documentation

</td><td>

Documentation page of the Glide API.

</td></tr><tr><td rowspan="2">

Table

</td><td>

Show Definition

</td><td>

Definition of the system or custom table in a new window.

</td></tr><tr><td>

Show Data

</td><td>

Records in the table that are based on the role of the current user.

</td></tr></tbody>
</table>Enable or disable the context menu in the script editor using the **glide.ui.syntax\_editor.context\_menu** property in the System Property \[sys\_properties\] table. See [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) for more information.

**Note:** Context menu options can be accessed only if the browser supports SharedWorker. For example, Google Chrome and Mozilla Firefox.

**Parent Topic:**[JavaScript syntax editor](c_SyntaxEditor.md)

