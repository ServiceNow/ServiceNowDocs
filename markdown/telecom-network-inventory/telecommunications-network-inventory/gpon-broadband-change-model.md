---
title: Create a change request by using the GPON Broadband Service change model
description: Create a change request in the Telecommunications Network Inventory application so that you can design a Gigabyte Passive Optical Network \(GPON\) broadband service. The GPON Broadband Service change model enables you to create multiple change tasks so that you can fulfill an order request for a GPON broadband service.
locale: en-US
release: xanadu
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Create a change request from Network Inventory Workspace, Instantiating your network inventory by using design and assign, Using Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Create a change request by using the GPON Broadband Service change model

Create a change request in the Telecommunications Network Inventory application so that you can design a Gigabyte Passive Optical Network \(GPON\) broadband service. The GPON Broadband Service change model enables you to create multiple change tasks so that you can fulfill an order request for a GPON broadband service.

## Before you begin

Before you can establish a GPON Broadband Service change request and complete the related change tasks, your inventory catalog and template managers must do the following network configuration setup:

1.  Navigate to **Telecom Network Inventory** &gt; **Inventory Models**, create your inventory models, and define their relationships.

    To learn more, see [Manually creating and reviewing your network asset instances](../concept/creating-telecommunications-network-inventory.md).

2.  Navigate to **Telecom Network Inventory** &gt; **Network Inventory Templates**, create the inventory templates for your equipment, and establish the template relationships.

    To learn more, see [Creating inventory template for network asset instantiation](../concept/preparing-inv-templates-network-asset-generation.md).


Install the Telecommunications Network Inventory Advanced and Core demo data.

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Changes** &gt; **All**.

3.  Select the **New** button.

4.  Select **GPON Broadband Service** &gt; **Next**.

5.  On the record producer form, you can update the fields.

    The fields of the record producer form are auto-populated. This demonstration displays how to create configuration items \(CIs\) to show the design and assign of a GPON broadband service. You can change the flow as needed. To learn more about the fields, see [Change request and change task forms](../concept/change_request_forms.md).

6.  Select **Save**.

    The Change \(Design &amp; Assign\) flow is triggered and a change request is created. Depending on the given inputs, change tasks are automatically created and other related tabs appear. To learn more, see [Change request related tabs](../reference/tni-change-request-related-tabs.md).

7.  Open and review each change task record.

    On the Task Attributes form, fill in the fields. For a description of the field values, see [Change request and change task forms](../concept/change_request_forms.md).

8.  Select **Submit**.

    The **Details** tab is updated.

9.  On the **Affected CIs** related tab, see all the configuration items that are impacted due to this change task.

10. Select **Save**.


**Parent Topic:**[Create a change request from Network Inventory Workspace](create_a_change_request_in_tni.md)

