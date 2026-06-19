---
title: Edit code with the Now Code Editor \(advanced feature\)
description: Now Code Editor is a rich-text editor like interface that supports Cascading Style Sheets \(CSS\), Hypertext Markup Language \(HTML\), JavaScript, Extensible Markup Language \(XML\), and JavaScript Object Notation \(JSON\). Use Now Code Editor to modify UI configuration, data resource configuration, styles, events, client-side and server-side scripts in Next Experience UI Builder components.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/now-code-editor.html
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

Format code \[Omitted image "nce\_format\_code.png"\] Alt text:

</td><td>

Applies proper indentation to the script.Keyboard shortcut:

-   Windows: Shift+Alt+F
-   Mac: Shift+Option+F

</td></tr><tr><td>

Highlight syntax

</td><td>

Highlights the syntax of the code.

</td></tr><tr><td>

Check syntax \[Omitted image "nce\_syntax\_check.png"\] Alt text: syntax check icon

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

Toggle comments \[Omitted image "nce\_toggle\_comments.png"\] Alt text: toggle comments icon

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

Expand editor \[Omitted image "nce\_exp\_editor.png"\] Alt text: expand editor icon or collapse editor \[Omitted image "nce\_coll\_editor.png"\] Alt text: collapse editor icon

</td><td>

Expands or collapses the editor.Keyboard shortcut

-   Windows: Control+M
-   Mac: Control+M

</td></tr></tbody>
</table>## Debugging

To launch Script Debugger, click the Script Debugger icon \[Omitted image "nce\_script\_debugger.png"\] Alt text: Script Debugger icon in the toolbar.

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

Use the side-by-side view icon \[Omitted image "nce\_side\_by\_side\_view.png"\] Alt text: now code editor side by side view and inline view icon \[Omitted image "nce\_inline\_view.png"\] Alt text: Now code editor inline view to toggle between views.

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


**Parent Topic:**[Advanced UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/advanced-uib.md)

