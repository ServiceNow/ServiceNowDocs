---
title: Fix the cause of a sensor error message
description: To fix a Discovery sensor error message, you must fix the JavaScript file containing the code that generated the error.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-26"
reading_time_minutes: 1
breadcrumb: [Discovery error messages, Discovery monitoring and issue resolution, Discovery, ITOM Visibility, IT Operations Management]
---

# Fix the cause of a sensor error message

To fix a Discovery sensor error message, you must fix the JavaScript file containing the code that generated the error.

## Before you begin

Verify the following:

-   You have access to the Discovery Definition modules.
-   You have completed the steps in [Find the cause of a sensor error message](t_FindTheCauseOfASensorErrorMessage.md).

Role required: admin

## About this task

Use the sensor name and stack trace you identified in [Find the cause of a sensor error message](t_FindTheCauseOfASensorErrorMessage.md) to locate the failing code. The stack trace provides the line number and function name where the error occurred.

**Note:** The exact fix depends on the specific sensor and payload. This topic describes where and how to fix the error, not specific code changes. Contact ServiceNow Support for complex cases.

## Procedure

1.  Navigate to the Discovery Definition module where the error occurred.

    For example, navigate to **Discovery Definition** &gt; **Script Includes**.

2.  Search for the sensor name in the **Name** field.

3.  Select the link to open the record.

4.  Locate the failing function or line using the stack trace, then correct the JavaScript.

    For example, if the error indicates it "Cannot read property X of undefined", add a defensive check around the payload fields.

5.  Select **Update**.


## What to do next

Rerun Discovery to verify the sensor no longer generates the error. If the error persists after applying the fix, contact ServiceNow Support and provide the full stack trace, the sensor name, and a description of the changes you made.

**Parent Topic:**[Discovery error messages](../concept/c_DiscoveryErrorMessages.md)

**Related topics**  


[Find the cause of a sensor error message](t_FindTheCauseOfASensorErrorMessage.md)

[Find the cause of a "No Sensor Defined" error message](t_IdentifyCauseNoSenDefEM.md)

[Find the cause of a "Probe not found" error](t_FindTheCauseOfAProbeNotFoundError.md)

