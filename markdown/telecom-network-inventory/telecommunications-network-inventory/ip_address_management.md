---
title: IP addresses allocation
description: By using the IP address allocation of the Telecommunications Network Inventory application, you can create, review, and update IP pools, IP network subnets, allocated IP addresses, and Classless Inter-Domain Routing \(CIDR\).
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Inventory number allocation, Explore, Telecommunications Network Inventory]
---

# IP addresses allocation

By using the IP address allocation of the Telecommunications Network Inventory application, you can create, review, and update IP pools, IP network subnets, allocated IP addresses, and Classless Inter-Domain Routing \(CIDR\).

## IP address tables

-   **IP pool**: An IP pool is a sequential range of IP addresses that are allocated to a large network, such as the subnet mask of /16 or /24 IP addresses.
-   **IP network subnet**: An IP network subnet represents the IP address that is allocated to the customer, such as the subnet mask of /28 or /29 addresses.
-   **Allocated IP address**: An allocated IP address is a list of all individual IP addresses that are part of an IP network subnet and can be assigned to configuration Items \(CIs\). By using an allocated IP address, you can assign an IP address to a host.
-   **Managed Network**: A managed network is a list of all existing networks or new networks. By using a managed network, you can assign a network to an IP pool or to an allocated IP address. To learn more, see [Create managed network](../task/create_managed_network.md).

To learn more about how to manage IP addresses, see [IP address inventory management data model](../reference/data_model_of_ip_address_inventory_management.md).

## Use case

Let's say a company that is in need of an internet access submits an order request to their service provider. The order request generates the order line items for allocating a WAN IP address with a subnet of /30 and order tasks. To assign IP addresses, a change request is initiated. This change request initiates the following change tasks:

-   Create an IP pool record for the subnet mask of /30 IP addresses according to the design guidelines. For more information, see [Create an IP pool record](../task/define-ip-pool.md).
-   Create an IP network subnet for the subnet mask of /30 IP addresses and four individual IP addresses. For more information, see [Create an IP network subnet record](../task/define-ip-network-subnet.md) and [IP addresses](../task/define-ip-addresses.md).
-   Create an application service.
-   Relate an IP network subnet with the change request.

**Related topics**  


[Create IP address allocation](ip_pool_ip_network_subnet_allocated_ip_address_and_ip_address.md)

