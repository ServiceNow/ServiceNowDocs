---
title: Bulk allocation limits for allocated IP addresses
description: When you trigger bulk creation of allocated IP records from an IP Subnetwork, the system applies size limits and reserved-address rules before generating the records. This topic describes those limits and the messages displayed when they apply.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/bulk-allocation-limits-for-allocated-ip-addresses.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2026-06-25"
reading_time_minutes: 1
breadcrumb: [Reference, Telecommunications Network Inventory]
---

# Bulk allocation limits for allocated IP addresses

When you trigger bulk creation of allocated IP records from an IP Subnetwork, the system applies size limits and reserved-address rules before generating the records. This topic describes those limits and the messages displayed when they apply.

## Maximum allocation size

A single bulk allocation operation creates at most 64 allocated IP records. The minimum prefix length supported for bulk allocation is therefore /26 for IPv4 and /122 for IPv6 — both equate to 64 addresses.

Attempting bulk allocation on a subnetwork with a shorter \(less specific\) prefix is rejected with the following error:

```
Subnetwork {CIDR} contains {N} addresses, which exceeds the maximum of 64 ({/26 or /122}) permitted for bulk IP Address generation. Please subdivide into smaller subnetworks before generating allocated IPs.
```

The \{/26 or /122\} placeholder is replaced with /26 for IPv4 subnetworks and /122 for IPv6 subnetworks.

## Reserved addresses generated during allocation

Bulk allocation creates one record per address in the subnetwork’s CIDR. Addresses that are structurally unassignable are flagged automatically with Is Reserved = True on the resulting allocated IP records. The rule depends on the protocol and prefix.

IPv4 subnetworks:

|Prefix range|Addresses reserved|Notes|
|------------|------------------|-----|
|/26 – /30|First address \(network\) and last address \(broadcast\)|Standard IPv4 convention|
|/31|None|Both addresses usable \(RFC 3021 — point-to-point links\)|
|/32|None|Single-host network|

IPv6 subnetworks:

|Prefix range|Addresses reserved|Notes|
|------------|------------------|-----|
|/122 – /127|First address only \(Subnet Router Any cast\)|RFC 4291. IPv6 has no broadcast address.|
|/128|None|Single-address network|

**Parent Topic:**[Telecommunications Network Inventory reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/telecommunications-network-inventory-reference.md)

**Related topics**  


[Allocate IP address slots in a subnetwork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/allocate-ip-address-slots-in-a-subnetwork.md)

[Allocated IP Address form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/allocated-ip-address-form.md)

