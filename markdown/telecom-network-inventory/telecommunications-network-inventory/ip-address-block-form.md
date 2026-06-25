---
title: IP Address Block form
description: The IP Address Block form defines a top-level IP address range using CIDR notation. The fields on this form are listed below.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/ip-address-block-form.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2026-06-25"
reading_time_minutes: 2
breadcrumb: [Reference, Telecommunications Network Inventory]
---

# IP Address Block form

The IP Address Block form defines a top-level IP address range using CIDR notation. The fields on this form are listed below.

|Field|Description|
|-----|-----------|
|Name|User-friendly name for the IP Address Block.|
|CIDR|The Classless Inter-Domain Routing \(CIDR\) notation that defines the address range of this block. Supports IPv4 prefixes /0 to /32 and IPv6 prefixes /0 to /128.|
|Managed Network|The Managed Network this block belongs to. Optional. If set, the value propagates to all subnetworks beneath this block and cannot be changed at a lower level. To learn more, see [Managed Network form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/managed_network_form.md).|
|Description|Free-text description. Optional.|
|Life Cycle Stage|The current lifecycle stage of the block. Default value: Operational. Used together with Life Cycle Stage Status to determine if the block is active.|
|Life Cycle Stage Status|The current lifecycle stage status. Default value: In Use. The block is active when Life Cycle Stage is Operational and Life Cycle Stage Status is In Use.|
|Reported Addresses In Use|The count of addresses currently in use under this block.|
|Reported Free Addresses|The count of addresses available for use under this block.|
|Reported Reserved Addresses|The count of addresses flagged as reserved under this block.|

**Parent Topic:**[Telecommunications Network Inventory reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/telecommunications-network-inventory-reference.md)

**Related topics**  


[Create an IP Address Block record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-an-ip-address-block-record.md)

[CIDR validation rules for IP Address Blocks and IP Subnetworks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/cidr-validation-rules.md)

[Hierarchy rules for IP Subnetworks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/hierarchy-rules-for-ip-subnetworks.md)

[Managed Network and IP address allocation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/managed-network-and-ip-address-allocation.md)

[Inventory number allocation fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/inventory-number-allocation-fields.md)

