---
title: IP address inventory management data model
description: By using the IP address inventory management data model, you can understand how the tables that are used for the IP pools, IP subnetworks, allocated IP addresses, and IP addresses all relate to each other.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Telecommunications Network Inventory]
---

# IP address inventory management data model

By using the IP address inventory management data model, you can understand how the tables that are used for the IP pools, IP subnetworks, allocated IP addresses, and IP addresses all relate to each other.

## Data model

The following diagram shows the IP address inventory management data model.

![Data model that shows how the IP pools, IP subnetworks, allocated IP addresses, and IP addresses are related.](../image/IP_datamodel.png)

With this data model, you can store the related tables of your IP pool, IP subnetwork addresses, or allocated IP addresses. You can also create an IP pool table or IP subnet table to allocate services. To do this task, you create an IP pool or IP subnet. Each IP address in the subnet is created in an allocated IP address table. You can then relate IP addresses from the allocated IP address table to the IP address table for discovery and configuration item \(CI\) mapping.

An IP address is allocated this way:

1.  A telco operator gets an IP subnet that has been allocated from the external system for their customers. This IP subnet is stored in an IP network subnet table.
2.  A telco operator can create an IP address of the subnet so that they can track the IP address allocation. In this case, each IP address of this subnet gets stored in the allocated IP address table.

3.  The IP addresses that are ready to use in the allocated IP address table are then related to a record in the IP address table.

**Parent Topic:**[Telecommunications Network Inventory reference](../concept/telecommunications-network-inventory-reference.md)

**Related topics**  


[Create IP address allocation](../concept/ip_pool_ip_network_subnet_allocated_ip_address_and_ip_address.md)

[IP addresses allocation](../concept/ip_address_management.md)

