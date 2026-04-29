---
title: HTML syntax editor
description: The HTML syntax editor provides support for editing HTML and Jelly scripts and defines what's rendered when the page is displayed. The HTML syntax editor can contain either static XHTML or dynamically generated content defined as Jelly, and can call script includes and UI Macros.
locale: en-US
release: australia
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Scripting, API implementation, API implementation and reference]
---

# HTML syntax editor

The HTML syntax editor provides support for editing HTML and Jelly scripts and defines what's rendered when the page is displayed. The HTML syntax editor can contain either static XHTML or dynamically generated content defined as Jelly, and can call script includes and UI Macros.

The syntax editor has these features.

-   HTML and Jelly script support
-   HTML and Jelly syntax coloring, indentation, line numbers, and automatic creation of closing braces and quotes
-   Auto-suggestions for HTML and Jelly tags
-   Script macros for common code shortcuts

![Syntax editor for HTML and Jelly scripts.](../image/HTMLSyntaxEditor.png "HTML syntax editor")

<table id="table_cwn_f3t_3hb"><thead><tr><th>

Icon

</th><th>

Keyboard shortcut

</th><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

![Toggle syntax editor icon](../image/toggle-syntax-editor.png)

</td><td>

N/A

</td><td>

Toggle syntax editor

</td><td>

Disables the syntax editor. Click the Toggle syntax editor icon \(![Toggle syntax editor icon](../image/toggle-syntax-editor.png)\) again to enable the syntax editor.

</td></tr><tr><td>

![Toggle comment icon](../image/toggle-comment.png)

</td><td>

Cmd+/

</td><td>

Toggle comment

</td><td>

Comments the selected code.

</td></tr><tr><td>

![Replace icon](../image/replace-html-syn-editor.png)

</td><td>

Cmd+E

</td><td>

Replace

</td><td>

Replaces the next occurrence of a text string in the script field.1.  Click the Replace icon \(![Replace icon](../image/replace-html-syn-editor.png)\), then enter the string to replace, and press Enter. You can use regular expressions enclosed in slashes to define the string to replace. For example, the term `/a{3}/` locates `aaa`.
2.  Enter the replacement string and press Enter.

</td></tr><tr><td>

![Replace all icon](../image/replace-all.png)

</td><td>

Cmd

</td><td>

Replace All

</td><td>

Replaces all occurrences of a text string in the script field.1.  Click the Replace all icon \(![Replace all icon](../image/replace-all.png)\), then enter the string to replace and press Enter. You can use regular expressions enclosed in slashes to define the string to replace. For example, the term `/a{3}/` locates `aaa`.
2.  Enter the replacement string and press Enter.

</td></tr><tr><td>

![Start searching icon](../image/start-searching.png)

</td><td>

Cmd+F

</td><td>

Start Searching

</td><td>

Highlights all occurrences of a search term in the script field and locates the first occurrence. Click the Start searching icon \(![Start searching icon](../image/start-searching.png)\), then enter the search term and press Enter.

</td></tr><tr><td>

![Find next icon](../image/find-next.png)

</td><td>

Cmd+G

</td><td>

Find Next

</td><td>

Locates the next occurrence of the current search term in the script field. Click the Start searching icon \(![Start searching icon](../image/start-searching.png)\) to change the current search term.

</td></tr><tr><td>

![Find previous icon](../image/find-previous.png)

</td><td>

Cmd+Shift+G

</td><td>

Find Previous

</td><td>

Locates the previous occurrence of the current search term in the script field. Click the Start searching icon \(![Start searching icon](../image/start-searching.png)\) to change the current search term.

</td></tr><tr><td>

![Toggle full screen icon](../image/toggle-full-screen.png)

</td><td>

Ctrl+M

</td><td>

Toggle Full Screen

</td><td>

Expands the script field to use the full form view for easier editing. Click the Toggle full screen icon \(![Toggle full screen icon](../image/toggle-full-screen.png)\) again to return to standard form view. This feature is not available for Internet Explorer.

</td></tr><tr><td>

![Help icon](../image/help-html-syn-editor.png)

</td><td>

Cmd+H

</td><td>

Help

</td><td>

Displays the keyboard shortcuts help screen.

</td></tr><tr><td>

![Save icon](../image/save.png)

</td><td>

N/A

</td><td>

Save

</td><td>

Saves changes without leaving the current view. Click the Save icon \(![Save icon](../image/save.png)\) in full screen mode to save without returning to standard form view.

</td></tr></tbody>
</table>## Editing tips

-   To insert a fixed space anywhere in your code, press Tab.
-   To indent a single line of code, click in the leading white space of the line and then press Tab.
-   To indent one or more lines of code, select the code and then press Tab. To decrease the indentation, press Shift+Tab.
-   To remove one tab from the start of a line of code, click in the line and press Shift+Tab.

**Parent Topic:**[Scripting](../../topic/c_Script.md)

