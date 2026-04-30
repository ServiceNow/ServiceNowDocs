---
title: Syntax editor JavaScript support
description: The syntax editor provides editing functions to support editing JavaScript scripts.
locale: en-US
release: yokohama
product: Scripts
classification: scripts
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Syntax editor plugin, JavaScript syntax editor, Scripting, Building pro-code applications, Developing your application, Building applications]
---

# Syntax editor JavaScript support

The syntax editor provides editing functions to support editing JavaScript scripts.

## JavaScript editing functions

<table id="simpletable_vx3_1sc_bq"><thead><tr><th>

Icon

</th><th>

Keyboard Shortcut

</th><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

![](../image/SyntaxEditorIcon.png)

</td><td>

N/A

</td><td>

Toggle Syntax Editor

</td><td>

Disables the syntax editor. Click the button again to enable the syntax editor.

</td></tr><tr><td>

![](../image/FormatCode.png)

</td><td>

Access Key + R

</td><td>

Format Code

</td><td>

Applies the proper indentation to the script.

</td></tr><tr><td>

![](../image/IconComment.png)

</td><td>

Access Key + C

</td><td>

Comment Selected Code

</td><td>

Comments out the selected code.

</td></tr><tr><td>

![](../image/JSunComment.png)

</td><td>

Access Key + U

</td><td>

Uncomment Selected Code

</td><td>

Removes comment codes from the selected code.

</td></tr><tr><td>

![](../image/JsValidate.png)

</td><td>

N/A

</td><td>

Check Syntax

</td><td>

Checks the code for syntax errors. By default, the system automatically checks for syntax errors as you type in a script field. If an error or warning is found, the syntax editor displays a bullet beside the script line containing the error or warning. This check occurs on all script fields.

</td></tr><tr><td>

![](../image/Find.png)

</td><td>

Access Key + \\

</td><td>

Start Searching

</td><td>

Highlights all occurrences of a search term in the script field and locates the first occurrence. Click the icon, then enter the search term and press **Enter**. You can use [regular expressions](http://www.regular-expressions.info/reference.html) enclosed in slashes to define the search term. For example, the term /a\{3\}/ locates aaa.

</td></tr><tr><td>

![](../image/FindNext.png)

</td><td>

Access Key + \[

</td><td>

Find Next

</td><td>

Locates the next occurrence of the current search term in the script field. Use Start Searching to change the current search term.

</td></tr><tr><td>

![](../image/FindPrevious.png)

</td><td>

Access Key + \]

</td><td>

Find Previous

</td><td>

Locates the previous occurrence of the current search term in the script field. Use Start Searching to change the current search term.

</td></tr><tr><td>

![](../image/Replace.png)

</td><td>

Access Key + W

</td><td>

Replace

</td><td>

Replaces the next occurrence of a text string in the script field.1.  Click the icon, then enter the string to replace and press **Enter**. You can use regular expressions enclosed in slashes to define the string to replace. For example, the term /a\{3\}/ locates aaa.
2.  Enter the replacement string and press **Enter**.

</td></tr><tr><td>

![](../image/ReplaceAll.png)

</td><td>

Access Key + ;

</td><td>

Replace All

</td><td>

Replaces all occurrences of a text string in the script field.1.  Click the icon, then enter the string to replace and press **Enter**. You can use regular expressions enclosed in slashes to define the string to replace. For example, the term /a\{3\}/ locates aaa.
2.  Enter the replacement string and press **Enter**.

</td></tr><tr><td>

![](../image/JsSave.png)

</td><td>

N/A

</td><td>

Save

</td><td>

Saves changes without leaving the current view. Use this button in full screen mode to save without returning to standard form view.

</td></tr><tr><td>

![](../image/FullScreen.png)

</td><td>

Access Key + L

</td><td>

Toggle Full Screen Mode

</td><td>

Expands the script field to use the full form view for easier editing. Click the button again to return to standard form view. This feature is not available for Internet Explorer.

</td></tr><tr><td>

![](../image/Help.png)

</td><td>

Access Key + P

</td><td>

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

**Parent Topic:**[Syntax editor plugin](../concept/c_SyntaxEditorPlugin.md)

