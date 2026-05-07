---
title: Fulfill a telesales sequence
description: Connect with leads or customers using the click-to-call outbound calling capability in telesales flows.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Customer Engagement Sequences, Lead and opportunity apps, Use, Sales Customer Relationship Management]
---

# Fulfill a telesales sequence

Connect with leads or customers using the click-to-call outbound calling capability in telesales flows.

## Before you begin

Role required: Sequence executor \[sn\_crm\_sequence.executor\]

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the List icon ![](../../../reuse/icons/product-icons/list-outline-24.svg).

3.  Navigate to **Sequences** &gt; **My Sequence Tasks**.

4.  Select a sequence task record.

5.  In the record, select the **Sequence Steps** tab.

6.  Review detailed call task information by selecting **Call task details**.

7.  Select the Call icon ![](../../../reuse/icons/product-icons/phone-fill-24.svg) next to the **Callback number** field to start an outbound call.

    **Note:** The Call icon ![](../../../reuse/icons/product-icons/phone-fill-24.svg) does not appear on the **Callback number** field in Xanadu or in Yokohama if you created the schedule call activity using the Schedule call - Deprecated activity. For compatibility information, see [Compatibility information for Customer Engagement Sequences](../reference/compatibility-matrix-upgrade-info.md).

8.  Complete the activity by setting the following fields.

<table id="table_okf_ycp_ghc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Reason

</td><td>

Call outcome. The available options are:-   Resolved: The call task was successfully completed and the goal met.
-   Timeout: The task expired because it was not accepted or acted upon in the allowed time.
-   Max attempts exceeded: Multiple attempts to connect or complete the task failed, reaching the configured limit.
-   No show: The customer did not join the scheduled call.
-   Cancelled by agent: The assigned agent manually cancelled the task before completion.
-   Technical issue: Call task could not proceed due to a system or connectivity problem.
-   Other: The task ended for a reason not covered by the predefined categories.


</td></tr><tr><td>

State

</td><td>

Status of the call task. The available options are: -   Open: The task has been created but work has not yet started.
-   Work in Progress: The task is actively being worked on.
-   Closed Complete: The task has finished successfully and all required actions are done.
-   Closed Abandoned: The task was closed without completion, usually due to irrelevance or inability to proceed.
-   Cancelled: The task terminated before completion.


</td></tr><tr><td>

Work notes

</td><td>

Optional field for capturing internal work notes.

</td></tr></tbody>
</table>9.  Select **Save**.

10. On the Sequence Steps tab, select **Mark Complete** to indicate you have finished all activities in the sequence task.


**Parent Topic:**[Using Customer Engagement Sequences](../concept/using-customer-engagement-sequences.md)

**Related topics**  


[View sequence tasks](view-sequence-tasks.md)

