---
title: Configure the Accounts Payable Operations queues
description: Configure AWA for Accounts Payable Operations queues so that email, chat, and requests raised by suppliers are routed to respective agents belonging to the Accounts Payable supplier group.
locale: en-US
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Advanced Work Assignment for Accounts Payable Operations, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Configure the Accounts Payable Operations queues

Configure AWA for Accounts Payable Operations queues so that email, chat, and requests raised by suppliers are routed to respective agents belonging to the Accounts Payable supplier group.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **Source to Pay Workspace** &gt; **All** &gt; **Advanced Work Assignment** &gt; **&gt;Queues**.

2.  Select one of the following mentioned queues for Account Payable Operations.

    -   Invoice Inquiry case
    -   Chat
3.  In the **Assignment Eligibility related** list, select **New**.

    1.  In the **Agent assignment rule** field, select **Chat - Most Capacity**.
    2.  Select the lock icon \(![Lock icon](../../supplier-lifecycle-operations/image/lock-icon.png)\) next to the **Groups** field.
    3.  Select the look-up icon \(![Look-up icon](../../supplier-lifecycle-operations/image/look-up-icon.png)\) to view the list of groups.
    4.  Select **New**.
    5.  In the **Name** field, enter a name for the group.
    6.  Fill in the remaining fields, as appropriate.
    7.  Select **Submit**.
    8.  Select the lock icon \(![Lock icon](../../supplier-lifecycle-operations/image/lock-icon.png)\) to lock the **Groups** field.
    9.  Right-select and select **Save**.
4.  Next to the **Groups** field, select the link to the group, which opens the group record.

    1.  In the Group Members related list, select **Edit** to add members to the group.
    2.  Select one or more users in the Collection list and move them to the Group Members List.
    3.  Select **Save**.

        **Note:** The users that you add to this assignment group are automatically granted the awa\_agent role.


**Parent Topic:**[Configure Advanced Work Assignment for Accounts Payable Operations](configure-advanced-work-assignment-for-apo.md)

