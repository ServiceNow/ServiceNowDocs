---
title: Create an IP Address Block record
description: Create an IP Address Block record to define a top-level IP address range, expressed in Classless Inter-Domain Routing \(CIDR\) notation. The block becomes the parent for one or more IP Subnetworks. Supports both IPv4 and IPv6.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/create-an-ip-address-block-record.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-06-25"
reading_time_minutes: 5
breadcrumb: [Manage IP addresses, Inventory number allocation, Define inventory records, Use, Telecommunications Network Inventory]
---

# Create an IP Address Block record

Create an IP Address Block record to define a top-level IP address range, expressed in Classless Inter-Domain Routing \(CIDR\) notation. The block becomes the parent for one or more IP Subnetworks. Supports both IPv4 and IPv6.

## Before you begin

Before you begin:

-   Install all required [Modeling your workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/telecommunications-network-inventory-workflow.md)
-   Role required: `sn_ni_core.inventory_agent, sn_ni_core.dc_ops_agent`

## About this task

An IP Address Block represents a routable address range that you want to subdivide and allocate. Once created, the IP Address Block becomes the parent for IP Subnetwork records.

The IP Address Block label in the user interface refers to the Managed IP Pool class in the underlying data model.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace** or **Service Operations Workspace**.

2.  Select the list icon, and then go to **Inventory Number Allocation** &gt; **IP Address Block**.

3.  Select **Create Address Block**.

4.  On the Create Address Block form, fill in the fields:

    |Field|Description|Required|
    |-----|-----------|--------|
    |Address Block Name|Name the IP Address Block.|Yes|
    |CIDR|CIDR on save is subject to validation. To learn more about the validation rules, see [CIDR validation rules for IP Address Blocks and IP Subnetworks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/cidr-validation-rules.md).|Yes|
    |Description|Free-text description of the block.|No|
    |Managed Network|The value set in the Managed Network propagates to every subnetwork beneath this block and cannot be changed at a lower level. If you leave this empty, the block is unscoped, and its child subnetworks can each set their own Managed Network. To learn more, see [Managed Network form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/managed_network_form.md) .|No|
    |Life cycle stage|The current life-cycle stage. Default: Operational.|No|
    |Life Cycle Stage Status|The current life-cycle status. Default: In Use. The block must be Operational and In Use to support child subnetworks and IP allocations.|No|

5.  Select **Submit**.

    If the CIDR fails validation, an inline error message is displayed beneath the CIDR field. Correct the CIDR and resubmit. On successful submission, the system navigates to the new IP Address Block record. The record shows three tabs: Details, IP Subnetwork, and Packs.

6.  To create attributes for this IP Address Block, select **Set Inventory Attributes**.

    When you select Set Inventory Attributes, the system creates a TNI CI Attributes record. The record is created in the CI table and in the CI Attributes tables, and linked to the CI record.

    **Note:** If you select Save without selecting Set Inventory Attributes, the system creates a CI record but not a [Modeling your workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/telecommunications-network-inventory-workflow.md) CI record. In the Network Inventory Workspace, Set Inventory Attributes is visible only for [Modeling your workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/telecommunications-network-inventory-workflow.md) roles. In the TNI CI attributes form, the name is fetched from the Name field by default, and the Inventory Category is set as IP Address.

7.  To add packs to this service, select **Add Packs**.

    To learn more about packs, see [Attribute packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/telecommunication-network-inventory-pack.md) .

8.  To add attachments such as graphics or documents, select the attachment icon in the right panel.

9.  View the hierarchy of records under this block by selecting the **Dependency View** option from the three-dot menu.

10. View the related network inventories by selecting the brick icon.

    The Infrastructure Relationships section shows all the related network inventories grouped by the individual network instance.


## What to do next

Create one or more IP Subnetworks within this IP Address Block. See [Create an IP Subnetwork record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-an-ip-subnetwork-record.md).

You can also review or update the fields, create a related tab record, or delete a record. To learn more, see [Update or delete a record of an inventory number allocation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/update_and_delete_ip_address_space.md).

**Parent Topic:**[Manage IP addresses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/manage-ip-addresses.md)

**Related topics**  


[IP address management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/ip-address-management.md)

[Managed Network and IP address allocation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/managed-network-and-ip-address-allocation.md)

[IP Address Block form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/ip-address-block-form.md)

[Create an IP Address Block record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-an-ip-address-block-record.md)

[Create Managed Network](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create_managed_network.md)

