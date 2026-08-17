---
title: Create an IP Subnetwork record
description: Create an IP Subnetwork record to subdivide an IP Address Block or to nest a subnetwork within an existing IP Subnetwork. The subnetwork's CIDR must fall within its parent's range. This task supports both IPv4 and IPv6.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/create-an-ip-subnetwork-record.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 7
breadcrumb: [Manage IP addresses, Inventory number allocation, Define inventory records, Use, Telecommunications Network Inventory]
---

# Create an IP Subnetwork record

Create an IP Subnetwork record to subdivide an IP Address Block or to nest a subnetwork within an existing IP Subnetwork. The subnetwork's CIDR must fall within its parent's range. This task supports both IPv4 and IPv6.

## Before you begin

Install all required [Modeling your workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/telecommunications-network-inventory-workflow.md) plugins.

The parent IP Address Block or IP Subnetwork must be in an active state \(Life Cycle Stage = Operational and Life Cycle Stage Status = In Use\).

Role required: `core.dc_ops_agent, sn_ni_core.inventory_agent`

## About this task

When you create an IP Subnetwork record, the system creates a corresponding configuration item \(CI\) record in the IP Network Subnet \(`cmdb_ci_ip_network_subnet`\) table.

An IP Subnetwork can itself contain further nested IP Subnetworks. The nesting depth is not limited. To create a nested subnetwork, start from the parent IP Subnetwork record instead of the IP Address Block.

The IP Subnetwork label in the user interface refers to the Managed IP Network Subnet class in the underlying data model.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace** or **Service Operations Workspace**.

2.  Open the parent record under which you want to create the subnetwork:

    -   To create a top-level subnetwork, open an IP Address Block record by navigating to **Inventory Number Allocation** &gt; **IP Address Block**and select the block.
    -   To create a nested subnetwork, open an IP Subnetwork record by navigating to **Inventory Number Allocation** &gt; **IP Network Subnets** and select the subnetwork.
3.  Select the **IP Subnetwork** tab \(for top-level subnetworks\) or the **Nested IP Subnet** tab \(for nested subnetworks\).

4.  Select **Create IP Subnetwork**.

5.  On the Create Nested IP Subnetwork form, fill in the fields.

<table id="create-nested-ip-subnetwork-fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Nested Pool Name

</td><td>

Name for this subnetwork.

</td></tr><tr><td>

CIDR

</td><td>

The subnetwork's address range in CIDR notation. The CIDR must be a more-specific range within the parent's CIDR. The system validates the CIDR on save. For more information, see [CIDR validation rules for IP Address Blocks and IP Subnetworks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/cidr-validation-rules.md).

</td></tr><tr><td>

Managed Network

</td><td>

Network inherited from the parent. If the parent has a Managed Network set, this field is read-only and pre-populated with the parent's value. If the parent has no Managed Network, this field is editable. For more information, see [Managed Network form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/managed_network_form.md).

</td></tr><tr><td>

Parent Pool

</td><td>

The parent record.

</td></tr><tr><td>

DNS Domain

</td><td>

DNS domain for this subnetwork.

</td></tr><tr><td>

Description

</td><td>

Description of the subnetwork.

</td></tr><tr><td>

Life cycle stage

</td><td>

Current lifecycle stage. This field is automatically set to **Operational**.

</td></tr><tr><td>

Life Cycle Stage Status

</td><td>

Current lifecycle status. This field is automatically set to **In Use**. **Note:** The subnetwork must be **Operational** and **In Use** to support nested subnetworks and IP allocations.

</td></tr></tbody>
</table>6.  Select **Submit**.

    If the CIDR fails validation, an inline error message is displayed. Common rejections include the CIDR falling outside the parent's range, the CIDR being identical to the parent, and the CIDR duplicating another subnetwork under the same parent. For more information about the validation rules, see [CIDR validation rules for IP Address Blocks and IP Subnetworks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/cidr-validation-rules.md).

    After successful submission, the system navigates to the new IP Subnetwork record.

7.  Create the [Modeling your workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/telecommunications-network-inventory-workflow.md) attributes for this IP Subnetwork by selecting **Set Inventory Attributes**.

    When you select **Set Inventory Attributes**, the system creates a TNI CI Attributes record. The record is added to the CI table and the [Modeling your workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/telecommunications-network-inventory-workflow.md) CI Attributes tables, and linked to the CI record.

    **Note:** If you select Save without selecting **Set Inventory Attributes** the system creates a CI record but not a [Modeling your workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/telecommunications-network-inventory-workflow.md) CI record. In the Network Inventory Workspace, Set Inventory Attributes is visible only for [Modeling your workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/telecommunications-network-inventory-workflow.md) roles. In the TNI CI attributes form, the name is fetched from the Name field by default, and the Inventory Category is set as IP Address.

8.  Add packs to this service by selecting **Add Packs**.

9.  Add attachments such as graphics or documents by selecting the attachment icon.

10. View the hierarchy of records under this subnetwork by selecting the **Dependency View** option.

11. View the related network inventories by selecting the brick icon.

    The Infrastructure Relationships section shows all the related network inventories grouped by the individual network instance.


## What to do next

-   To allocate IP address slots in bulk, see [Allocate IP address slots in a subnetwork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/allocate-ip-address-slots-in-a-subnetwork.md).
-   To create IP Address records for selected slots after allocation, see [Create an IP Address record from allocated IPs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-ip-address-records-from-allocated-ips.md).
-   To create a single IP Address record at the subnetwork level, see [Create an IP Address record at subnet level](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-an-ip-address-record-at-subnet-level.md) .

You can also review or update the fields, create a related tab record, or delete a record. For more information, see [Update or delete a record of an inventory number allocation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/update_and_delete_ip_address_space.md).

**Parent Topic:**[Manage IP addresses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/manage-ip-addresses.md)

**Related topics**  


[Allocate IP address slots in a subnetwork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/allocate-ip-address-slots-in-a-subnetwork.md)

[Create an IP Address record from allocated IPs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-ip-address-records-from-allocated-ips.md)

[Create an IP Address record at subnet level](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-an-ip-address-record-at-subnet-level.md)

[CIDR validation rules for IP Address Blocks and IP Subnetworks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/cidr-validation-rules.md)

[Hierarchy rules for IP Subnetworks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/hierarchy-rules-for-ip-subnetworks.md)

[IP Subnetwork form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/ip-subnetwork-form.md)

