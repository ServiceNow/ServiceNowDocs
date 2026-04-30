---
title: Commonly used network asset instance identification fields
description: Some network asset instance fields are common in the identification sections of the Telecommunications Network Inventory forms. The ServiceNow AI Platform uses these fields to identify and categorize your network inventory assets.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Reference, Telecommunications Network Inventory]
---

# Commonly used network asset instance identification fields

Some network asset instance fields are common in the identification sections of the Telecommunications Network Inventory forms. The ServiceNow AI Platform uses these fields to identify and categorize your network inventory assets.

<table id="table_htp_wkd_wrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Is Alarmable

</td><td>

Option that designates if an alarm system can be assigned to this network asset.

</td></tr><tr><td>

Asset

</td><td>

Name of the asset that is associated with this record.

</td></tr><tr><td>

Availability

</td><td>

Current status of whether a resource is used or not used. Select one of the following options:

-   Available
-   Used
-   Reserved
-   Shared

</td></tr><tr><td>

CLEI code

</td><td>

Assigned Common Language Equipment Identification \(CLEI\) for this network asset. CLEI codes are globally unique, 10-character alphanumeric intelligent codes that identify the equipment in a structured naming format. There’s a one-to-one relationship between a CLEI code and a manufacturer's product code, which is a part number that includes the hardware version.

</td></tr><tr><td>

CLLI code

</td><td>

Assigned equipment Common Location Identifier Code \(CLLI\) for this network asset. The North American telecommunications industry uses the CLLI code to specify the location and function of telecommunications equipment.

</td></tr><tr><td>

Function

</td><td>

Optional user-defined function code that you use to categorize the functions of the various network entities or assets. Select the search icon \(![Search icon.](../image/search.png)\) and select a function code.

</td></tr><tr><td>

Life Cycle Stage

</td><td>

Stage of the life cycle that this network asset is in:

-   **Deploy**

Network asset that is deployed in your network.

-   **Design**

Network asset that is being used for design purposes.

-   **End of life**

Network asset that is at the end of its useful life.

-   **Inventory**

Network asset that is an inventory item in use in the network.

-   **End of life**

Network asset that is missing and can't be located.

-   **Operational**

Network asset that is operational.

-   **Purchase**

Network asset that is in the purchase phase of its life.


</td></tr><tr><td>

Life Cycle Stage Status

</td><td>

Status of the network asset as it relates to the life cycle stage that it is in:

-   **In Maintenance**

Network asset that is currently in maintenance.

-   **In Use**

Network asset that is currently in use.

-   **Pending Retirement**

Network asset that is currently in maintenance.


</td></tr><tr><td>

Location

</td><td>

Geographic location of the network site. Select the search icon \(![Search icon.](../image/search.png)\) and select a location from the Location hierarchy. To learn more about the Location hierarchy, see [17d5ab04176723ba602d3da0ccbd65a6205cccb4.dita](../task/define-tni-locations.md).

</td></tr><tr><td>

Managed by

</td><td>

Name of the person who manages this network asset. Select the search icon \(![Search icon.](../image/search.png)\) and select a user from the listing.

</td></tr><tr><td>

Network domain

</td><td>

Domain of ownership and responsibility for this network asset or connection. Select one of the following options:

-   **Mobility**

Network asset that is associated with the mobility equipment domain.

-   **Telco**

Network asset that is associated with the telco equipment domain.

-   **Core**

Network asset that is associated with the core equipment domain.


</td></tr><tr><td>

Product Model

</td><td>

Product model, if any, that is associated with this network asset. Select the search icon \(![Search icon.](../image/search.png)\) and select a product model.

</td></tr><tr><td>

Replaceable

</td><td>

Option that designates if this network asset can be replaced if it malfunctions or is affected by a network outage.

</td></tr><tr><td>

Role

</td><td>

Optional user-defined role code that you use to categorize the roles or purposes of the various network entities or assets. Select the search icon \(![Search icon.](../image/search.png)\) and select a role code.

</td></tr><tr><td>

Serial number

</td><td>

Assigned serial number for this network asset.

</td></tr><tr><td>

Support group

</td><td>

Group that supports the network inventory.

</td></tr><tr><td>

Type

</td><td>

Optional user-defined type code that you use to categorize the types of the various network entities or assets. Select the search icon \(![Search icon.](../image/search.png)\) and select a type code.

</td></tr><tr><td>

Name

</td><td>

Descriptive name for this IP pool or IP network subnet.

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

Description

</td><td>

Descriptive information about this IP pool or IP network subnet.

</td></tr><tr><td>

DNS Domain

</td><td>

Name of the IP addresses.

</td></tr><tr><td>

Reported Addresses in Use

</td><td>

Number of the addresses that are in use for this IP pool or IP subnet.

</td></tr><tr><td>

Reported Free Addresses

</td><td>

Number of the addresses that are free for this IP pool or IP subnet.

</td></tr><tr><td>

Reported Reserved Addresses

</td><td>

Number of the addresses that are reserved for this IP pool or IP subnet.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Cable type|Name of the cable type.|
|Cable number|Number of the cable that is used in the physical connection.|
|Stand count|Number of fibers that this cable contains.|
|Cable length|Length of the cable in millimeters \(mm\).|
|Parent cable|Option that designates the top-layer physical connection.|
|Color code|Color of the cable line.|
|Spare length A|Length of the cable that connects to site A in millimeters \(mm\).|
|Spare length Z|Length of the cable that connects to site Z in millimeters \(mm\).|
|KML Route|Option that designates the fiber route maps in a KML format.|

**Parent Topic:**[Telecommunications Network Inventory reference](../concept/telecommunications-network-inventory-reference.md)

