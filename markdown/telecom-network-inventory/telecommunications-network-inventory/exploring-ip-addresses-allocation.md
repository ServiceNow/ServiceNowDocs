---
title: IP addresses allocation
description: Using the IP address allocation feature, you can create, review, and update IP Address Blocks and IP Subnetworks. You can also manage allocated IP addresses and IP addresses expressed in Classless Inter-Domain Routing \(CIDR\) notation. Both IPv4 and IPv6 are supported.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/exploring-ip-addresses-allocation.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-06-25"
reading_time_minutes: 5
breadcrumb: [IP address management, Inventory number allocation, Explore, Telecommunications Network Inventory]
---

# IP addresses allocation

Using the IP address allocation feature, you can create, review, and update IP Address Blocks and IP Subnetworks. You can also manage allocated IP addresses and IP addresses expressed in Classless Inter-Domain Routing \(CIDR\) notation. Both IPv4 and IPv6 are supported.

## IP address tables

-   IP Address Block: An IP Address Block is a top-level range of IP addresses expressed as a CIDR. The user interface label IP Address Block refers to the underlying Managed IP Pool class.
-   IP Subnetwork: An IP Subnetwork is an operational subdivision of an IP Address Block. An IP Subnetwork can itself contain further nested IP Subnetworks, allowing IP address space to be subdivided to any depth.
-   Allocated IP address: An allocated IP address represents a single address slot within an IP Subnetwork's CIDR. Allocated IP address records carry two flags. Is Reserved is set automatically for structurally unassignable addresses. Is Managed is set automatically when an IP Address record is created from this slot.
-   IP address: An IP address record is the active CMDB record for an address. It can represent a single host address within a subnetwork, created from an allocated IP. Alternatively, it can represent the entire subnetwork by using the subnetwork's CIDR as its value.
-   Managed Network: A Managed Network defines a network scope within which an IP Address Block's CIDR must be unique. The same CIDR may exist in different Managed Networks without conflict. The Managed Network assigned to an IP Address Block propagates down to its IP Subnetworks and cannot be changed at a lower level. To learn more, see [Create Managed Network](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create_managed_network.md).

## IP allocation methods

An IP Subnetwork uses one of two methods to create IP address records. The two methods are mutually exclusive: A subnetwork may use one or the other, but never both at the same time.

-   **From allocated IPs:** The user selects one or more allocated IP records on a subnetwork and creates a corresponding IP address record for each selected slot. Each new IP address record uses the host address as its value. This method is appropriate when individual addresses are being assigned to devices, interfaces, or services.
-   **At subnet level:** A single IP address record is created for the subnetwork as a whole. The IP address record uses the subnetwork's CIDR as its value, rather than a single host address. This method is appropriate when the subnetwork is bound to a service, port, customer, or interface.

Once the first IP address record is created on a subnetwork by either method, the other method is locked for that subnetwork. To switch methods, delete the existing IP address records. The underlying allocated IP slots are preserved across deletion.

## Active state required for operations

A record must be in an active state before child records or IP allocations can be created against it. A record is active when the Life Cycle Stage is Operational and the Life Cycle Stage Status is In Use. Any other combination of values prevents the creation of subnetworks beneath the record or the allocation of addresses from it.

## Reserved addresses

When allocated IP records are generated for a subnetwork, addresses that are structurally unassignable are flagged automatically with Is Reserved = True. The rule differs by protocol. For IPv4, the first address \(the network address\) and the last address \(the broadcast address\) are reserved. A /31 IPv4 subnet reserves no addresses \(RFC 3021\); a /32 IPv4 subnet reserves no addresses. For IPv6, only the first address — the Subnet Router Anycast address \(RFC 4291\) — is reserved. IPv6 has no broadcast address. A /128 IPv6 subnet reserves no addresses.

## CMDB relationships

Every IP Address record participates in standard ServiceNow CMDB relationships. The relationships created depend on the method used. When IP Address records are created from selected Allocated IPs, the system writes two relationships per record. The first is an IP Address Manages Allocated IP relationship, linking the new record to its source slot. The second is an IP Subnetwork Contains IP Address relationship, linking it to the subnetwork. When a single IP Address record is created at the subnetwork level, only the IP Subnetwork Contains IP Address relationship is created.

Both relationship types are visible on each IP Address record’s Related Items panel and in the Dependency View.

**Related topics**  


[Create an IP Address Block record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-an-ip-address-block-record.md)

[Create an IP Subnetwork record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-an-ip-subnetwork-record.md)

[Allocate IP address slots in a subnetwork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/allocate-ip-address-slots-in-a-subnetwork.md)

[Create IP Address records from allocated IPs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-ip-address-records-from-allocated-ips.md)

[Create an IP Address record at subnet level](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-an-ip-address-record-at-subnet-level.md)

[Create Managed Network](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create_managed_network.md)

