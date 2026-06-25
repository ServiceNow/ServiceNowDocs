---
title: Managed Network and IP address allocation
description: A Managed Network record defines a network scope that can be assigned to an IP Address Block. When assigned, the Managed Network propagates to every IP Subnetwork beneath that block. It also propagates to every allocated IP record beneath those subnetworks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/managed-network-and-ip-address-allocation.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-06-25"
reading_time_minutes: 1
breadcrumb: [IP address management, Inventory number allocation, Explore, Telecommunications Network Inventory]
---

# Managed Network and IP address allocation

A Managed Network record defines a network scope that can be assigned to an IP Address Block. When assigned, the Managed Network propagates to every IP Subnetwork beneath that block. It also propagates to every allocated IP record beneath those subnetworks.

## Propagation behavior

The propagation behavior is as follows:

-   When you create an IP Subnetwork beneath an IP Address Block, the Managed Network field behaves differently if the parent block has a Managed Network assigned. In that case, the subnetwork's Managed Network field is pre-populated with the parent's value and is read-only. The subnetwork cannot be assigned to a different Managed Network.
-   When you create an IP Subnetwork beneath an IP Address Block that has no Managed Network assigned, the subnetwork's Managed Network field is editable. You can leave it empty or assign it to any Managed Network. Your choice then propagates down to any nested subnetworks beneath this subnetwork.

## Uniqueness scope

The Managed Network value defines the scope within which an IP Address Block’s CIDR must be unique. The same CIDR may exist in different Managed Networks. To learn more, see [CIDR validation rules for IP Address Blocks and IP Subnetworks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/cidr-validation-rules.md).

**Related topics**  


[Create Managed Network](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create_managed_network.md)

[Create an IP Address Block record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-an-ip-address-block-record.md)

[CIDR validation rules for IP Address Blocks and IP Subnetworks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/cidr-validation-rules.md)

