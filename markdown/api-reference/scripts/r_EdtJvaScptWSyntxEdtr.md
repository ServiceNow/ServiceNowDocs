---
title: Using the JavaScript syntax editor
description: The syntax editor provides editing functions to support editing JavaScript scripts.
locale: en-US
release: australia
product: Scripts
classification: scripts
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [JavaScript syntax editor, Scripting, API implementation, API implementation and reference]
---

# Using the JavaScript syntax editor

The syntax editor provides editing functions to support editing JavaScript scripts.

## JavaScript editing functions

<table id="simpletable_vx3_1sc_bq"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Toggle Syntax Editor

</td><td>

Disables the syntax editor. Click the button again to enable the syntax editor.

</td></tr><tr><td>

Format Code

</td><td>

Applies the proper indentation to the script.

</td></tr><tr><td>

Comment Selected Code

</td><td>

Comments out the selected code.

</td></tr><tr><td>

Uncomment Selected Code

</td><td>

Removes comment codes from the selected code.

</td></tr><tr><td>

Check Syntax

</td><td>

Checks the code for syntax errors. By default, the system automatically checks for syntax errors as you type in a script field. If an error or warning is found, the syntax editor displays a bullet beside the script line containing the error or warning. This check occurs on all script fields.

</td></tr><tr><td>

Start Searching

</td><td>

Highlights all occurrences of a search term in the script field and locates the first occurrence. Click the icon, then enter the search term and press **Enter**. You can use [regular expressions](http://www.regular-expressions.info/reference.html) enclosed in slashes to define the search term. For example, the term /a\{3\}/ locates aaa.

</td></tr><tr><td>

Find Next

</td><td>

Locates the next occurrence of the current search term in the script field. Use Start Searching to change the current search term.

</td></tr><tr><td>

Find Previous

</td><td>

Locates the previous occurrence of the current search term in the script field. Use Start Searching to change the current search term.

</td></tr><tr><td>

Replace

</td><td>

Replaces the next occurrence of a text string in the script field.1.  Click the icon, then enter the string to replace and press **Enter**. You can use regular expressions enclosed in slashes to define the string to replace. For example, the term /a\{3\}/ locates aaa.
2.  Enter the replacement string and press **Enter**.

</td></tr><tr><td>

Replace All

</td><td>

Replaces all occurrences of a text string in the script field.1.  Click the icon, then enter the string to replace and press **Enter**. You can use regular expressions enclosed in slashes to define the string to replace. For example, the term /a\{3\}/ locates aaa.
2.  Enter the replacement string and press **Enter**.

</td></tr><tr><td>

Save

</td><td>

Saves changes without leaving the current view. Use this button in full screen mode to save without returning to standard form view.

</td></tr><tr><td>

Toggle Full Screen Mode

</td><td>

Expands the script field to use the full form view for easier editing. Click the button again to return to standard form view. This feature is not available for Internet Explorer.

</td></tr><tr><td>

Help

</td><td>

Displays the keyboard shortcuts help screen.

</td></tr></tbody>
</table>## JavaScript editing tips

-   To fold a code block, click the minus sign beside the first line of the block. The minus sign only appears beside blocks that can be folded. To unfold the code block, click the plus sign.
-   To insert a fixed space anywhere in your code, press Tab.
-   To indent a single line of code, click in the leading white space of the line and then press Tab.
-   To indent one or more lines of code, select the code and then press Tab. To decrease the indentation, press Shift + Tab.
-   To remove one tab from the start of a line of code, click in the line and press Shift + Tab.

## JavaScript resources

Scripts use ECMA 262 standard JavaScript. Helpful resources include:

-   Mozilla: [http://developer.mozilla.org/en/docs/Core\_JavaScript\_1.5\_Reference](http://developer.mozilla.org/en/docs/Core_JavaScript_1.5_Reference)
-   ECMA Standard in PDF format: [http://www.ecma-international.org/publications/files/ECMA-ST/Ecma-262.pdf](http://www.ecma-international.org/publications/files/ECMA-ST/Ecma-262.pdf)
-   History and overview: [http://javascript.crockford.com/survey.html](http://javascript.crockford.com/survey.html)
-   JavaScript number reference: [http://www.hunlock.com/blogs/The\_Complete\_Javascript\_Number\_Reference](http://www.hunlock.com/blogs/The_Complete_Javascript_Number_Reference)

-   **[Syntax editor keyboard shortcuts and actions](r_SyntxEdtrKybrdSrtctsActn.md)**  
The syntax editor offers keyboard shortcuts and actions to assist in writing code.
-   **[JavaScript syntax editor macros](r_SyntaxEditorMacros.md)**  
Script macros provide shortcuts for typing commonly used code. To insert macro text into a script field, enter the macro keyword followed by the Tab.
-   **[Context menu in the syntax editor](../concept/context-menu-syntax-editor.md)**  
View the context menu for script includes, Glide APIs, and tables in the JavaScript syntax editor.
-   **[Syntax errors and warnings](../../debugging/concept/c_ScriptSyntaxErrorChecking.md)**  
All script fields provide controls for checking the syntax for errors and for locating the error easily when one occurs.

**Parent Topic:**[JavaScript syntax editor](../concept/c_SyntaxEditor.md)

