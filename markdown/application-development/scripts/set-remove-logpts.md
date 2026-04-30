---
title: Set or remove logpoints
description: Set breakpoints or conditional logpoints to log messages to the console at specific lines, and remove logpoints when you are done debugging them.
locale: en-US
release: xanadu
product: Scripts
classification: scripts
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Script Debugger and Session Log, Debugging scripts, Scripting, Building pro-code applications, Developing your application, Building applications]
---

# Set or remove logpoints

Set breakpoints or conditional logpoints to log messages to the console at specific lines, and remove logpoints when you are done debugging them.

## Before you begin

-   Set the **glide.debug.log\_point** system property to `true`. See [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) for more information.
-   Role required: admin or script\_debugger

## About this task

Logpoints belong to the developer who sets them. Developers must set and remove their own logpoints.

**Note:** At a specific line, you can set either a logpoint or breakpoint but not both.

## Procedure

1.  Navigate to the server script to debug.

    For example, navigate to **All** &gt; **System Definition** &gt; **Business Rules**.

2.  From the Syntax Editor, click the gutter next to a script line.

    |Action|Description|
    |------|-----------|
    |**Set a logpoint**|Right-click a blank line and click **Add logpoint** to set a logpoint.|
    |**Remove a logpoint**|Right-click a logpoint and select **Remove logpoint** to remove it.|
    |**Edit a logpoint**|Right-click a logpoint and select **Edit logpoint** to edit it.|

    **Note:** The script entered for the logpoint must have the same format as that of the script in GSLog and GSInfo script includes.

3.  From the Syntax Editor toolbar, click the **Open Script Debugger** icon ![Script debugger icon](../image/script-debugger.png).

4.  On the Script Debugger window, trigger the script.

    For example, create a record to trigger an insert business rule script.

    **Note:** You can also add logpoints in the Script Debugger window.

5.  In the Script Debugger window, click **Session Log** to view the logpoints.

6.  When debugging is complete, remove logpoints from the script.


**Parent Topic:**[Script Debugger and Session Log](../concept/script-debugger.md)

