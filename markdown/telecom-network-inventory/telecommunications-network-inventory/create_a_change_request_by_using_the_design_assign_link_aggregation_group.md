---
title: Create a Link Aggregation Group using design and assign function
description: Added as per STRY55494783 - DOC1073902Design and assign a Link Aggregation Group \(LAG\) with the creation of Ethernet connections in the Telecommunications Network Inventory application. By creating a LAG connection, you can fulfill an order request from the customer.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Using Design &amp; Assign Network, Use, Telecommunications Network Inventory]
---

# Create a Link Aggregation Group using design and assign function

Design and assign a Link Aggregation Group \(LAG\) with the creation of Ethernet connections in the Telecommunications Network Inventory application. By creating a LAG connection, you can fulfill an order request from the customer.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Changes** &gt; **All**.

3.  Select the **New** button.

4.  Select **Design assign link aggregation group**.

5.  Select **Next**.

6.  On the Provision LAG form, fill in the fields.

    To learn more about the fields, see [Provision LAG form](../reference/provision-lag-form.md).

7.  Select **Submit**.

    A new change request is created and the Change TNI LAG Template workflow is triggered. Three change tasks have been created.

8.  Expand the change task section on the **Overview** tab or select the **Change Tasks** tab.

    **Note:** To learn more about the **Overview** tab, see [Create a change request from Network Inventory Workspace](create_a_change_request_in_tni.md).

    To create change tasks, see [Create and execute a change task](create-change-task-in-tni.md).

9.  Open a task.

10. On the **Details** tab, on the change task form, fill in the fields.

    For a description of the field values, see the Change task form in [Change request and change task forms](../concept/change_request_forms.md).

11. Create, review, update, or delete an affected configuration item by selecting the **Affected CIs** related tab.

12. Select **Save**.


## What to do next

Add or remove a member to LAG using [Add or remove a member to Link Aggregation](create-a-change-request-to-add-or-remove-member-to-link-aggregation.md).

**Parent Topic:**[Instantiating inventory using design and assign](../concept/instantiate-asset-using-template-relationship-model.md)

