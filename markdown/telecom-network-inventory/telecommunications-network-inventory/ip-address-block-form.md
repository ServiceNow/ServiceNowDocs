---
title: IP Address Block form
description: The IP Address Block form defines a top-level IP address range using CIDR notation. Use this reference to understand the available fields and their behavior.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/ip-address-block-form.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2026-08-17"
reading_time_minutes: 2
breadcrumb: [Reference, Telecommunications Network Inventory]
---

# IP Address Block form

The IP Address Block form defines a top-level IP address range using CIDR notation. Use this reference to understand the available fields and their behavior.

## IP Address Block form fields

<table id="ip-address-block-form-fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

User-friendly name for the IP Address Block.

</td></tr><tr><td>

CIDR

</td><td>

The Classless Inter-Domain Routing \(CIDR\) notation that defines the address range of this block. Supports IPv4 prefixes /0 to /32 and IPv6 prefixes /0 to /128.

</td></tr><tr><td>

Managed Network

</td><td>

The Managed Network this block belongs to. If set, the value propagates to all subnetworks beneath this block and cannot be changed at a lower level. For more information, see [Managed Network form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/managed_network_form.md).

</td></tr><tr><td>

Description

</td><td>

Free-text description.

</td></tr><tr><td>

Life Cycle Stage

</td><td>

The current lifecycle stage of the block. This field is automatically set to **Operational**.

</td></tr><tr><td>

Life Cycle Stage Status

</td><td>

The current lifecycle stage status. This field is automatically set to **In Use**. **Note:** The block is active when Life Cycle Stage is Operational and when Life Cycle Stage Status is In Use.

</td></tr><tr><td>

Reported Addresses In Use

</td><td>

The count of addresses currently in use under this block.

</td></tr><tr><td>

Reported Free Addresses

</td><td>

The count of addresses available for use under this block.

</td></tr><tr><td>

Reported Reserved Addresses

</td><td>

The count of addresses flagged as reserved under this block.

</td></tr></tbody>
</table>**Parent Topic:**[Telecommunications Network Inventory reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/telecommunications-network-inventory-reference.md)

**Related topics**  


[Create an IP Address Block record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-an-ip-address-block-record.md)

[CIDR validation rules for IP Address Blocks and IP Subnetworks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/cidr-validation-rules.md)

[Hierarchy rules for IP Subnetworks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/hierarchy-rules-for-ip-subnetworks.md)

[Managed Network and IP address allocation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/managed-network-and-ip-address-allocation.md)

[Inventory number allocation fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/inventory-number-allocation-fields.md)

