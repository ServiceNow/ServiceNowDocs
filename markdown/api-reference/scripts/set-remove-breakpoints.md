---
title: Set or remove breakpoints
description: Set breakpoints or conditional breakpoints to pause scripts at specific lines, and remove breakpoints when you're done debugging them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/scripts/set-remove-breakpoints.html
release: brazil
product: Scripts
classification: scripts
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Use Script Debugger, Debug scripts, Scripting, API implementation, API implementation and reference]
---

# Set or remove breakpoints

Set breakpoints or conditional breakpoints to pause scripts at specific lines, and remove breakpoints when you're done debugging them.

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

2.  From the Syntax Editor, select the gutter next to a script line.

    |Action|Description|
    |------|-----------|
    |**Set a breakpoint**|Select a blank line to set a breakpoint.|
    |**Set a conditional breakpoint**|Right-click a blank line and select **Add conditional breakpoint** to set a conditional breakpoint.|
    |**Remove a breakpoint**|Select a breakpoint to remove it.|
    |**Remove a conditional breakpoint**|Right-click a conditional breakpoint and select **Remove breakpoint** to remove it.|

3.  From the Syntax Editor toolbar, select the **Open Script Debugger** icon \[Omitted image "script-debugger.png"\] Alt text:.

4.  From the Script Debugger window, trigger the script.

    For example, create a record to trigger an insert business rule script.

    The Script Debugger pauses the script on the first line containing a breakpoint.

5.  From the confirmation window, select **Start Debugging**.

    The system switches focus to the Script Debugger window and displays the target script paused at the first breakpoint.

6.  When debugging is complete, remove breakpoints from the script.


**Parent Topic:**[Script Debugger and Session Log](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/script-debugger.md)

**Related topics**  


[Script Debugger step-through and console controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/step-through-controls.md)

