---
title: Allocated IP Address form
description: The Allocated IP Address form represents a single address slot within an IP Subnetwork. The fields on this form are listed below.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/allocated-ip-address-form.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2026-06-25"
reading_time_minutes: 1
breadcrumb: [Reference, Telecommunications Network Inventory]
---

# Allocated IP Address form

The Allocated IP Address form represents a single address slot within an IP Subnetwork. The fields on this form are listed below.

|Field|Description|
|-----|-----------|
|Name|The address value \(matches the IP Address field\).|
|IP Address|The address value.|
|Is Reserved|Set automatically. True for addresses that are structurally unassignable \(the first and last addresses of an IPv4 subnet, the first address of an IPv6 subnet\). Records with Is Reserved set to True can't be promoted to IP Address records.|
|Is Managed|Set automatically by the system. Flips to True when an IP Address record is created from this slot using the From allocated IPs method. Flips back to False when the IP Address record is deleted. Not user-editable.|
|Managed Network|The Managed Network value inherited from the parent subnetwork. Read-only.|

**Parent Topic:**[Telecommunications Network Inventory reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/telecommunications-network-inventory-reference.md)

**Related topics**  


[Allocate IP address slots in a subnetwork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/allocate-ip-address-slots-in-a-subnetwork.md)

[Bulk allocation limits for allocated IP addresses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/bulk-allocation-limits-for-allocated-ip-addresses.md)

[Create IP Address records from allocated IPs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-ip-address-records-from-allocated-ips.md)

