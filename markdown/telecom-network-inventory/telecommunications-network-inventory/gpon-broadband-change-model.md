---
title: Design your GPON Broadband Service
description: The GPON broadband service change model creates and orchestrates multiple change tasks required to fulfill a GPON broadband service order.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Using Design &amp; Assign Network, Use, Telecommunications Network Inventory]
---

# Design your GPON Broadband Service

The GPON broadband service change model creates and orchestrates multiple change tasks required to fulfill a GPON broadband service order.

## Before you begin

Before establishing a GPON Broadband Service change request and completing the related change tasks, inventory catalog managers and template managers must complete the following network configuration setup.

1.  Navigate to **Telecom Network Inventory** &gt; **Inventory Models**, create your inventory models, and define their relationships.

    To learn more, see [Manually create and review your network asset instances](../concept/creating-telecommunications-network-inventory.md).

2.  Navigate to **Telecom Network Inventory** &gt; **Network Inventory Templates**, create the inventory templates for your equipment, and establish the template relationships.

    To learn more, see [Create inventory template for network asset instantiation](../concept/preparing-inv-templates-network-asset-generation.md).


Install the Telecommunications Network Inventory Advanced and Core demo data.

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Changes** &gt; **All**.

3.  Select the **New** button.

4.  Select **GPON Broadband Service** &gt; **Next**.

5.  On the GPON Broadband form select the **Customer Site name**.

    Other fields are pre-populated but can be updated as needed.. To learn more about the fields, see [Change request and change task forms](../concept/change_request_forms.md).

6.  Select **Submit**.

    The change request is created based on your input and GPON Broadband service form appears with relevant tabs. To learn more, see [Change request related tabs](../reference/tni-change-request-related-tabs.md)

7.  Select an **Assignment group.**

8.  Select **Save.**

9.  The system automatically creates change tasks and displays them in the **Change Tasks**tab.For more information see [Change request related tabs](../reference/tni-change-request-related-tabs.md)

10. Switch to **Change Task** tab and click on the change task to review it.

    In the change task tab, you will find the change request number, request status and other related tabs.

11. Click on Affected CIs tab, to view the configuration items affected by this change task.

12. Select **Save**.


**Parent Topic:**[Instantiating inventory using design and assign](../concept/instantiate-asset-using-template-relationship-model.md)

