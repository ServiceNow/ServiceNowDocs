---
title: Context menu in the syntax editor
description: View the context menu for script includes, Glide APIs, and tables in the JavaScript syntax editor.
locale: en-US
release: zurich
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using the JavaScript syntax editor, JavaScript syntax editor, Scripting, API implementation, API implementation and reference]
---

# Context menu in the syntax editor

View the context menu for script includes, Glide APIs, and tables in the JavaScript syntax editor.

In the syntax editor, bold font is used for tokens that have a context menu. Right-click the token to view context menu options. With the context menu options, your users can navigate to:

-   Script include definitions
-   Glide API documentation
-   System and custom table definitions and data

![The context menu options for a script include in the syntax editor.](../image/js-editor-context-menu.png "Context menu in the syntax editor")

|Token type|Context menu option|Description|
|----------|-------------------|-----------|
|Script include|Open Definition|Opens the definition of the script include in a new window.|
|Script include|Find References|Displays a list of all files referencing the script include. You can preview the file or open the file in a new window.|
|Glide API|Show Documentation|Opens the API reference documentation for the Glide API in a new window.|
|Table|Show Definition|Opens the definition of the system or custom table in a new window.|
|Table|Show Data|Displays records in the table that are based on the role of the current user.|

You can configure whether to show the context menu in the syntax editor with the **glide.ui.syntax\_editor.context\_menu** system property.

**Note:** Context menu options can be accessed only if the browser supports SharedWorker, such as Google Chrome and Mozilla Firefox.

**Parent Topic:**[Using the JavaScript syntax editor](../reference/r_EdtJvaScptWSyntxEdtr.md)

