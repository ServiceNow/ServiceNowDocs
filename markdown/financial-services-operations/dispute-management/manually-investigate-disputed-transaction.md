---
title: Manually investigate a disputed transaction
description: If a merchant refuses a transaction dispute, the case may move to the manual investigation task.
locale: en-US
release: xanadu
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Investigating a dispute, Work on a dispute case, Managing dispute service requests, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Manually investigate a disputed transaction

If a merchant refuses a transaction dispute, the case may move to the manual investigation task.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

When a case moves to the Manual investigation task, a dispute agent reviews case details to determine if there is potential fraud involved. For transactions disputed under the reason of “Unrecognized transaction” or “Stolen card”, the selection made from the Potential fraud field determines the next steps that the case moves to. For other dispute reasons the dispute agent makes a decision to either proceed with chargeback or deny the disputed transaction.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon.](../image/list-icon.png)\).

3.  In the **Lists** tab, under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select the case to work on.

    To work on a case that is not assigned to you yet, assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

6.  Select the **Manual investigation** activity under the Investigation playbook stage.

7.  Select the manual investigation task that you want to complete.

8.  On the form, fill in the required fields and any other related information that you've gathered.

9.  In the **Work notes** field, enter any comments.

10. Select **Update** to save your changes.

11. Select **Submit for approval**.

    The case is submitted for a review and approval to the dispute manager.

12. Close the task from the playbook.

<table id="choicetable_dpp_ngx_f5b"><thead><tr><th align="left" id="d65489e213">

Dispute activity

</th><th align="left" id="d65489e216">

Action

</th></tr></thead><tbody><tr><td id="d65489e222">

**To close the Manual investigation task**

</td><td>

Select whether to create a chargeback request:-   **Create chargeback**- Select to pursue a chargeback from the merchant.
-   **No chargeback**- Select to indicate not to pursue chargeback from the merchant.


</td></tr></tbody>
</table>
## Result

The task state updates to Closed Complete.

-   If fraud was not flagged during the Manual investigation task, the disputed transaction updates to Closed Complete.
-   If fraud was flagged by the agent during the task, the case moves to the Fraud reporting task within the Chargeback stage.

**Parent Topic:**[Investigating a dispute](investigate-a-dispute.md)

