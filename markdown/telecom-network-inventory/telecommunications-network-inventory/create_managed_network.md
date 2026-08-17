---
title: Create a Managed Network
description: Create a Managed Network record to define a network scope that can be assigned to IP Address Blocks. A Managed Network value propagates to subnetworks and allocated IP records beneath the IP Address Block, and the same CIDR can exist in different Managed Networks without conflict.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/telecom-network-inventory/telecommunications-network-inventory/create\_managed\_network.html
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 2
breadcrumb: [Manage IP addresses, Inventory number allocation, Defining inventory records, Use, Telecommunications Network Inventory]
---

# Create a Managed Network

Create a Managed Network record to define a network scope that can be assigned to IP Address Blocks. A Managed Network value propagates to subnetworks and allocated IP records beneath the IP Address Block, and the same CIDR can exist in different Managed Networks without conflict.

## Before you begin

Install network discovery plugins.

Role required: `sn_ni_core.inventory_admin, sn_ni_core.inventory_agent, sn_ni_core.inventory_template_manager, sn_ni_core.telco_inventory_catalog_manager`

## About this task

The Managed Network record is optional for IP Address Block creation. If you create an IP Address Block without a Managed Network, its CIDR must be globally unique across all unscoped IP Address Blocks. If you create an IP Address Block with a Managed Network assigned, its CIDR must be unique within that Managed Network.

For more information about the propagation rules, see [Managed Network form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/managed_network_form.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace** or **Service Operations Workspace**.

2.  Select the list icon, and then go to **Inventory Number Allocation** &gt; **Managed Network**.

3.  Select **New**.

4.  On the Details tab, fill in the **Name** field.

    For more information about the available fields, see [Managed Network form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/managed_network_form.md).

5.  Add packs to this service by selecting **Add Packs**.

6.  Add attachments, such as graphics or documents, by selecting the attachment icon.

7.  Select **Save**.

8.  View the related network inventories by selecting the brick icon.

    The Infrastructure Relationships section shows all the related network inventories grouped by the individual network asset instances.


## What to do next

Create an IP Address Block that uses this Managed Network. See [Create an IP Address Block record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/create-an-ip-address-block-record.md).

You can also review or update the fields, create a related tab record, or delete a record. For more information, see [Update or delete a record of an inventory number allocation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/update_and_delete_ip_address_space.md).

**Parent Topic:**[Manage IP addresses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/manage-ip-addresses.md)

**Related topics**  


[Create an IP Address Block record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/create-an-ip-address-block-record.md)

[Managed Network and IP address allocation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/managed-network-and-ip-address-allocation.md)

