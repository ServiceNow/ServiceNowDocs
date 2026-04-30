---
title: Make a decision on chargeback, write off, or transaction denial
description: Determine whether to initiate a chargeback for a transaction if the cardholder hasn’t yet received the final credit.
locale: en-US
release: zurich
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Investigate, Processing a Mastercard dispute, Resolving disputes with Mastercard, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Make a decision on chargeback, write off, or transaction denial

Determine whether to initiate a chargeback for a transaction if the cardholder hasn’t yet received the final credit.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector.

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

Recovery option task to choose whether to pursue chargeback for a transaction where final credit to the card holder is provided.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select which case you want to work on.

    If you want to work on a case that isn't assigned to you yet, you can assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

6.  In the **Processing** tab, select the transaction ID.

7.  Select the **Make decision on chargeback, write off or transaction denial** task in **Dispute Workspace**.

8.  On the form, fill in the required fields and any other related information.

9.  In the **Pursue recovery** drop-down, select one of the following.

<table id="choicetable_gwh_bjs_3fcc"><tbody><tr><td id="d90415e217">

**Yes**

</td><td>

The relevant tasks for the transaction trigger for the **Chargeback** stage.

</td></tr><tr><td id="d90415e229">

**No**

</td><td>

The **Deny dispute** drop-down is displayed. Select one of the following options:-   **Yes** to deny the dispute. No credit is provided to the cardholder for the disputed transaction. The dispute life-cycle ends.
-   **No** to write off the final credit to the card holder. The task moves forward based on the policy. For more information about Financial adjustments, see [About Financial adjustments in Mastercard disputes](../concept/financial-adjustments.md).


</td></tr></tbody>
</table>10. Select **Add file** to attach supporting documents to the task.

    **Note:** You must upload a single `.zip` file whenever you submit documents to Mastercard.

11. Select **Continue**.


## Result

If the decision is to deny the dispute, the transaction task state updates to **Closed complete**.

**Parent Topic:**[Processing a Mastercard dispute](../concept/processing-mastercard-dispute-case.md)

