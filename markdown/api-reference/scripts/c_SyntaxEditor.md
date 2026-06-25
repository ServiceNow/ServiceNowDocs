---
title: JavaScript syntax editor
description: The syntax editor provides support for editing JavaScript scripts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/api-reference/scripts/c\_SyntaxEditor.html
release: xanadu
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Scripting, API implementation, API implementation and reference]
---

# JavaScript syntax editor

The syntax editor provides support for editing JavaScript scripts.

The syntax editor has these features.

-   JavaScript syntax coloring, indentation, line numbers, and automatic creation of closing braces and quotes
-   JavaScript support
-   Linting using the ESLint utility

    **Note:** Modify or view default linting configurations by accessing the **glide.ui.syntax\_editor.linter.eslint\_config** property in the System Property \[sys\_properties\] table. See [Available system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/platform-administration/r_AvailableSystemProperties.md) for more information.

-   Context menu for script includes, API, and tables
-   Script macros for common code shortcuts

This feature requires the Syntax Editor \(com.glide.syntax\_editor\) plugin.

\[Omitted image "JavaScriptSyntaxEditor.png"\] Alt text: JavaScript editor

-   **[Syntax editor plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/api-reference/scripts/c_SyntaxEditorPlugin.md)**  
Enable the syntax editor plugin to use the syntax editor.
-   **[Context menu in the syntax editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/api-reference/scripts/context-menu-syntax-editor.md)**  
View the context menu for script includes, Glide APIs, and tables in the JavaScript syntax editor.
-   **[Script syntax error checking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/api-reference/scripts/c_ScriptSyntaxErrorChecking.md)**  
All script fields provide controls for checking the syntax for errors and for locating the error easily when one occurs. The script editor places the cursor at the site of a syntax error and lets you search for errors in scripts by line number.
-   **[Searching for errors by line](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/api-reference/scripts/c_SearchingForErrorsByLine.md)**  
To locate the exact position of the error in a large script, click the **Go to line** icon.

**Parent Topic:**[Scripting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/api-reference/scripts/c_Script.md)

