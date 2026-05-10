---
title: JavaScript syntax editor
description: The JavaScript syntax editor provides support for editing JavaScript scripts.
locale: en-US
release: australia
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Scripting, API implementation, API implementation and reference]
---

# JavaScript syntax editor

The JavaScript syntax editor provides support for editing JavaScript scripts.

With the JavaScript syntax editor, you can use the following features:

-   JavaScript syntax coloring, indentation, line numbers, and automatic creation of closing braces and quotes
-   Context menu for script includes, API, and tables
-   Script macros for common code shortcuts
-   Linting using the ESLint utility

![JavaScript code in the syntax editor](../image/JavaScriptSyntaxEditor.png "JavaScript syntax editor")

## Configuring the syntax editor

The Syntax Editor plugin \(com.glide.syntax\_editor\) is required to use this functionality. To configure the JavaScript syntax editor functionality on an instance, you can use the following system properties:

-   **glide.ui.javascript\_editor**: Turn on or off using the JavaScript syntax editor for script fields.
-   **glide.ui.syntax\_editor.show\_warnings\_errors**: Configure whether to show indicators next to a line of code that contains an issue for errors, warnings, both, or none.
-   **glide.ui.syntax\_editor.linter.eslint\_config**: View or modify the default linting configurations for scripts.
-   **glide.ui.syntax\_editor.linter.eslint\_config.ecmascript2021**: View or modify the default linting configurations for scripts using the ECMAScript 2021 \(ES12\) JavaScript mode.
-   **glide.ui.syntax\_editor.context\_menu**: Turn on or off showing the context menu for script includes, Glide APIs, and tables in the syntax editor.

For more information about system properties, see [Available system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md).

-   **[Using the JavaScript syntax editor](../reference/r_EdtJvaScptWSyntxEdtr.md)**  
The syntax editor provides editing functions to support editing JavaScript scripts.
-   **[Create a script macro for the syntax editor](../task/t_ManageScriptMacros.md)**  
Administrators can define new script macros or modify existing script macros.

**Parent Topic:**[Scripting](../../topic/c_Script.md)

