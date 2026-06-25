---
title: IP address inventory management data model
description: By using the IP address inventory management data model, you can understand how the tables used for IP Address Blocks, IP Subnetworks, allocated IP addresses, and IP addresses relate to each other. The data model supports both IPv4 and IPv6, and supports nesting subnetworks to any depth within a parent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/ip-address-inventory-management-data-model.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-06-25"
reading_time_minutes: 2
breadcrumb: [IP address management, Inventory number allocation, Explore, Telecommunications Network Inventory]
---

# IP address inventory management data model

By using the IP address inventory management data model, you can understand how the tables used for IP Address Blocks, IP Subnetworks, allocated IP addresses, and IP addresses relate to each other. The data model supports both IPv4 and IPv6, and supports nesting subnetworks to any depth within a parent.

## Data model

The data model defines four record types in a parent-child hierarchy:

-   **IP Address Block** \(class: Managed IP Pool\) — top-level record representing a routable address range.
-   **IP Subnetwork** \(class: Managed IP Network Subnet\) — operational subdivision of an IP Address Block. An IP Subnetwork can contain further nested IP Subnetworks recursively.
-   **Allocated IP Address** — one record per address slot within an IP Subnetwork’s CIDR.
-   **IP Address** — the active CMDB Configuration Item for an address. Created from an allocated IP slot or from a subnetwork as a whole.

## How IP addresses are allocated

The allocation flow depends on whether individual host addresses are tracked or the subnetwork is bound as a single entity.

Per-host tracking \(from allocated IPs\):

1.  Define the IP Address Block representing the routable range.
2.  Create one or more IP Subnetworks within the block.
3.  Generate allocated IP records for a subnetwork \(one per address in its CIDR\).
4.  Create IP Address records from selected allocated IPs as individual hosts are assigned.

Subnetwork-level binding \(at subnet level\):

1.  Define the IP Address Block representing the routable range.
2.  Create one or more IP Subnetworks within the block.
3.  Create a single IP Address record representing the subnetwork as a whole. The IP Address record’s value is the subnetwork’s CIDR.

The two methods are mutually exclusive within a subnetwork. To learn more about the methods and the relationships they create, see [CMDB relationships for IP address records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/cmdb-relationships-for-ip-address-records.md)

**Related topics**  


[CMDB relationships for IP address records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/cmdb-relationships-for-ip-address-records.md)

[Create an IP Address Block record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-an-ip-address-block-record.md)

[Create an IP Subnetwork record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-an-ip-subnetwork-record.md)

