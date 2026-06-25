---
title: IP Subnetwork form
description: The IP Subnetwork form defines a subdivision of an IP Address Block or a nested subdivision of another IP Subnetwork. The fields on this form are listed below.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/ip-subnetwork-form.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2026-06-25"
reading_time_minutes: 2
breadcrumb: [Reference, Telecommunications Network Inventory]
---

# IP Subnetwork form

The IP Subnetwork form defines a subdivision of an IP Address Block or a nested subdivision of another IP Subnetwork. The fields on this form are listed below.

|Field|Description|
|-----|-----------|
|Name \(Nested Pool Name on creation\)|User-friendly name for the IP Subnetwork.|
|CIDR|The CIDR notation that defines the address range of this subnetwork. Must fall within the parent’s range, must be more specific \(longer prefix\) than the parent’s, and must not duplicate any sibling under the same parent. To learn more about CIDR validation, see[CIDR validation rules for IP Address Blocks and IP Subnetworks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/cidr-validation-rules.md) .|
|Managed Network|The Managed Network this subnetwork belongs to. Read-only and pre-populated when the parent has a Managed Network set; editable when the parent has none. Can't differ from the parent’s value.|
|Parent Pool|The parent IP Address Block or IP Subnetwork. Read-only after creation.|
|DNS Domain|The DNS domain associated with this subnetwork. Optional.|
|Description|Free-text description. Optional.|
|Life Cycle Stage|The current life-cycle stage of the subnetwork. Default value: Operational.|
|Life Cycle Stage Status|The current life-cycle stage status. Default value: In Use. The sub network is active when Life Cycle Stage is Operational and Life Cycle Stage Status is In Use.|
|Reported Addresses In Use|The count of addresses currently in use under this subnetwork.|
|Reported Free Addresses|The count of addresses available for use under this subnetwork.|
|Reported Reserved Addresses|The count of addresses flagged as reserved under this subnetwork.|

**Parent Topic:**[Telecommunications Network Inventory reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/telecommunications-network-inventory-reference.md)

**Related topics**  


[Create an IP Subnetwork record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-an-ip-subnetwork-record.md)

[CIDR validation rules for IP Address Blocks and IP Subnetworks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/cidr-validation-rules.md)

[Hierarchy rules for IP Subnetworks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/hierarchy-rules-for-ip-subnetworks.md)

[Managed Network and IP address allocation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/managed-network-and-ip-address-allocation.md)

[Inventory number allocation fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/inventory-number-allocation-fields.md)

