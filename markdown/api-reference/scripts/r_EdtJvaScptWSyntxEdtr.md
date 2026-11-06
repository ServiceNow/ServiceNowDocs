---
title: Using the JavaScript syntax editor
description: The syntax editor provides editing functions to support editing JavaScript scripts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/api-reference/scripts/r\_EdtJvaScptWSyntxEdtr.html
release: australia
product: Scripts
classification: scripts
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [JavaScript syntax editor, Explore, Scripting, API implementation, API implementation and reference]
---

# Using the JavaScript syntax editor

The syntax editor provides editing functions to support editing JavaScript scripts.

## Syntax editor functions

**Tip:** For available keyboard shortcuts, select the **Help** icon \[Omitted image "help-html-syn-editor.png"\] Alt text:.

<table id="simpletable_vx3_1sc_bq"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Turn on ECMAScript 2021 \(ES12\) mode

</td><td>

Enables using the latest JavaScript features supported with ECMAScript 2021 \(ES12\) mode. This option is read only for scripts in applications with the JavaScript mode set to ECMAScript 2021 \(ES12\), which automatically use ECMAScript 2021 \(ES12\). For more information, see [Turn on ECMAScript 2021 \(ES12\) mode for a script](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/scripts/set-es12-mode-scripts.md).

</td></tr><tr><td>

Toggle Syntax Editor

</td><td>

Turns off the syntax editor. Select the button again to enable the syntax editor.

</td></tr><tr><td>

Toggle Comment

</td><td>

Comments out the selected code. Select the button again to remove the comment and leave the code.

</td></tr><tr><td>

Format Code

</td><td>

Applies the proper indentation to the script.

</td></tr><tr><td>

Replace

</td><td>

Replaces the next occurrence of a text string in the script field.1.  Select the icon, then enter the string to replace and press **Enter**. You can use regular expressions enclosed in slashes to define the string to replace. For example, the term /a\{3\}/ locates aaa.
2.  Enter the replacement string and press **Enter**.

</td></tr><tr><td>

Replace All

</td><td>

Replaces all occurrences of a text string in the script field.1.  Select the icon, then enter the string to replace and press **Enter**. You can use regular expressions enclosed in slashes to define the string to replace. For example, the term /a\{3\}/ locates aaa.
2.  Enter the replacement string and press **Enter**.

</td></tr><tr><td>

Start Searching

</td><td>

Highlights all occurrences of a search term in the script field and locates the first occurrence. Select the icon, then enter the search term and press **Enter**. You can use [regular expressions](http://www.regular-expressions.info/reference.html) enclosed in slashes to define the search term. For example, the term /a\{3\}/ locates aaa.

</td></tr><tr><td>

Find Next

</td><td>

Locates the next occurrence of the current search term in the script field. Use Start Searching to change the current search term.

</td></tr><tr><td>

Find Previous

</td><td>

Locates the previous occurrence of the current search term in the script field. Use Start Searching to change the current search term.

</td></tr><tr><td>

Toggle Full Screen

</td><td>

Expands the script field to use the full form view for easier editing. select the button again to return to standard form view. This feature is not available for Internet Explorer.

</td></tr><tr><td>

Help

</td><td>

Displays the keyboard shortcuts help screen.

</td></tr><tr><td>

Save

</td><td>

Saves changes without leaving the current view. Use this button in full screen mode to save without returning to standard form view.

</td></tr><tr><td>

Toggle Check Syntax

</td><td>

Checks the code for syntax errors. By default, the system automatically checks for syntax errors as you type in a script field. If an error or warning is found, the syntax editor displays a bullet beside the script line containing the error or warning. This check occurs on all script fields.

</td></tr><tr><td>

Open Script Debugger

</td><td>

Opens the Script Debugger window to debug the script. For more information, see [Script Debugger and Session Log](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/scripts/script-debugger.md).

</td></tr><tr><td>

Toggle Script Tree

</td><td>

Opens the Script Tree with the available APIs.

</td></tr></tbody>
</table>## Coding keyboard shortcuts and actions

The syntax editor offers keyboard shortcuts and actions to assist in writing code.

<table id="table_wmy_bpl_ss"><thead><tr><th>

Keyboard shortcut or action

</th><th>

Description

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Scripting assistance

 Control+Spacebar

</td><td>

Displays a list of valid elements at the insertion point such as:

-   Class names
-   Function names
-   Object names
-   Variable names

 Select an entry to add it to the script.

**Note:** The elements are based on server or client type of script. However, these elements are available based on the UI type you select. For example, spUtil is available for Service Portal client scripts and g\_navigation is available for Desktop scripts.

</td><td>

\[Omitted image "ScriptingAssistanceSuggestions.png"\] Alt text: A line of code for a variable definition with a pop-up window displaying potential scripting elements.

</td></tr><tr><td>

Enter a period character after a valid class name.

</td><td>

Displays a list methods for the class.

 Double-click an entry to add it to the script.

</td><td>

\[Omitted image "ScriptingAssistanceMatchingSuggestionsMethods.png"\] Alt text: A line of code for a variable definition with a pop-up window displaying potential scripting elements.

</td></tr><tr><td>

Enter an open parenthesis character after a valid class, function, or method name.

</td><td>

Displays the expected parameters for the class or method.

 Enter the expected parameters as needed.

</td><td>

\[Omitted image "ScriptingAssistanceParameters.png"\] Alt text: A line of code for a variable defining a method call. There is a pop-up window displaying potential scripting elements.

</td></tr><tr><td>

Insert macro text

1.  In the **Script** field, type the macro keyword text.

To list the available macros, enter `help`.

2.  Press Tab.

</td><td>

Inserts macro text at the current position. For more information, see [JavaScript syntax editor macros](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/scripts/r_SyntaxEditorMacros.md).

</td><td>

\[Omitted image "ScriptingAssistanceMacroAdded.png"\] Alt text: The macro text for help added to the script.

</td></tr></tbody>
</table>## JavaScript editing tips

-   To fold a code block, select the minus sign beside the first line of the block. The minus sign only appears beside blocks that can be folded. To unfold the code block, select the plus sign.
-   To insert a fixed space anywhere in your code, press Tab.
-   To indent a single line of code, select in the leading white space of the line and then press Tab.
-   To indent one or more lines of code, select the code and then press Tab. To decrease the indentation, press Shift + Tab.
-   To remove one tab from the start of a line of code, select in the line and press Shift + Tab.

-   **[JavaScript syntax editor macros](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/scripts/r_SyntaxEditorMacros.md)**  
Script macros provide shortcuts for typing commonly used code. To insert macro text into a script field, enter the macro keyword followed by the Tab.
-   **[Context menu in the syntax editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/scripts/context-menu-syntax-editor.md)**  
View the context menu for script includes, Glide APIs, and tables in the JavaScript syntax editor.
-   **[Syntax errors and warnings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/scripts/c_ScriptSyntaxErrorChecking.md)**  
All script fields provide controls for checking the syntax for errors and for locating the error easily when one occurs.
-   **[JavaScript API context-sensitive help](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/scripts/c_ScriptingAssistance.md)**  
The syntax editor can display context-sensitive API information.

**Parent Topic:**[JavaScript syntax editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/scripts/c_SyntaxEditor.md)

