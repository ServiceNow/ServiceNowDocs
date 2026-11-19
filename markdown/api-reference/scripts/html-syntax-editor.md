---
title: HTML syntax editor
description: The HTML syntax editor provides support for editing HTML and Jelly scripts and defines what's rendered when the page is displayed. The HTML syntax editor can contain either static XHTML or dynamically generated content defined as Jelly, and can call script includes and UI Macros.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/scripts/html-syntax-editor.html
release: zurich
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2025-07-31"
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

\[Omitted image "HTMLSyntaxEditor.png"\] Alt text: Syntax editor for HTML and Jelly scripts.

<table id="table_cwn_f3t_3hb"><thead><tr><th>

Icon

</th><th>

Keyboard shortcut

</th><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\[Omitted image "toggle-syntax-editor.png"\] Alt text: Toggle syntax editor icon

</td><td>

N/A

</td><td>

Toggle syntax editor

</td><td>

Disables the syntax editor. Click the Toggle syntax editor icon \(\[Omitted image "toggle-syntax-editor.png"\] Alt text: Toggle syntax editor icon\) again to enable the syntax editor.

</td></tr><tr><td>

\[Omitted image "toggle-comment.png"\] Alt text: Toggle comment icon

</td><td>

Cmd+/

</td><td>

Toggle comment

</td><td>

Comments the selected code.

</td></tr><tr><td>

\[Omitted image "replace-html-syn-editor.png"\] Alt text: Replace icon

</td><td>

Cmd+E

</td><td>

Replace

</td><td>

Replaces the next occurrence of a text string in the script field.1.  Click the Replace icon \(\[Omitted image "replace-html-syn-editor.png"\] Alt text: Replace icon\), then enter the string to replace, and press Enter. You can use regular expressions enclosed in slashes to define the string to replace. For example, the term `/a{3}/` locates `aaa`.
2.  Enter the replacement string and press Enter.

</td></tr><tr><td>

\[Omitted image "replace-all.png"\] Alt text: Replace all icon

</td><td>

Cmd

</td><td>

Replace All

</td><td>

Replaces all occurrences of a text string in the script field.1.  Click the Replace all icon \(\[Omitted image "replace-all.png"\] Alt text: Replace all icon\), then enter the string to replace and press Enter. You can use regular expressions enclosed in slashes to define the string to replace. For example, the term `/a{3}/` locates `aaa`.
2.  Enter the replacement string and press Enter.

</td></tr><tr><td>

\[Omitted image "start-searching.png"\] Alt text: Start searching icon

</td><td>

Cmd+F

</td><td>

Start Searching

</td><td>

Highlights all occurrences of a search term in the script field and locates the first occurrence. Click the Start searching icon \(\[Omitted image "start-searching.png"\] Alt text: Start searching icon\), then enter the search term and press Enter.

</td></tr><tr><td>

\[Omitted image "find-next.png"\] Alt text: Find next icon

</td><td>

Cmd+G

</td><td>

Find Next

</td><td>

Locates the next occurrence of the current search term in the script field. Click the Start searching icon \(\[Omitted image "start-searching.png"\] Alt text: Start searching icon\) to change the current search term.

</td></tr><tr><td>

\[Omitted image "find-previous.png"\] Alt text: Find previous icon

</td><td>

Cmd+Shift+G

</td><td>

Find Previous

</td><td>

Locates the previous occurrence of the current search term in the script field. Click the Start searching icon \(\[Omitted image "start-searching.png"\] Alt text: Start searching icon\) to change the current search term.

</td></tr><tr><td>

\[Omitted image "toggle-full-screen.png"\] Alt text: Toggle full screen icon

</td><td>

Ctrl+M

</td><td>

Toggle Full Screen

</td><td>

Expands the script field to use the full form view for easier editing. Click the Toggle full screen icon \(\[Omitted image "toggle-full-screen.png"\] Alt text: Toggle full screen icon\) again to return to standard form view. This feature is not available for Internet Explorer.

</td></tr><tr><td>

\[Omitted image "help-html-syn-editor.png"\] Alt text: Help icon

</td><td>

Cmd+H

</td><td>

Help

</td><td>

Displays the keyboard shortcuts help screen.

</td></tr><tr><td>

\[Omitted image "save.png"\] Alt text: Save icon

</td><td>

N/A

</td><td>

Save

</td><td>

Saves changes without leaving the current view. Click the Save icon \(\[Omitted image "save.png"\] Alt text: Save icon\) in full screen mode to save without returning to standard form view.

</td></tr></tbody>
</table>## Editing tips

-   To insert a fixed space anywhere in your code, press Tab.
-   To indent a single line of code, click in the leading white space of the line and then press Tab.
-   To indent one or more lines of code, select the code and then press Tab. To decrease the indentation, press Shift+Tab.
-   To remove one tab from the start of a line of code, click in the line and press Shift+Tab.

**Parent Topic:**[Scripting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/scripts/c_Script.md)

