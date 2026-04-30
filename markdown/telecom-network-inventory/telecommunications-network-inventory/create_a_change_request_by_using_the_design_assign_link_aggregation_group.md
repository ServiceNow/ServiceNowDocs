---
title: Create a change request by using the design assign link aggregation
description: Added as per STRY55494783 - DOC1073902Create a design assign link aggregation change request by using the Telecommunications Network Inventory application. You can also review, update, or delete a record of the design assign link aggregation group.
locale: en-US
release: xanadu
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Create a change request from Network Inventory Workspace, Instantiating your network inventory by using design and assign, Using Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Create a change request by using the design assign link aggregation

Create a design assign link aggregation change request by using the Telecommunications Network Inventory application. You can also review, update, or delete a record of the design assign link aggregation group.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Changes** &gt; **All**.

3.  Select the **New** button.

4.  Select **Design assign link aggregation group**.

5.  Select **Next**.

6.  On the Record producer form, fill in the fields.

    For a description of the field values, see the form in [Change request and change task forms](../concept/change_request_forms.md).

    **Note:** By default, the Record producer form is assigned to the design and assign aggregation group. For other change models, see [Assign a record producer form to a change model](create_record_producer_form_for_a_change_request.md).

7.  Select **Submit**.

    A new change request is created and the Change TNI LAG Template workflow is triggered. Three change tasks have been created.

8.  Expand the change task section on the **Overview** tab or select the **Change Tasks** tab.

    **Note:** To learn more about the **Overview** tab, see [Create a change request from Network Inventory Workspace](create_a_change_request_in_tni.md).

    To create change tasks, see [Create and execute a change task in Telecommunications Network Inventory](create-change-task-in-tni.md).

9.  Open a task.

10. On the **Details** tab, on the change task form, fill in the fields.

    For a description of the field values, see the Change task form in [Change request and change task forms](../concept/change_request_forms.md).

11. Create, review, update, or delete an affected configuration item by selecting the **Affected CIs** related tab.

12. Select **Save**.


## What to do next

Add or remove a member to LAG using [Create a change request to Add or remove a member to Link Aggregation](create-a-change-request-to-add-or-remove-member-to-link-aggregation.md).

-   **[Create a change request to Add or remove a member to Link Aggregation](create-a-change-request-to-add-or-remove-member-to-link-aggregation.md)**  
Create a change request to add or remove a member to the design assign link aggregation change request by using the Telecommunications Network Inventory application.

**Parent Topic:**[Create a change request from Network Inventory Workspace](create_a_change_request_in_tni.md)

