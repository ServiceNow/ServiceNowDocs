---
title: Create IP subnetwork function
description: Created this topic as per STRY55038360 - DOC1068501
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/create\_ip\_subnetwork.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-06-25"
reading_time_minutes: 3
breadcrumb: [Function catalog, Reference, Telecommunications Network Inventory]
---

# Create IP subnetwork function

The Create IP Subnetwork function enables you to create an IP subnetwork record in the Telecommunications Network Inventory application based on the input that you receive when you instantiate an inventory.

You can use this action as a flow designer action in the Telecommunications Network Inventory workflow. Here, either CIDR or, first IP and last IP, or first IP and total host are required inputs to create a subnetwork. If the parent IP pool is provided in input, then the function validates and ensures that the subnetwork that is being created is under the provided IP pool.

## Roles and availability

Users with the admin role can add an action to a flow and define the configuration details of the flow. This function is available as a Flow Designer action in the Telecommunications Network Inventory application so that you can perform inventory-related data operations.

## Input fields

|Field name|Description|Data type|
|----------|-----------|---------|
|Parent IP pool|Provide the name of the parent IP pool to which you want to assign this subnetwork to.|String|
|CIDR|CIDR|String|
|First IP|First IP address in the series|IP Address \(Validated IPv4, IPv6\)|
|Last IP|Last IP address in the series|IP Address \(Validated IPv4, IPv6\)|
|Total Host|Number of hosts in the IP subnet|Integer|
|Managed Network|managed network of private IPs|Reference|

## Output

The following table lists the information about the function output.

|Name|Description|Data type|
|----|-----------|---------|
|IP subnetwork|Returns a glide a record|Record|

**Parent Topic:**[Telecommunications Network Inventory function catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/tni-flow-action.md)

**Related topics**  


[Allocate Free Number function]()

[Create CI From Template function]()

[Cascade Update function]()

[Create and Assign Range/Single Number function]()

[Create Logical Interface function]()

[Create Logical Connection function]()

[Create Physical Connection function]()

[CIDR to IP range function]()

[Get Interface Summary function]()

[Lookup Next Hub function]()

[Path Search function]()

