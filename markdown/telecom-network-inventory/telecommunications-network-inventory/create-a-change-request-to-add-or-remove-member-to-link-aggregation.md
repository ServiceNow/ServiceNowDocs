---
title: Add or remove a member to Link Aggregation
description: Created topic as per STRY55939345 - DOC1079350Create a change request to add or remove a member to the design assign link aggregation change request by using the Telecommunications Network Inventory application.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Design &amp; Assign Network, Use, Telecommunications Network Inventory]
---

# Add or remove a member to Link Aggregation

Create a change request to add or remove a member to the design assign link aggregation change request by using the Telecommunications Network Inventory application.

## Before you begin

Role required: sn\_ni\_core.inventory\_agent

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Changes** &gt; **All**.

3.  Select the **New** button.

4.  Select **Add/Remove member to Link Aggregation**.

5.  Select **Next**.

6.  On the Add/Remove member to Link Aggregation form, fill in the fields.

    To learn more about the fields, see [Add or Remove member to Link Aggregation form](../reference/add-remove-member-link-aggregation-form.md).

7.  Select **Submit**.

8.  Select the **Affected CIs** tab.

9.  Select the revised CI having V1 as the suffix.

    The revised CI is added under the **Affected CIs** tab only if the **Create revision** check box is selected.

10. Modify the fields as required.

    -   Adding a new member interface automatically creates a new ENET with a corresponding logical interface.
    -   Adding an interface that belongs to an existing ENET connection, the system automatically links it to the existing ENET connection instead of creating an ENET.
11. Create a change task for operationalization.

    To learn more, see [Operationalize a configuration item](operationalize-a-configuration-item.md).


**Parent Topic:**[Instantiating inventory using design and assign](../concept/instantiate-asset-using-template-relationship-model.md)

