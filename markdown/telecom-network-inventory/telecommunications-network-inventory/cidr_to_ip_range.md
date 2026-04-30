---
title: CIDR to IP range function
description: Classless Inter-Domain Range \(CIDR\) to IP range flow action enables you to create a set of IP addresses using the Classless Inter-Domain Range \(CIDR\) using Telecommunications Network Inventory application based on the input that you receive when you instantiate an inventory.
locale: en-US
release: xanadu
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Telecommunications Network Inventory function catalog, Telecommunications Network Inventory reference, Telecommunications Network Inventory]
---

# CIDR to IP range function

Classless Inter-Domain Range \(CIDR\) to IP range flow action enables you to create a set of IP addresses using the Classless Inter-Domain Range \(CIDR\) using Telecommunications Network Inventory application based on the input that you receive when you instantiate an inventory.

Upon calling this flow action, a CIDR is fetched using the given IP subnetwork. Further, using the CIDR a set of IP addresses are created. These IP addresses are further stored in the allocated IP addresses table.

This function also ensures that there is no other allocated IP address created for this particular IP subnetwork.

## Roles and availability

Users with the admin role can add an action to a flow and define the configuration details of the flow. This function is available as a Flow Designer action in the Telecommunications Network Inventory application so that you can perform inventory-related data operations.

## Input fields

|Field name|Description|Data type|
|----------|-----------|---------|
|Change Task|Provide change task number for this task|Reference|
|IP Subnetwork|Provide name of the subnetwork from where the CIDR must be fetched|String|

## Output

The following table lists the information about the function output.

|Name|Description|Data type|
|----|-----------|---------|
|Allocated IP address|Returns a glide a record|Record|

**Parent Topic:**[Telecommunications Network Inventory function catalog](tni-flow-action.md)

**Related topics**  


[Allocate Free Number function](allocate-free-number-action.md)

[Create CI From Template function](add-card-action.md)

[Cascade Update function](cascade-update-action.md)

[Create and Assign Range/Single Number function](create-assign-range-single-number-function.md)

[Create Logical Interface function](create-logical-interface-action.md)

[Create Logical Connection function](create-logical-connection-action.md)

[Create Physical Connection function](create-physical-connection-action.md)

[Create IP subnetwork function](create_ip_subnetwork.md)

[Get Interface Summary function](get-interface-summary-action.md)

[Lookup Next Hub function](lookup-next-hub-action.md)

[Path Search function](path-compute-action.md)

