---
title: Create an IP network subnet record
description: Created topic as per DOC1067583Define an IP network subnet so that you can categorize and manage all the child IP network subnets in your network by using the Telecommunications Network Inventory application. You can also review, create, or delete an IP subnetwork.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create IP address allocation, Inventory number allocation, Defining inventory records, Use, Telecommunications Network Inventory]
---

# Create an IP network subnet record

Define an IP network subnet so that you can categorize and manage all the child IP network subnets in your network by using the Telecommunications Network Inventory application. You can also review, create, or delete an IP subnetwork.

## Before you begin

-   Get access to the IP subnetwork by ensuring that you’ve installed all advanced plugins.
-   Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent

## About this task

When you create a IP network subnet record, it creates a corresponding configuration item \(CI\) record in the IP Network Subnet \[cmdb\_ci\_ip\_network\_subnet\] table.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Inventory** &gt; **IP Network Subnets**.

3.  Select **New**

4.  On the **Details** tab, in the IP Network Subnet section, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|User-friendly name for this IP network subnet.|

    To learn about the other fields, see [Inventory number allocation fields](../reference/inventory-number-allocation-fields.md).

5.  Create the Telecommunications Network Inventory attributes for this IP network subnet form by selecting **Set Inventory Attributes**.

    When you select the **Set Inventory Attributes** button, it creates the TNI CI Attributes record in the CI table and in the Telecommunications Network Inventory CI Attributes tables and makes a relationship with the CI record.

    **Note:**

    -   If you select **Save** without selecting **Set Inventory Attributes**, it creates a CI record but not a Telecommunications Network Inventory CI record. In the network inventory workspace, the **Set Inventory Attributes** is visible only for the Telecommunications Network Inventory roles.
    -   In the TNI CI attributes form, by default, the name is fetched from the **Name** field and the **Inventory Category** is set as **IP Address**.
6.  Add packs to this service by selecting **Add Packs**.

    To learn more about the packs, see [Attribute packs](../concept/telecommunication-network-inventory-pack.md).

7.  Add the attachments, such as the graphics or documents, by selecting the attachment icon \(![Attachment icon.](../image/attachments-icon.png)\) in the right panel.

8.  Select **Save**.

9.  View the hierarchy or flow chart of the created IP pool by selecting the **Dependency View** button.

10. View the associated network inventories by selecting the brick icon \(![brick icon.](../image/infrastructure-relashionship.png)\).

    The Infrastructure Relationships section shows all the associated network inventories that are grouped by the individual network instances.


## What to do next

You can review and update the fields, create a related tab record, or delete a record. To learn more, see [Update or delete a record of an inventory number allocation](update_and_delete_ip_address_space.md).

**Parent Topic:**[Create IP address allocation](../concept/ip_pool_ip_network_subnet_allocated_ip_address_and_ip_address.md)

