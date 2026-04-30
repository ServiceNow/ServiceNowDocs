---
title: Create an allocated IP address record
description: Define and categorize all IP addresses that are ready for allocation by using the Telecommunications Network Inventory application. You can review, create, update, or delete an allocated IP address in your network. Created topic as per DOC1067583
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Create IP address allocation, Inventory number allocation, Defining inventory records, Use, Telecommunications Network Inventory]
---

# Create an allocated IP address record

Define and categorize all IP addresses that are ready for allocation by using the Telecommunications Network Inventory application. You can review, create, update, or delete an allocated IP address in your network.

## Before you begin

-   Get access to an IP subnetwork by ensuring that you install all advanced plugins.
-   Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent

## About this task

To understand how the IP pools, IP subnetworks, and allocated IP addresses are related to each other, see [IP address inventory management data model](../reference/data_model_of_ip_address_inventory_management.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Inventory** &gt; **Allocated IP Addresses**.

3.  Select **New**.

4.  On the **Details** tab, in the IP address section, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|User-friendly name for this IP address.|
    |IP Address|IPv4 or IPv6 IP address.|
    |Is Broadcast|Value that you set to true if this IP address is a broadcast type IP address.|
    |Is DHCP|Value that you set to true to override the Grid Level DHCP option with this option at the network level.|
    |Is DNS|Value that you set to true if a Domain Name System \(DNS\) name is provided for this IP address.|

5.  Create the Telecommunications Network Inventory attributes for this IP pool form by selecting the **Set Inventory Attributes** button.

    When you select the **Set Inventory Attributes** button, it creates the TNI CI Attributes record in the CI table and the Telecommunications Network Inventory CI Attributes tables and makes a relationship with the CI record.

    **Note:**

    -   If you select **Save** without selecting the **Set Inventory Attributes** button, it creates a CI record but not a Telecommunications Network Inventory CI record. In the network inventory workspace, the **Set Inventory Attributes** is visible only for the Telecommunications Network Inventory roles.
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

