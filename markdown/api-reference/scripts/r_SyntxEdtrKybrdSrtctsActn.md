---
title: Syntax editor keyboard shortcuts and actions
description: The syntax editor offers keyboard shortcuts and actions to assist in writing code.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/scripts/r\_SyntxEdtrKybrdSrtctsActn.html
release: zurich
product: Scripts
classification: scripts
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Using the JavaScript syntax editor, JavaScript syntax editor, Scripting, API implementation, API implementation and reference]
---

# Syntax editor keyboard shortcuts and actions

The syntax editor offers keyboard shortcuts and actions to assist in writing code.

<table id="table_wmy_bpl_ss"><thead><tr><th>

Keyboard shortcut or action

</th><th>

Description

</th><th>

Example

</th></tr></thead><tbody><tr><td class="sub-head" colspan="3">

Write code

</td></tr><tr><td>

Scripting assistance

 Control+Spacebar

</td><td>

Displays a list of valid elements at the insertion point such as:

-   Class names
-   Function names
-   Object names
-   Variable names

 Double-click an entry to add it to the script.

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

Toggle full screen mode

 Control+M

</td><td>

Switches between displaying the form with the full screen and displaying it normally.

</td><td>

 

</td></tr><tr><td>

Format code

-   Windows: Control+Shift+B
-   Mac: Command+Shift+B

</td><td>

Formats the selected lines to improve readability.

</td><td>

\[Omitted image "ScriptingAssistanceUnformattedCode.png"\] Alt text: Several lines of unformatted code\[Omitted image "ScriptingAssistanceFormattedCode.png"\] Alt text: Several lines of code formatted for readability

</td></tr><tr><td>

Toggle comment

-   Windows: Control+/
-   Mac: Command+/

</td><td>

Adds or removes the comment characters `//` from the selected lines.

</td><td>

\[Omitted image "ScriptingAssistanceUncommentedCode.png"\] Alt text: A line of code selected with no comment characters\[Omitted image "ScriptingAssistanceCommentedCode.png"\] Alt text: A line of code selected with comment characters added to the front of the line.

</td></tr><tr><td>

Insert macro text

1.  In the **Script** field, type the macro keyword text. For example `help`.
2.  Press Tab.

</td><td>

Inserts macro text at the current position.

</td><td>

\[Omitted image "ScriptingAssistanceMacroTyped.png"\] Alt text: A line of code containing the string help.\[Omitted image "ScriptingAssistanceMacroAdded.png"\] Alt text: The macro text for help added to the script.

</td></tr><tr><td class="sub-head" colspan="3">

Search

</td></tr><tr><td>

Start search

-   Windows: Control+F
-   Mac: Command+F

</td><td>

Highlights all occurrences of a search term in the script field and locates the first occurrence.

 You can create [regular expressions](http://www.regular-expressions.info/reference.html) by enclosing the search terms between slash characters . For example, the search term `/a{3}/` locates the string `aaa` .

</td><td>

\[Omitted image "ScriptingAssistanceSearchTerm.png"\] Alt text: A search field with the term gr.\[Omitted image "ScriptingAssistanceSearchResults.png"\] Alt text: The search results of the search term gr displaying four highlighted items. The first search result is selected.

</td></tr><tr><td>

Find next

-   Windows: Control+G
-   Mac: Command+G

</td><td>

Locates the next occurrence of the current search term in the script field. Use **Start Searching** to change the current search term.

</td><td>

\[Omitted image "ScriptingAssistanceFindNext.png"\] Alt text: The search results of the search term gr displaying four highlighted items. The second search result is selected.

</td></tr><tr><td>

Find previous-   Windows: Control+Shift+G
-   Mac: Command+Shift+G

</td><td>

Locates the previous occurrence of the current search term in the script field. Use **Start Searching** to change the current search term.

</td><td>

\[Omitted image "ScriptingAssistanceSearchResults.png"\] Alt text: The search results of the search term gr displaying four highlighted items. The first search result is selected.

</td></tr><tr><td>

Replace

-   Windows: Control+E
-   Mac: Command+E

</td><td>

Replaces the next occurrence of a text string in the script field.

</td><td>

\[Omitted image "ScriptingAssistanceReplaceSearchTerm.png"\] Alt text: A replace field with the string gr.\[Omitted image "ScriptingAssistanceReplaceWith.png"\] Alt text: A replace with field with the string gl.\[Omitted image "ScriptingAssistanceReplaceConfirm.png"\] Alt text: A replace confirmation dialog with options for Yes, No, and Stop

</td></tr><tr><td>

Replace all

-   Windows: Control+;
-   Mac: Command+;

</td><td>

Replaces all occurrences of a text string in the script field.

</td><td>

\[Omitted image "ScriptingAssistanceReplaceAllSearchTerm.png"\] Alt text: A replace field with the search term gr.\[Omitted image "ScriptingAssistanceReplaceAllWith.png"\] Alt text: A replace with field with the string gl.

</td></tr><tr><td class="sub-head" colspan="3">

Help

</td></tr><tr><td>

Help

-   Windows: Control+H
-   Mac: Command+H

</td><td>

Displays the list of syntax editor keyboard shortcuts.

</td><td>

\[Omitted image "SyntaxEditorHelp.png"\] Alt text: A pop-up window displaying the keyboard shortcuts for the Syntax Editor.

</td></tr><tr><td>

Show description

-   Windows: Control+J
-   Mac: Command+J

</td><td>

Displays API documentation for the scripting element at the cursor's current location.

</td><td>

\[Omitted image "ScriptingAssistanceAPIdoc.png"\] Alt text: A line of code selected with a pop-up window displaying API help for the GlideRecord object

</td></tr><tr><td>

Show macros

1.  In the **Script** field, type `help`.
2.  Press Tab.

</td><td>

Displays the list of available syntax editor macros as text within the script field.

</td><td>

\[Omitted image "ScriptingAssistanceMacroTyped.png"\] Alt text: A line of code containing the string help.\[Omitted image "ScriptingAssistanceMacroAdded.png"\] Alt text: The macro text for help added to the script.

</td></tr></tbody>
</table>**Parent Topic:**[Using the JavaScript syntax editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/scripts/r_EdtJvaScptWSyntxEdtr.md)

