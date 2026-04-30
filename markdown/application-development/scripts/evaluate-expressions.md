---
title: Evaluate expressions in runtime using Console
description: Define, declare, and verify new variables and functions while you debug a script in runtime using Console. The script execution must be paused to use Console.
locale: en-US
release: yokohama
product: Scripts
classification: scripts
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Script Debugger and Session Log, Debugging scripts, Scripting, Building pro-code applications, Developing your application, Building applications]
---

# Evaluate expressions in runtime using Console

Define, declare, and verify new variables and functions while you debug a script in runtime using Console. The script execution must be paused to use Console.

## Before you begin

-   Review [Limitations with using Console](https://www.servicenow.com/docs/access?context=console-limitatations-sd&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)
-   Role required: script\_debugger, admin

## Procedure

1.  Launch the Script Debugger in one of the following ways.

    |Application|Navigation path|
    |-----------|---------------|
    |**Application navigator**|Navigate to **All** &gt; **System Diagnostics** &gt; **Script Debugger**.|
    |**Studio**|Navigate to **File** &gt; **Launch Script Debugger**.|
    |**Syntax Editor**|Click the Script Debugger icon ![script debugger icon](../image/script-debugger.png).|

    The Script Debugger modal is displayed.

2.  Trigger the script.

    For example, create a record to trigger an insert business rule script. The Script Debugger pauses the script on the first line that contains a breakpoint, and then you see the ServiceNow Script Debugger confirmation window.

    ![ServiceNow Script Debugger confirmation window.](../image/start-debugging-confirmation.png)

3.  Click **Start Debugging**.

    The focus shifts to the Script Debugger window and you see the target script that paused at the first breakpoint.

    **Note:** Make sure that the status of Script Debugger is EXECUTION\_PAUSED. You can use Console only when the script execution is paused during debugging.

4.  Click the expand console \(![Expand Console icon.](../image/console_expand.png)\) to expand the Console pane.

    To start evaluating expressions, enter one or more expressions in the Console and press Enter. For example, enter `var x = 10;` and press Enter. To enter multiple lines of expressions, press Shift + Enter after each line and press Enter after the last expression. To clear all the expressions in the Console, click the clear console icon \(![Clear console icon](../image/console_clear.png)\). For more information on Console controls, see [Script Debugger step-through and console controls](https://www.servicenow.com/docs/access?context=step-through-controls&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

    ![Evaluating expressions in Console when a business rule execution is paused in the Script Debugger.](../image/console-script-debugger.png)

    After a statement is executed, it is stored in the browser cache. You can use the up arrow key to get the previous statement and the down arrow key to get the next statement from the browser cache. You can configure the number of cached statements for a session from user preferences. For more information about user preferences settings, see [Script Debugger and Session Log](https://www.servicenow.com/docs/access?context=script-debugger&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).


## Result

After a statement is executed, it is stored in the browser cache. You can use the up arrow key to get the previous statement and down arrow key to get the next statement from the browser cache. You can configure the number of cached statements for a session from user preferences. For more information about user preferences settings, see [Script Debugger and Session Log](https://www.servicenow.com/docs/access?context=script-debugger&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

-   **[Limitations with using Console](../reference/console-limitatations-sd.md)**  
You need to be aware of a few limitations when you use Console to evaluate expressions while debugging a script in runtime.

**Parent Topic:**[Script Debugger and Session Log](../concept/script-debugger.md)

**Related topics**  


[Limitations with using Console](https://www.servicenow.com/docs/access?context=console-limitatations-sd&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

