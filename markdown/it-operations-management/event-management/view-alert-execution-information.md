---
title: View alert execution information
description: You can click any link in the Alert Executions list to view the alert execution information of the referenced item. This information appears in the Alert Management Rule record only after an alert matched the filter in the rule and an action was performed.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Alert executions information, Alert management rules for resolving alerts, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# View alert execution information

You can click any link in the Alert Executions list to view the alert execution information of the referenced item. This information appears in the Alert Management Rule record only after an alert matched the filter in the rule and an action was performed.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

Among the information shown in the Alert Executions list is:

-   The list of alerts that matched the filter of the rule.
-   The tasks, including incidents, that were opened.
-   Which remediation workflows ran and which subflows ran.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Rules** &gt; **Alert Management Rules**.

2.  In the Alert Management Rules list, click the rule.

    If an alert matched the filter in the rule and an action was performed, the Alert Executions list appears in the Alert Management Rules record. The list appears irrespective of the stage of the selected alert management rule.

<table id="table_zlc_ghk_d2b"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Alert

</td><td>

Alert number of the alerts that matched the alert management rule.

</td></tr><tr><td>

Action name

</td><td>

Name of the action that was taken to resolve the alert \(subflow or workflow\).

</td></tr><tr><td>

Link to execution

</td><td>

Link to the action execution log that was created when the action was performed.

</td></tr><tr><td>

Related task

</td><td>

Link to the task that was created when the alert was resolved. For example, if the action for a rule is to create an incident, this field provides the incident number with a link to open the incident.A link is provided to the workflow remediation task that is created to monitor the remediation.

</td></tr><tr><td>

Log

</td><td>

Notice or information showing the result of the execution action, for example, how executions took place, "`1 out of 2 executions`". When the alert closes, the execution count number \(the first number\) resets to 0.This information does not indicate that the subflow was executed successfully, rather that the call to that subflow was successful and that the subflow is correctly configured.

</td></tr><tr><td>

Automatic run

</td><td>

Indication of how the action ran: automatically \(true\) or manually \(false\).

</td></tr><tr><td>

Created

</td><td>

Date and time that the entry was created.

</td></tr></tbody>
</table>
**Parent Topic:**[Alert executions information](../concept/alert-rule-execution.md)

