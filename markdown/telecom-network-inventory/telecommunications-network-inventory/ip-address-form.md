---
title: IP Address form
description: The IP Address form is the active CMDB record for an IP address, created from an allocated IP slot or at the subnetwork level.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/ip-address-form.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2026-07-28"
reading_time_minutes: 1
breadcrumb: [Reference, Telecommunications Network Inventory]
---

# IP Address form

The IP Address form is the active CMDB record for an IP address, created from an allocated IP slot or at the subnetwork level.

## IP Address form fields

|Field|Description|
|-----|-----------|
|IP Address|The address value. For records created using the From allocated IPs method, this is the host address \(for example, 10.0.0.1\). For records created using the At subnet level method, this is the subnetwork’s full CIDR \(for example, 10.0.0.0/26\).|
|IP version|Either IPv4 or IPv6.|
|Owned By Configuration Item|Reference to the CI that owns this address.|
|Netmask|The subnet mask for this address.|

**Parent Topic:**[Telecommunications Network Inventory reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/telecommunications-network-inventory-reference.md)

**Related topics**  


[Create IP Address records from allocated IPs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-ip-address-records-from-allocated-ips.md)

[Create an IP Address record at subnet level](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-an-ip-address-record-at-subnet-level.md)

[CMDB relationships for IP address records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/cmdb-relationships-for-ip-address-records.md)

