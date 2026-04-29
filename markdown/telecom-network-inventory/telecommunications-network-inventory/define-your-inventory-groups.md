---
title: Define your inventory groups
description: An inventory group is a collection of CIs that lets you apply CI actions collectively to all the CIs in Telecommunications Network Inventory application. By defining inventory groups, you can group different CIs, and apply actions to all CIs.Added as per DOC1059334
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manually creating and reviewing your network asset instances, Define inventory records, Use, Telecommunications Network Inventory]
---

# Define your inventory groups

An inventory group is a collection of CIs that lets you apply CI actions collectively to all the CIs in Telecommunications Network Inventory application. By defining inventory groups, you can group different CIs, and apply actions to all CIs.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent

**Note:** An inventory agent and inventory admin only can review, create, and update an inventory group. Also, only an inventory admin can delete a group.

## About this task

An inventory group represents a group of configuration items\(CIs\). In a group, you can add any CI but you cannot be duplicate a CI.

When you create an inventory group, it creates a group in the inventory group\[cmdb\_group\] table. To learn more, see [Data model](../concept/uses-for-network-inventory-data.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Click the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then click **Inventory** &gt; **Inventory Groups**

3.  Click **New**.

4.  On the **Details** tab, in the CMDB Group section, fill the form.

<table id="table_xgs_534_1vb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Group Name

</td><td>

Name of the inventory group

</td></tr><tr><td>

Group type

</td><td>

Select one of the following group type-   CMDB Workspace or Service Graph Workspace
-   Default
-   Health
-   Network Inventory Group


</td></tr><tr><td>

Description

</td><td>

Describe your inventory group

</td></tr><tr><td>

Category

</td><td>

Select one of the following category-   Segment
-   Section
-   Route
-   Others


</td></tr></tbody>
</table>5.  To add the attachments, such as graphics or documents, click the attachment icon \(![Attachment icon.](../image/attachments-icon.png)\) in the right panel.

6.  Click **Save**.

    The related tabs appear on the form. You can view or modify the related tab information. To learn more about the related tabs, see [Related tabs in the Network inventory forms](../reference/inventory-related-tab.md).

    **Note:** To see the last modified or updated information, see the list view of the Inventory Groups.


## What to do next

If you want to establish relationships with the other network assets, enter the details in the related tabs. To learn more, see [Related tabs in the Network inventory forms](../reference/inventory-related-tab.md).

**Parent Topic:**[Manually creating and reviewing your network asset instances](../concept/creating-telecommunications-network-inventory.md)

