---
title: Set or remove breakpoints
description: Set breakpoints or conditional breakpoints to pause scripts at specific lines, and remove breakpoints when you are done debugging them.
locale: en-US
release: xanadu
product: Scripts
classification: scripts
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Script Debugger and Session Log, Debugging scripts, Scripting, Building pro-code applications, Developing your application, Building applications]
---

# Set or remove breakpoints

Set breakpoints or conditional breakpoints to pause scripts at specific lines, and remove breakpoints when you are done debugging them.

## Before you begin

Role required:

-   admin
-   script\_debugger

## About this task

Breakpoints belong to the developer who sets them. Developers must set and remove their own breakpoints.

**Note:** At a specific line, you can set either a logpoint or breakpoint but not both.

## Procedure

1.  Navigate to the server script to debug.

    For example, navigate to **All** &gt; **System Definition** &gt; **Business Rules**.

2.  From the Syntax Editor, click the gutter next to a script line.

    |Action|Description|
    |------|-----------|
    |**Set a breakpoint**|Click a blank line to set a breakpoint.|
    |**Set a conditional breakpoint**|Right-click a blank line and click **Add conditional breakpoint** to set a conditional breakpoint.|
    |**Remove a breakpoint**|Click a breakpoint to remove it.|
    |**Remove a conditional breakpoint**|Right-click a conditional breakpoint and select **Remove breakpoint** to remove it.|

3.  From the Syntax Editor toolbar, click the **Open Script Debugger** icon.

    The system opens a Script Debugger window.

4.  Trigger the script.

    For example, create a record to trigger an insert business rule script.

    The Script Debugger pauses the script on the first line containing a breakpoint, and the system displays a confirmation window.

    ![ServiceNow script debugger](../image/start-debugging-confirmation.png)

5.  Click **Start Debugging**.

    The system switches focus to the Script Debugger window and displays the target script paused at the first breakpoint. Console pane is enabled.

6.  When debugging is complete, remove breakpoints from the script.


**Parent Topic:**[Script Debugger and Session Log](../concept/script-debugger.md)

**Related topics**  


[Script Debugger step-through and console controls](../reference/step-through-controls.md)

