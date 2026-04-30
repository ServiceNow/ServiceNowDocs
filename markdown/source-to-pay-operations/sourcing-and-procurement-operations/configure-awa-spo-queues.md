---
title: Configure the Sourcing and Procurement Operations queues
description: Configure the Advanced Work Assignment for Source-to-Pay Operations queues to ensure that email and chat requests are routed and assigned to specific agents belonging to defined groups.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up Advanced Work Assignment for Source-to-Pay Operations, Advanced Work Assignment for Source-to-Pay Operations, Configure, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Configure the Sourcing and Procurement Operations queues

Configure the Advanced Work Assignment for Source-to-Pay Operations queues to ensure that email and chat requests are routed and assigned to specific agents belonging to defined groups.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Queues**.

2.  Select one of these queues specific to Advanced Work Assignment for Source-to-Pay Operations.

    -   General Ledger Accounting Queue
    -   Legal Review for Procurement Queue
    -   Strategy Sourcing Queue
    -   Service Desk &amp; Others Queue
3.  In the Assignment Eligibility related list, select **New**.

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

5.  Repeat steps 3 and 4 for the remaining Advanced Work Assignment for Source-to-Pay Operations queues.


**Parent Topic:**[Setting up Advanced Work Assignment for Source-to-Pay Operations](../concept/awa-spo-setup.md)

