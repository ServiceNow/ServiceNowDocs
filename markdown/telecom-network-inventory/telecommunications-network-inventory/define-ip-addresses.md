---
title: Create IP addresses
description: Created topic as per DOC1058818.Define the attributes for IP addresses so that you can track and manage them in the Telecommunications Network Inventory application. You can also review, update, or create IP addresses.
locale: en-US
release: xanadu
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Create IP address allocation, Inventory number allocation, Reviewing and updating your network inventory with the Network Inventory Workspace, Using Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Create IP addresses

Define the attributes for IP addresses so that you can track and manage them in the Telecommunications Network Inventory application. You can also review, update, or create IP addresses.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent, sn\_ni\_core.inventory\_template\_manager, sn\_ni\_core.telco\_inventory\_catalog\_manager

## About this task

**Note:** An inventory agent can create, review, update, and delete an IP address.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Inventory** &gt; **IP Addresses**.

3.  Select **New**

4.  On the **Details** tab, in the IP address section, fill in the general information.

<table id="table_rdn_tqg_w5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

IP Address

</td><td>

Name of this network function that you use in the ServiceNow AI Platform to identify it in your network inventory.

</td></tr><tr><td>

IP Version

</td><td>

Name of the database. Select one from the following:-   IPv4 - Fourth version of the Internet Protocol,
-   IPv6 - Sixth version of the Internet Protocol


</td></tr><tr><td>

Netmask

</td><td>

Unique ID of the network instance.

</td></tr><tr><td>

Owned by Configuration item

</td><td>

Type of network function, Virtual Network Function \(VNF\), or Cloud Native Function \(CNF\).

</td></tr></tbody>
</table>5.  To create the Telecommunications Network Inventory attributes for this IP pool form, select the **Set Inventory Attributes** button.

    When you select the **Set Inventory Attributes** button, it creates the TNI CI Attributes record in the CI table as well as the Telecommunications Network Inventory CI Attributes tables and makes a relationship with the CI record.

    **Note:**

    -   If you select **Save** without selecting **Set Inventory Attributes**, it creates a CI record but not a Telecommunications Network Inventory CI record. In the network inventory workspace, the **Set Inventory Attributes** is visible only for the Telecommunications Network Inventory roles.
    -   In the TNI CI attributes form, by default, the name is fetched from the **Name** field and the **Inventory Category** is set as **IP Address**.
6.  Select **Add Packs** to add packs to this service.

    To learn more about packs, see [Attribute packs](../concept/telecommunication-network-inventory-pack.md).

7.  To add the attachments, such as graphics or documents, select the attachment icon \(![Attachment icon.](../image/attachments-icon.png)\) in the right panel.

8.  Select **Save**.

    The related tabs appear on the form. You can view or modify the related tab information. To learn more about the related tabs, see [Related tabs in the Network inventory forms](../reference/inventory-related-tab.md).

9.  To view the associated network inventories, select the brick icon \(![brick icon](../image/infrastructure-relashionship.png)\).

    The Infrastructure Relationships section shows all the associated network inventories that are grouped by the individual network instances.


## What to do next

You can review, or update the fields, create a related tab record, or can delete a record. To learn more, see [Update or delete a record of an inventory number allocation](update_and_delete_ip_address_space.md).

**Parent Topic:**[Create IP address allocation](../concept/ip_pool_ip_network_subnet_allocated_ip_address_and_ip_address.md)

