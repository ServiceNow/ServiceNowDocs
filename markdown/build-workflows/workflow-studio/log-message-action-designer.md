---
title: Log step
description: Logs a message in the Workflow Studio log table sys\_flow\_log.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Steps, Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Log step

Logs a message in the Workflow Studio log table sys\_flow\_log.

## Roles and availability

Available as an Workflow Studio action step. Users with the action\_designer role can create a custom action with one or more action steps.

## Fields

<table id="table_fzt_n55_3cb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Log level

</td><td>

Level of importance of the log message.-   Error
-   Warn
-   Info

</td></tr><tr><td>

Log message

</td><td>

Message to display in the Flow log \[sys\_flow\_log\] table. Enter text or drag data pills into the field. **Note:** The Workflow Studio design environment only supports entering 255 characters of text for a log message. The length limitation only applies to text entered directly into the input. Data pill values can exceed 255 characters in length. You can log values greater than 255 characters long by using either a data pill value or calling the GlideSystem - log\(String message, String source\) method from a script.

</td></tr></tbody>
</table>## Action error evaluation

-   **If this step fails**

    Data type: **Choice**

    Option to continue running the next step or go to error evaluation. To use the step status code or message for a custom action error condition, see [Action error evaluation](../concept/action-error-evaluation.md).


**Parent Topic:**[Workflow Studio steps](../concept/steps.md)

