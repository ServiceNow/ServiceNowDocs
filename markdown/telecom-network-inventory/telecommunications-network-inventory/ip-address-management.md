---
title: IP address management
description: IP address management in the Telecommunications Network Inventory application lets you create, review, and update IP Address Blocks, IP Subnetworks, allocated IP addresses, and IP addresses, expressed in Classless Inter-Domain Routing \(CIDR\) notation. Both IPv4 and IPv6 are supported.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/ip-address-management.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-06-25"
reading_time_minutes: 1
breadcrumb: [Inventory number allocation, Explore, Telecommunications Network Inventory]
---

# IP address management

IP address management in the Telecommunications Network Inventory application lets you create, review, and update IP Address Blocks, IP Subnetworks, allocated IP addresses, and IP addresses, expressed in Classless Inter-Domain Routing \(CIDR\) notation. Both IPv4 and IPv6 are supported.

## IP address management overview

An IP Subnetwork can itself contain further nested IP Subnetworks, allowing IP address space to be subdivided to any depth. A Managed Network defines a network scope within which an IP Address Block’s CIDR must be unique; the same CIDR may exist in different Managed Networks without conflict.

The topics in this section explain the conceptual model of IP address management, the propagation rules that govern how Managed Network values flow through the hierarchy, the CMDB relationships that the system writes automatically, and the data model that ties IP Address Blocks, IP Subnetworks, allocated IP addresses, and IP addresses together.

**Related topics**  


[IP addresses allocation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/exploring-ip-addresses-allocation.md)

[Managed Network and IP address allocation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/managed-network-and-ip-address-allocation.md)

[CMDB relationships for IP address records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/cmdb-relationships-for-ip-address-records.md)

[IP address inventory management data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/ip-address-inventory-management-data-model.md)

