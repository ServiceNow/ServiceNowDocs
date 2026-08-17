---
title: IP Subnetwork form
description: The IP Subnetwork form defines a subdivision of an IP Address Block or a nested subdivision of another IP Subnetwork.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/ip-subnetwork-form.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2026-08-17"
reading_time_minutes: 2
breadcrumb: [Reference, Telecommunications Network Inventory]
---

# IP Subnetwork form

The IP Subnetwork form defines a subdivision of an IP Address Block or a nested subdivision of another IP Subnetwork.

## IP Subnetwork form fields

<table id="ip-subnetwork-form-fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \(Nested Pool Name on creation\)

</td><td>

User-friendly name for the IP Subnetwork.

</td></tr><tr><td>

CIDR

</td><td>

The CIDR notation that defines the address range of this subnetwork. The value Must fall within the parent's range, must be more specific \(longer prefix\) than the parent'hs, and must not duplicate any sibling under the same parent. For more information about CIDR validation, see [CIDR validation rules for IP Address Blocks and IP Subnetworks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/cidr-validation-rules.md).

</td></tr><tr><td>

Managed Network

</td><td>

The Managed Network that this subnetwork belongs to. This field is read-only and pre-populated when the parent has a Managed Network set. This field is editable when the parent has none. Cannot differ from the parent’s value.

</td></tr><tr><td>

Parent Pool

</td><td>

The parent IP Address Block or IP Subnetwork. This field is read-only after creation.

</td></tr><tr><td>

DNS Domain

</td><td>

The DNS domain associated with this subnetwork.

</td></tr><tr><td>

Description

</td><td>

Free-text description.

</td></tr><tr><td>

Life Cycle Stage

</td><td>

The current life-cycle stage of the subnetwork. This field is automatically set to **Operational**.

</td></tr><tr><td>

Life Cycle Stage Status

</td><td>

The current life-cycle stage status. This field is automatically set to **In Use****Note:** The subnetwork is active when Life Cycle Stage is Operational, and when the Life Cycle Stage Status is In Use.

</td></tr><tr><td>

Reported Addresses In Use

</td><td>

The count of addresses currently in use under this subnetwork.

</td></tr><tr><td>

Reported Free Addresses

</td><td>

The count of addresses available for use under this subnetwork.

</td></tr><tr><td>

Reported Reserved Addresses

</td><td>

The count of addresses flagged as reserved under this subnetwork.

</td></tr></tbody>
</table>**Parent Topic:**[Telecommunications Network Inventory reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/telecommunications-network-inventory-reference.md)

**Related topics**  


[Create an IP Subnetwork record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-an-ip-subnetwork-record.md)

[CIDR validation rules for IP Address Blocks and IP Subnetworks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/cidr-validation-rules.md)

[Hierarchy rules for IP Subnetworks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/hierarchy-rules-for-ip-subnetworks.md)

[Managed Network and IP address allocation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/managed-network-and-ip-address-allocation.md)

[Inventory number allocation fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/inventory-number-allocation-fields.md)

