---
title: Manage IP addresses
description: Manage IP address allocation in the application by creating IP Address Blocks, IP Subnetworks, allocated IP addresses, and IP Address records, expressed in Classless Inter-Domain Routing \(CIDR\) notation. Both IPv4 and IPv6 are supported.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/telecom-network-inventory/telecommunications-network-inventory/manage-ip-addresses.html
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-08-17"
reading_time_minutes: 2
breadcrumb: [Inventory number allocation, Defining inventory records, Use, Telecommunications Network Inventory]
---

# Manage IP addresses

Manage IP address allocation in the application by creating IP Address Blocks, IP Subnetworks, allocated IP addresses, and IP Address records, expressed in Classless Inter-Domain Routing \(CIDR\) notation. Both IPv4 and IPv6 are supported.

IP address management involves creating top-level IP Address Blocks and subdividing them into IP Subnetworks with optional nesting. Follow the procedures in this section to allocate IP address slots and create IP Address records.

-   **[Create an IP Address Block record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/create-an-ip-address-block-record.md)**  
Create an IP Address Block record to define a top-level IP address range, expressed in Classless Inter-Domain Routing \(CIDR\) notation. The block becomes the parent for one or more IP Subnetworks. Supports both IPv4 and IPv6.
-   **[Create an IP Subnetwork Record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown)**  
Create an IP Subnetwork record to subdivide an IP Address Block or to nest a subnetwork within an existing IP Subnetwork. The subnetwork's CIDR must fall within its parent's range. Supports both IPv4 and IPv6.
-   **[Allocate IP Address Slots in a subnetwork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/allocate-ip-address-slots-in-a-subnetwork.md)**  
Allocate IP address slots in bulk from an IP Subnetwork. The system creates one allocated IP record for each address in the subnetwork's CIDR. Reserved addresses \(the first and last for IPv4, or the first for IPv6\) are flagged automatically and cannot be promoted to IP Address records.
-   **[Create IP Address Records from allocated IPs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/create-ip-address-records-from-allocated-ips.md)**  
Create one or more IP Address records by selecting allocated IP slots and promoting them to active CMDB Configuration Items.
-   **[Create an IP Address Record at subnet level](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/create-an-ip-address-record-at-subnet-level.md)**  
Create a single IP Address record that represents an entire IP Subnetwork as one Configuration Item. The IP Address record uses the subnetwork’s CIDR as its value, rather than a single host address. This method is used when the subnetwork is bound to a service, port, customer, or interface as a single entity.
-   **[Create a Managed Network](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/create_managed_network.md)**  
Create a Managed Network record to define a network scope that can be assigned to IP Address Blocks. A Managed Network value propagates to subnetworks and allocated IP records beneath the IP Address Block, and the same CIDR can exist in different Managed Networks without conflict.

**Parent Topic:**[Inventory number allocation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/vlan_or_lag_number_management.md)

**Related topics**  


[IP address management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/ip-address-management.md)

[Exploring IP addresses allocation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/exploring-ip-addresses-allocation.md)

