---
title: Log action
description: Logs a message in the Workflow Studio log table sys\_flow\_log.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-02-06"
reading_time_minutes: 1
breadcrumb: [Workflow Studio actions, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Log action

Logs a message in the Workflow Studio log table sys\_flow\_log.

## Roles and availability

Available as a Workflow Studio ServiceNow core action. Users with the flow\_designer or admin role can add an action to a flow and define configuration details.

You can view the logs in the flow execution details. To learn more, see [Flow execution details](../concept/flow-execution-details.md) and [Workflow Studio data](../concept/data-population.md).

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

Message to display in the Flow log \[sys\_flow\_log\] table. Enter text or drag data pills into the field. **Note:** The Workflow Studio design environment only supports entering 255 characters of text for a log message. The length limitation only applies to text entered directly into the input. Data pill values can exceed 255 characters in length. You can log values greater than 255 characters long by using either a data pill value or calling the [GlideSystem - log\(String message, String source\)](https://www.servicenow.com/docs/access?context=c_GlideSystemAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US) method from a script.

</td></tr></tbody>
</table>## General guidelines

-   **Test your flow to ensure it generates useful logging information**

    Test your flow and review its execution details. Make sure that the log action stores useful data.

-   **Use data pills to log dynamic data**

    Add one or more data pills to your Log action to store dynamically generated values. Make sure that the data pills come from actions and flow logic that have run before the Log action.


**Parent Topic:**[Workflow Studio actions](../concept/flow-actions.md)

