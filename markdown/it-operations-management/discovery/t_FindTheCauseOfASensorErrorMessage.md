---
title: Find the cause of a sensor error message
description: Use this procedure to identify a Discovery sensor error.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-06-05"
reading_time_minutes: 1
breadcrumb: [Discovery error messages, Discovery monitoring and issue resolution, Discovery, ITOM Visibility, IT Operations Management]
---

# Find the cause of a sensor error message

Use this procedure to identify a Discovery sensor error.

## Before you begin

Role required: sn\_cloud\_ops\_ws.cloud\_ops\_admin or admin

## About this task

This process requires that you identify the following:

-   The error.
-   The name of the sensor where the error occurred.
-   The datestamp of the error.
-   The associated stack trace of the error.

## Procedure

1.  Depending on the application you are using, do one of the following:

    -   To view the **Discovery Log** in Cloud Discovery Workspace, navigate to **Cloud Discovery Workspace** &gt; **Cloud Discovery** &gt; **Discovery Log**.
    -   To view the **Discovery Log** in Discovery, navigate to **All** &gt; **Discovery** &gt; **Discovery Log**.
2.  To find the error, filter on the **Level name** of **Error**.

    If you are using Discovery, you can also view the error and the date stamp in the Error Report. The report is available on the Discovery dashboard.

3.  Note the **Created** field of the error record.

    This timestamp is used to find the proper stack trace.

4.  Note the **Short Message** field of the error record.

    This field shows the name of the sensor where the error has occurred.

5.  To find the stack trace, navigate to **System Logs** &gt; **Errors**.

6.  Search for the date and time that matches the value in the **Created** field of the error record in the Discovery Log.

7.  The **Message** field of that entry contains the full stack trace of the error.

    The stack trace contains the error message, the sys\_id of the script, and the line number where the error has occurred.

8.  After determining the error details, you can fix the JavaScript file.


**Parent Topic:**[Discovery error messages](../concept/c_DiscoveryErrorMessages.md)

**Related topics**  


[Find the cause of a "No Sensor Defined" error message](t_IdentifyCauseNoSenDefEM.md)

[Fix the cause of a sensor error message](t_FixTheCauseOfASensorErrorMessage.md)

[Find the cause of a "Probe not found" error](t_FindTheCauseOfAProbeNotFoundError.md)

