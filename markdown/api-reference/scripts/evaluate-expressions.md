---
title: Evaluate expressions in runtime using Console
description: Define, declare, and verify new variables and functions while you debug a script in runtime using Console. The script execution must be paused to use Console.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/scripts/evaluate-expressions.html
release: zurich
product: Scripts
classification: scripts
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Script Debugger, Debugging scripts, Scripting, API implementation, API implementation and reference]
---

# Evaluate expressions in runtime using Console

Define, declare, and verify new variables and functions while you debug a script in runtime using Console. The script execution must be paused to use Console.

## Before you begin

Role required: script\_debugger or admin

## About this task

You need to be aware of a few limitations when you use Console to evaluate expressions while debugging a script in runtime.

-   The properties and values of an object don't display in Console. When you try to display an object to Console, only the string value of the object appears.
-   Console doesn't support GlideSystem printing methods, such as info\(\) and print\(\).
-   You can't use the this keyword in Console.
-   A script debugger timeout occurs when you evaluate expressions in Console.
-   While executing long scripts, if you see the response `Awaiting response from server`, you can't resume debugging or stop debugging using the resume or stop controls.

## Procedure

1.  Launch the Script Debugger in one of the following ways.

    |Application|Navigation path|
    |-----------|---------------|
    |**Application navigator**|Navigate to **All** &gt; **System Diagnostics** &gt; **Script Debugger**.|
    |**Studio**|Navigate to **File** &gt; **Launch Script Debugger**.|
    |**Syntax Editor**|Click the Script Debugger icon \[Omitted image "script-debugger.png"\] Alt text: script debugger icon.|

    The Script Debugger modal is displayed.

2.  Trigger the script.

    For example, create a record to trigger an insert business rule script. The Script Debugger pauses the script on the first line that contains a breakpoint, and then you see the ServiceNow Script Debugger confirmation window.

    \[Omitted image "start-debugging-confirmation.png"\] Alt text: ServiceNow Script Debugger confirmation window.

3.  Click **Start Debugging**.

    The focus shifts to the Script Debugger window and you see the target script that paused at the first breakpoint.

    **Note:** Make sure that the status of Script Debugger is EXECUTION\_PAUSED. You can use Console only when the script execution is paused during debugging.

4.  Click the expand console \(\[Omitted image "console\_expand.png"\] Alt text: Expand Console icon.\) to expand the Console pane.

    To start evaluating expressions, enter one or more expressions in the Console and press Enter. For example, enter `var x = 10;` and press Enter. To enter multiple lines of expressions, press Shift + Enter after each line and press Enter after the last expression. To clear all the expressions in the Console, click the clear console icon \(\[Omitted image "console\_clear.png"\] Alt text: Clear console icon\). For more information on Console controls, see [Script Debugger step-through and console controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/scripts/step-through-controls.md).

    \[Omitted image "console-script-debugger.png"\] Alt text: Evaluating expressions in Console when a business rule execution is paused in the Script Debugger.

    After a statement is executed, it is stored in the browser cache. You can use the up arrow key to get the previous statement and the down arrow key to get the next statement from the browser cache. You can configure the number of cached statements for a session from user preferences. For more information about user preferences settings, see [Script Debugger and Session Log](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/scripts/script-debugger.md).


## Result

After a statement is executed, it is stored in the browser cache. You can use the up arrow key to get the previous statement and down arrow key to get the next statement from the browser cache. You can configure the number of cached statements for a session from user preferences. For more information about user preferences settings, see [Script Debugger and Session Log](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/scripts/script-debugger.md).

**Parent Topic:**[Script Debugger and Session Log](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/scripts/script-debugger.md)

