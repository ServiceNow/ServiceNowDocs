---
title: Configure approval rule for a delegate
description: Configure an approval rule for a delegate to ensure that the business owner has better visibility into the request before approval.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure delegate for a shopper, Setting up primary data for ShoppingHub, Configure, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Configure approval rule for a delegate

Configure an approval rule for a delegate to ensure that the business owner has better visibility into the request before approval.

## Before you begin

Role required: admin

## About this task

In Shopping Hub, when a delegate checks out on behalf of the delegator, the default workflow assumes the delegate has full permissions to submit purchase requests \(PRs\). However, you can configure an approval rule to ensure that the first approval request is sent to the business owner \(delegator\). This configuration enables the delegator to review the approval request and decide whether to approve or reject it.

## Procedure

1.  Navigate to **All** &gt; **Sourcing and Purchasing Automation** &gt; **Administration** &gt; **Approval Rules**.

2.  In the form, fill in the fields.

<table id="table_awt_1wc_p2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-generated unique identifier for the approval rule.

</td></tr><tr><td>

Name

</td><td>

The name you assign to the approval rule.

</td></tr><tr><td>

Active

</td><td>

Option to enable the approval rule.

</td></tr><tr><td>

Approving object

</td><td>

Object you’re seeking approval for. Select **Purchase Requisition**.

</td></tr><tr><td>

Approving line

</td><td>

Approving object line that you're seeking approval for. For the Purchase Requisition object, the approving line is defaulted to Purchase Line.

</td></tr><tr><td>

Approval rule type

</td><td>

The type of approval rule that determines how approval plans are generated and routed when conditions are met.The following options are available:

-   Dynamic Users or Groups
-   Managerial Job Code Hierarchy
-   Managerial Hierarchy
-   Specified Users or Groups


</td></tr><tr><td>

Base approvals on

</td><td>

Purchase requisition fields that you want to base your approvals on. Select the **Business owner** field and move it from Available to Selected.

</td></tr><tr><td>

Allow automatic approval

</td><td>

Option to allow automatic approval.**Note:** Ensure that you deselect this option.

</td></tr><tr><td>

Approval trigger conditions

</td><td>

Conditions based on the approving object that determine the conditions under which an approval plan is created.See the following image to understand the approval trigger conditions you need to configure.

</td></tr></tbody>
</table>    ![Approval Rule form for creating a approval rule for a delegate.](../image/config-approval-delegate.png)

3.  Select **Submit**.


**Parent Topic:**[Configure delegate for a shopper](configure-delegate-for-a-shopper.md)

