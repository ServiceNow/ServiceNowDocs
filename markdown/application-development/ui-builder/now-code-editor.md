---
title: Edit code with the Now Code Editor \(advanced feature\)
description: Now Code Editor is a rich-text editor like interface that supports Cascading Style Sheets \(CSS\), Hypertext Markup Language \(HTML\), JavaScript, Extensible Markup Language \(XML\), and JavaScript Object Notation \(JSON\). Use Now Code Editor to modify UI configuration, data resource configuration, styles, events, client-side and server-side scripts in Next Experience UI Builder components.
locale: en-US
release: australia
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Advanced UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Edit code with the Now Code Editor \(advanced feature\)

Now Code Editor is a rich-text editor like interface that supports Cascading Style Sheets \(CSS\), Hypertext Markup Language \(HTML\), JavaScript, Extensible Markup Language \(XML\), and JavaScript Object Notation \(JSON\). Use Now Code Editor to modify UI configuration, data resource configuration, styles, events, client-side and server-side scripts in Next Experience UI Builder components.

Now Code Editor supports the following features:

-   Basic editing
-   Debugging
-   Command palette
-   Code formatting
-   Syntax checking and highlighting
-   Auto-suggestions
-   Script macros for common code

## Basic editing

<table id="table_unk_l3p_24b"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Format code ![](../image/nce_format_code.png)

</td><td>

Applies proper indentation to the script.Keyboard shortcut:

-   Windows: Shift+Alt+F
-   Mac: Shift+Option+F

</td></tr><tr><td>

Highlight syntax

</td><td>

Highlights the syntax of the code.

</td></tr><tr><td>

Check syntax ![syntax check icon](../image/nce_syntax_check.png)

</td><td>

Checks for formatting errors and highlights syntax errors.-   Windows: Shift+Alt+C
-   Mac: Shit+Option+C

</td></tr><tr><td>

Show suggestions

</td><td>

Displays a list of valid elements at the insertion point such as:-   Class names
-   Function names
-   Object names
-   Variable names

Select and click an entry to add it to the script.Keyboard shortcut:

-   Windows: Control+Space
-   Mac: Control+Space

You can also enable or turn off **Syntax highlighting** from the **Settings** menu.

</td></tr><tr><td>

Toggle comments ![toggle comments icon](../image/nce_toggle_comments.png)

</td><td>

Comments one or more lines of code with two consecutive forward-slashes //.Keyboard shortcut:

-   Windows: Control+/
-   Mac: Command+/

</td></tr><tr><td>

Show minimap

</td><td>

Displays the minimap of the code snippet. You can display or hide the minimap option, from the **Settings** menu.

</td></tr><tr><td>

Enable word wrap

</td><td>

Enables word wrap function in the editor area.You can toggle the **Enable word wrap** option from the **Settings** menu.

</td></tr><tr><td>

Show command palette

</td><td>

Displays a list of available commands for the common operations. You can execute editor commands, find and replace text, fold and unfold code blocks, toggle comments and many more tasks using the same interactive window. Keyboard shortcut

-   Windows: F1
-   Mac: F1

</td></tr><tr><td>

Expand editor ![expand editor icon](../image/nce_exp_editor.png) or collapse editor ![collapse editor icon](../image/nce_coll_editor.png)

</td><td>

Expands or collapses the editor.Keyboard shortcut

-   Windows: Control+M
-   Mac: Control+M

</td></tr></tbody>
</table>## Debugging

To launch Script Debugger, click the Script Debugger icon ![Script Debugger icon](../image/nce_script_debugger.png) in the toolbar.

**Note:** You can add a breakpoint, conditional breakpoint, or logpoint, only when debugging is enabled and selected language is JavaScript.

<table id="table_ysr_rzp_24b"><thead><tr><th>

Task

</th><th>

Do this

</th></tr></thead><tbody><tr><td>

Add breakpoint

</td><td>

Right-click beside a line number in the ruler area and select **Add breakpoint**.

</td></tr><tr><td>

Add conditional breakpoint

</td><td>

1.  Right-click beside a line number in the ruler area and select **Add conditional breakpoint**.
2.  Enter a break condition in the editor.

</td></tr><tr><td>

Add logpoint

</td><td>

Right-click beside a line number in the ruler area and select **Add logpoint**.

</td></tr><tr><td>

Compare text in Diff mode

</td><td>

Use the side-by-side view icon ![now code editor side by side view](../image/nce_side_by_side_view.png) and inline view icon ![Now code editor inline view](../image/nce_inline_view.png) to toggle between views.

</td></tr></tbody>
</table>## Code editor macros

-   **for**
    -   Description: Inserts a standard for loop with an example array.
    -   Output:

        ```
        for (var i=0; i< myArray.length; i++) {
         //myArray[i];
         
        }
        ```

-   **method**
    -   Description: Inserts an empty JavaScript function template.
    -   Output:

        ```
        /*_________________________________________________________________
           * Description:
           * Parameters:
           * Returns:
           ________________________________________________________________*/
           : function() {
           
           },
        ```

-   **info**
    -   Description: Inserts a GlideSystem information message.
    -   Output:

        ```
        gs.addInfoMessage(gs.getMessage(""));
        ```

-   **doc**
    -   Description: Inserts a comment block for describing a function or parameters.
    -   Output:

        ```
        /**
         
        * Description: 
         
        * Parameters: 
         
        * Returns:
        */
        ```

-   **vargror**
    -   Description: Inserts a GlideRecord query for two values with an OR condition.
    -   Output:

        ```
        var gr = new GlideRecord('');
         
        var qc = gr.addQuery('field', 'value1');
         
        qc.addOrCondition('field', 'value2');
        gr.query();
         
        while (gr.next()) {
        
         
        }
        
        ```

-   **vargr**
    -   Description: Inserts a standard GlideRecord query for a single value.
    -   Output:

        ```
        var gr = new GlideRecord("");
        gr.addQuery("name", "value");
        gr.query();
        if (gr.next()) {
           
        }
        
        ```


**Parent Topic:**[Advanced UI Builder](../../ui-builder/concept/advanced-uib.md)

