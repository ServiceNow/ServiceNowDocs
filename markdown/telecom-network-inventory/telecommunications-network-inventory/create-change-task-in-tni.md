---
title: Create and execute a change task in Telecommunications Network Inventory
description: Created topic as per DOC1072352 - STRY55259624Create a change task after you create a change request in the Telecommunications Network Inventory application. By creating a change task, you can complete the requested change.
locale: en-US
release: xanadu
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Instantiating your network inventory by using design and assign, Using Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Create and execute a change task in Telecommunications Network Inventory

Create a change task after you create a change request in the Telecommunications Network Inventory application. By creating a change task, you can complete the requested change.

## Before you begin

-   1.  Navigate to **Telecom Network Inventory** &gt; **Inventory Models**, create your inventory models, and define their relationships.

    To learn more, see [Manually creating and reviewing your network asset instances](../concept/creating-telecommunications-network-inventory.md).

2.  Navigate to **Telecom Network Inventory** &gt; **Network Inventory Templates**, create the inventory templates for your equipment, and establish the template relationships.

    To learn more, see [Creating inventory template for network asset instantiation](../concept/preparing-inv-templates-network-asset-generation.md).

-   Role required: sn\_ni\_core.inventory\_template\_manager, sn\_ni\_core.inventory\_admin, sn\_ni\_core.telco\_inventory\_catalog\_manager, sn\_ni\_core.inventory\_agent.

## About this task

Based on the details in the change request form, a change task is created automatically. You can view, create, update, or close the change tasks from the **Overview** tab or from the **Change Tasks** tab of a change request. You can also assign a record producer form to a change task. To learn more, see [Assign a record producer form for a request type of a change task](assign_record_producer_form_for_a_change_task_of_a_change_request.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Changes** &gt; **All**.

3.  Open your change request.

4.  On the **Overview** tab, scroll down and expand the Change task section.

5.  Select the **Change Tasks** tab.

6.  After a change request is created, on the **Overview** tab, scroll down and expand the Change task section.

    You can also navigate to the **Overview** tab and initiate the creation of a change task.

7.  Select **New**.

8.  Choose a change task type:

    -   Planning
    -   Implementation
    -   Testing
    -   Review
9.  Select **Create**.

    A change task form that is based on the selected change model is displayed.

10. Select the existing change task.

11. On the form, fill in the fields.

    To learn more about the fields, see [Change request and change task forms](../concept/change_request_forms.md).

    **Note:** For the design assign link aggregation group and GPON broadband service, see [Create a change request by using the design assign link aggregation](create_a_change_request_by_using_the_design_assign_link_aggregation_group.md) and [Create a change request by using the GPON Broadband Service change model](gpon-broadband-change-model.md).

12. Select **Submit**.

    The **Details** tab is updated with the provided details and required modification to the CI is performed. All performed changes are updated in the work notes. To learn more about the fields, see [Change request and change task forms](../concept/change_request_forms.md).

    **Note:** The removal of equipment or a shelf from a rack also removes all associated CI relationships between the equipment/shelf and the rack, along with the selected CI.

13. On the **Affected CIs** related tab, see all the configuration items that are impacted due to this change task.

    After creating a rack, navigate to **Configuration item**, or **Affected CIs** to visualize the front view and rear view of a rack.

14. If your change model is a rack, select the **Configuration item** to visualize the rack.

15. Select **Save**.


**Parent Topic:**[Instantiating your network inventory by using design and assign](../concept/instantiate-asset-using-template-relationship-model.md)

