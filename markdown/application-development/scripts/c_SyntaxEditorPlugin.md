---
title: Syntax editor plugin
description: Enable the syntax editor plugin to use the syntax editor.
locale: en-US
release: xanadu
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [JavaScript syntax editor, Scripting, Building pro-code applications, Developing your application, Building applications]
---

# Syntax editor plugin

Enable the syntax editor plugin to use the syntax editor.

The syntax editor enables the following features for all script fields:

-   JavaScript syntax coloring, indentation, line numbers, and automatic creation of closing braces and quotes
-   Code editing functions
-   Code syntax checking
-   Script macros for common code shortcuts

![Edit JavaScript syntax](../image/JavaScriptSyntaxEditor.png "JavaScript syntax editor")

The syntax editor can be disabled or enabled by modifying the **glide.ui.javascript\_editor** property in the sys\_properties.list. In addition, administrators can configure the syntax editor to show error and warning indicators next to a line of code that contains an error by modifying the **glide.ui.syntax\_editor.show\_warnings\_errors** property. For information on the sys\_properties.list, refer to [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

**Note:** Administrators can disable or enable the syntax editor for all users, regardless of user preference.

-   **[Syntax editor JavaScript support](../reference/r_EdtJvaScptWSyntxEdtr.md)**  
The syntax editor provides editing functions to support editing JavaScript scripts.
-   **[Syntax editor keyboard shortcuts and actions](../reference/r_SyntxEdtrKybrdSrtctsActn.md)**  
The syntax editor offers keyboard shortcuts and actions to assist in writing code.
-   **[Syntax editor macros](../reference/r_SyntaxEditorMacros.md)**  
Script macros provide shortcuts for typing commonly used code. To insert macro text into a script field, enter the macro keyword followed by the Tab.
-   **[Create or modify a script macro](../task/t_ManageScriptMacros.md)**  
Administrators can define new script macros or modify existing script macros.

**Parent Topic:**[JavaScript syntax editor](c_SyntaxEditor.md)

