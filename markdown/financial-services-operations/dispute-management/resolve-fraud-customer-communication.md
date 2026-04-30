---
title: Manage customer communication
description: Provide a response and feedback to the customer for a decision made on a dispute, such as friendly fraud.
locale: en-US
release: zurich
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Investigation, Resolving disputes without network integration, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Manage customer communication

Provide a response and feedback to the customer for a decision made on a dispute, such as friendly fraud.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

## About this task

When you select the **Decline dispute transaction** option in the **Detect friendly fraud** activity, the **Customer communication** activity is displayed. Provide the customer feedback and the reason. You can accept or deny the response.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select which case you want to work on.

    If you want to work on a case that isn't assigned to you yet, you can assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

6.  Select the transaction ID in the transaction level playbook of the **Processing** tab.

    The **Investigate** stage is initiated for the transaction.

7.  Select the **Customer communication** activity.

8.  Select the **Customer decision** as **Accepted** or **Denied**.

    -   When the customer decision is accepted, provide **Customer feedback** and select **Mark complete**. The dispute is marked as **Closed Complete**.
    -   When the customer decision is denied, provide the **Customer feedback**. In the **Action** section, select one of the following.
<table id="choicetable_mzh_qdg_w2c"><thead><tr><th align="left" id="d56119e221">

Final action

</th><th align="left" id="d56119e224">

Steps

</th></tr></thead><tbody><tr><td id="d56119e230">

**Decline dispute transaction**

</td><td>

1.  Provide a **Resolution reason**.
2.  Select **Mark complete**.

The transaction is marked as**Closed Rejected**.

</td></tr><tr><td id="d56119e259">

**Issue credit and write-off**

</td><td>

1.  Provide the **Resolution reason**.
2.  Select **Mark complete**.

The **Issue credit** activity is displayed.

3.  Provide the final credit and select **Close task**. The task is marked as **Closed Complete.**


</td></tr><tr><td id="d56119e296">

**Proceed with dispute**

</td><td>

1.  Provide a **Resolution reason**.
2.  Select **Mark complete**.

The next activity **Report fraud** is displayed.

3.  Proceed with activities in the playbook as required. For more information about resolving fraud, see [Report fraud to a card network](report-fraud-to-card-network.md).


</td></tr></tbody>
</table>
**Parent Topic:**[Investigating a dispute](investigate-a-dispute.md)

