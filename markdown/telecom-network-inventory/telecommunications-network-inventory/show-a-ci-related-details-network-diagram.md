---
title: View the details of a network diagram
description: View the details of a connection node and visualize the underlying connection elements of a logical connection by using the network diagram in the Telecommunications Network Inventory. You can understand the detailed overview of the logical connection and how the connection elements are connected to each other.
locale: en-US
release: yokohama
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Using the network diagram, Using Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# View the details of a network diagram

View the details of a connection node and visualize the underlying connection elements of a logical connection by using the network diagram in the Telecommunications Network Inventory. You can understand the detailed overview of the logical connection and how the connection elements are connected to each other.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent

## About this task

With the use of a network diagram, you can do the following:

-   Drill down into the network diagram to view the underlying elements.
-   View the details of a connection node that makes up the network diagram.
-   View the details of the revision of a logical connection.
-   View the protection paths for a logical connection.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon](../image/ni-workspace-list-icon.png)\).

3.  Go to **Inventory** &gt; **Logical Connections**.

4.  Open a record and then select **View connection**.

5.  View the underlying elements or the details of the connection node.

    On the network diagram you can do the following actions:

<table id="choicetable_qtk_fr3_yxb"><thead><tr><th align="left" id="d28748e129">

Option

</th><th align="left" id="d28748e132">

Details

</th></tr></thead><tbody><tr><td id="d28748e138">

**Expand the network diagram and view the underlying elements**

</td><td>

1.  Expand the hierarchy level by selecting the add icon \(![Add Icon](../image/icon-add-circuit.png)\) on the connection node.
2.  Expand further by selecting the add icon \(![Add Icon](../image/icon-add-circuit.png)\) of the underlying connection nodes.
 **Note:** When there are underlying connection elements in a logical connection, the connection node appears as a stacked pill shape. After expansion, it transforms into a box shape.

</td></tr><tr><td id="d28748e171">

**View the revision of the logical connection**

</td><td>

1.  Select the clock icon \(![Clock Icon.](../image/icon-clock.png)\). The revision of the logical connection is displayed on the **Revision view** tab

**Note:** The clock icon \(![Clock Icon.](../image/icon-clock.png)\) is displayed on the map only when the logical connection record has a revision.

2.  Select **Current view** to view the original logical connection.
 You can toggle the view between the original logical connection and revision of the logical connection to compare the differences.

</td></tr><tr><td id="d28748e212">

**View the protection path**

</td><td>

Select the protection path icon \(![Protection Path Icon.](../image/icon-protection-path.png)\) to view the protection paths for the logical connection.**Note:** The protection path icon \(![Protection Path Icon.](../image/icon-protection-path.png)\) is displayed on the map only when the logical connection record has a protection path.

You can’t expand the underlying connection elements of a protection path. To view the details of the protection path, select the protection path node, and then select **View Details** in the details pane.

To learn more about to create a protection path, see [Create a protection path](create-a-protection-path.md).

</td></tr><tr><td id="d28748e252">

**View the details of a connection node**

</td><td>

1.  Select the connection node and view the related information in the details pane.
2.  Redirect to the CI record by selecting **View Details** in the details pane.


</td></tr></tbody>
</table>
**Parent Topic:**[Using the network diagram](../concept/using-network-diagram.md)

**Related topics**  


[Download a network diagram](download-network-diagram.md)

[Create a protection path](create-a-protection-path.md)

[Visualization of circuits](../concept/unified-map-view-of-connection-elements.md)

