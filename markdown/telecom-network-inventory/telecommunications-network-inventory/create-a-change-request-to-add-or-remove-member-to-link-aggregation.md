---
title: Create a change request to Add or remove a member to Link Aggregation
description: Created topic as per STRY55939345 - DOC1079350Create a change request to add or remove a member to the design assign link aggregation change request by using the Telecommunications Network Inventory application.
locale: en-US
release: xanadu
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Create a change request by using the design assign link aggregation, Create a change request from Network Inventory Workspace, Instantiating your network inventory by using design and assign, Using Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Create a change request to Add or remove a member to Link Aggregation

Create a change request to add or remove a member to the design assign link aggregation change request by using the Telecommunications Network Inventory application.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Changes** &gt; **All**.

3.  Select the **New** button.

4.  Select **Add/Remove member to Link Aggregation**.

5.  Select **Next**.

6.  On the form, fill in the fields.

<table id="table_r53_swg_rzb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

LAG

</td><td>

Select a LAG from the list

</td></tr><tr><td>

Bandwidth

</td><td>

Modify or select a bandwidth from the list for the selected LAG

</td></tr><tr><td>

Create revision

</td><td>

Option to create a revision of the selected LAG.**Note:** Revision of a LAG is not possible while it is already undergoing an active revision process.

</td></tr><tr><td>

Member interface A

</td><td>

Interface A of the selected LAG. Add or remove to modify the member interface A of the selected LAG.**Note:** The list displays only child model interfaces that are set as either Port A or Port Z of a physical connection.

</td></tr><tr><td>

Member interface Z

</td><td>

Interface Z of the selected LAG. Add or remove to modify the member interface Z of the selected LAG.**Note:** The list displays only child model interfaces that are set as either Port A or Port Z of a physical connection.

</td></tr></tbody>
</table>7.  Select **Submit**.

8.  Select the **Affected CIs** tab.

9.  Select the revised CI having V1 as the suffix.

    The revised CI is added under the **Affected CIs** tab only if the **Create revision** check box is selected.

10. Modify the fields as required.

    -   Adding a new member interface automatically creates a new ENET with a corresponding logical interface.
    -   Adding an interface that belongs to an existing ENET connection, the system automatically links it to the existing ENET connection instead of creating an ENET.
11. Create a change task for operationalization.

    To learn more, see [Operationalize a configuration item](operationalize-a-configuration-item.md).


**Parent Topic:**[Create a change request by using the design assign link aggregation](create_a_change_request_by_using_the_design_assign_link_aggregation_group.md)

