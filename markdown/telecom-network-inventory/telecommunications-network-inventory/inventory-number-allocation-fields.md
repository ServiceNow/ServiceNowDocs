---
title: Inventory number allocation fields
description: The inventory number allocation fields enables you to describe the details for LAG, VLAN, IP address, and telephone number records.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reference, Telecommunications Network Inventory]
---

# Inventory number allocation fields

The inventory number allocation fields enables you to describe the details for LAG, VLAN, IP address, and telephone number records.

<table id="table_kty_h2f_4xb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Telephone number

</td><td>

Telephone number that conforms with the e164 naming convention. For more information, see [E.164 phone number field configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_ConfigureE.164PhoneNumberFields.md).

</td></tr><tr><td>

Telephone number allocation

</td><td>

Telephone number allocation record.

</td></tr><tr><td>

Country Code

</td><td>

Select the country where you create the telephone number.

</td></tr><tr><td>

Area code

</td><td>

Code that identifies a geographic region within a country or territory. It’s usually the first three digits of a telephone number. The purpose of the area code is to route telephone calls to destinations that are based on the location of the recipient. For example, in the phone number \(123\) 456-7890, "123" represents the area code.

</td></tr><tr><td>

Central office code

</td><td>

Central office code that is also referred to as NXX. The NXX portion of a telephone number provides information about the central office or local exchange that belongs to a particular geographic area. Each central office code is related to a geographic location or service provider within the area code.For example, in the phone number \(123\) 456-7890, "456" represents the central office code.

</td></tr><tr><td>

Line number digits

</td><td>

Set of digits following the area code and central office code. These digits identifies an individual line within the area served by the central office code.For example, in the phone number \(123\) 456-7890,the set of "7890" represents the line number digits which is 4 digits long.

</td></tr><tr><td>

Status

</td><td>

Status of the telephone number:-   **New**: Indicates that this number is new.
-   **Reserved**: Indicates that the number is reserved for a service but isn't assigned yet.
-   **Unassigned**: Indicates that the number isn’t assigned to anyone yet or the number has been in a quarantined status for a few days.
-   **Assigned**: Indicates that the number is assigned.
-   **Quarantined**: Indicates that the number hasn't been in use for a long time. Depending on the network operator, this number changes to a quarantined status after a few days. After a while, the status changes to unassigned.
-   **Ported in**: Indicates that the number used to belong to some other network and has now moved to this network.
-   **Ported out**: Indicates that the number has moved out to some other network.

</td></tr><tr><td>

Number category

</td><td>

Categories:-   Owned: Indicates that these numbers are owned by your organization.
-   Third party: Indicates that these numbers are provided by a third-party organization.
-   Ported in: Indicates that these numbers are moved from another network.

</td></tr><tr><td>

Carrier

</td><td>

Name of the telecommunications company or service provider that owns and manages a range of telephone numbers within a block. They allocate the numbers to the customers and handle the routing of calls that are related to those numbers.

</td></tr><tr><td>

Parent Block

</td><td>

Parent block if there’s any.

</td></tr><tr><td>

Model ID

</td><td>

Model ID of the asset.

</td></tr><tr><td>

Number

</td><td>

Name of the parent inventory that you’re associating the child inventory with. The ServiceNow AI Platform automatically assigns this name.**Note:** This field is available only for the number elements of the inventory numbers.

</td></tr><tr><td>

Element type

</td><td>

Type of network inventory that you want to associate your VLAN or LAG number with. Select one of the following options: -   Network Interface
-   Physical Connection
-   Logical Connection

**Note:** This field is available only for the number elements of the inventory numbers.


</td></tr><tr><td>

Element

</td><td>

Network asset under an element type that you want to configure with.**Note:** This field is available only for the number elements of the inventory numbers.

</td></tr><tr><td>

Sequence

</td><td>

Sequence number of the network connection.**Note:** This field is available only for the number elements of the inventory numbers.

</td></tr><tr><td>

CIDR

</td><td>

Classless Inter-Domain Routing \(CIDR\) that is associated with the subnet, the IP address of the gateway, and the subnet mask. For VMware, the CIDR, gateway, and subnet mask fields are mandatory.

</td></tr><tr><td>

Managed Network

</td><td>

Name of the managed network that is associated with this IP pool and IP subnetwork.

</td></tr><tr><td>

Parent Pool

</td><td>

Name of the IP pool that is the parent of this IP pool or IP network subnet.

</td></tr><tr><td>

DNS Domain

</td><td>

Name of the IP addresses.

</td></tr><tr><td>

Reported Free Addresses

</td><td>

Number of the addresses that are free for this IP pool or IP subnet.

</td></tr><tr><td>

Reported Addresses In Use

</td><td>

Number of the addresses that are in use for this IP pool or IP subnet.

</td></tr><tr><td>

Reported Reserved Addresses

</td><td>

Number of the addresses that are reserved for this IP pool or IP subnet.

</td></tr><tr><td>

Service

</td><td>

Type of service.

</td></tr></tbody>
</table>**Parent Topic:**[Telecommunications Network Inventory reference](../concept/telecommunications-network-inventory-reference.md)

**Related topics**  


[Inventory number allocation](../concept/vlan_or_lag_number_management.md)

