---
title: Syntax editor macros
description: Script macros provide shortcuts for typing commonly used code. To insert macro text into a script field, enter the macro keyword followed by the Tab.
locale: en-US
release: xanadu
product: Scripts
classification: scripts
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Syntax editor plugin, JavaScript syntax editor, Scripting, Building pro-code applications, Developing your application, Building applications]
---

# Syntax editor macros

Script macros provide shortcuts for typing commonly used code. To insert macro text into a script field, enter the macro keyword followed by the Tab.

Syntax editor macros are defined in the Editor Macros \[syntax\_editor\_macro\] table. To create or modify a script macro, see [Create or modify a script macro](../task/t_ManageScriptMacros.md).

-   **vargr**
    -   Inserts a standard GlideRecord query for a single value.
    -   Output:

        ```
        var gr = new GlideRecord("$0");
        gr.addQuery("name", "value");
        gr.query();
        if (gr.next()) {
           
        }
        ```

-   **vargror**
    -   Inserts a GlideRecord query for two values with an `OR` condition.
    -   Output:

        ```
        var gr = new GlideRecord('$0');
         
        var qc = gr.addQuery('field', 'value1');
         
        qc.addOrCondition('field', 'value2');
        gr.query();
         
        while (gr.next()) {
        
         
        }
        ```

-   **for**
    -   Inserts a standard recursive loop with an array.
    -   Output:

        ```
        for (var i=0; i< myArray.length; i++) {
         //myArray[i];
        
        }
        ```

-   **info**
    -   Inserts a GlideSystem information message.
    -   Output:

        ```
        gs.addInfoMessage("");
        ```

-   **method**
    -   Inserts a blank JavaScript function template.
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

-   **doc**
    -   Inserts a comment block for describing a function or parameters.
    -   Output:

        ```
        /**
                        
         * Description: 
                        
         * Parameters: 
                        
         * Returns:
        */
        ```


**Parent Topic:**[Syntax editor plugin](../concept/c_SyntaxEditorPlugin.md)

