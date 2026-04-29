---
title: Cable form
description: The Cable form enables you to describe the details for an optical fiber cable record.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reference, Telecommunications Network Inventory]
---

# Cable form

The Cable form enables you to describe the details for an optical fiber cable record.

<table id="table_htp_wkd_wrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of this cable record. The ServiceNow AI Platform uses this name to identify it in your network inventory.

</td></tr><tr><td>

Support group

</td><td>

Group that supports the network inventory.

</td></tr><tr><td>

Asset

</td><td>

Name of the asset that is associated with this record.

</td></tr><tr><td>

Managed by

</td><td>

Name of the person who manages this network asset. Select the search icon \(![Search icon.](../image/search.png)\) and select a user from the listing.

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

Model ID

</td><td>

Model ID of the asset.

</td></tr><tr><td>

Domain

</td><td>

A unique name or address assigned to the device within the domain.

</td></tr><tr><td>

A end termination

</td><td>

Starting point such as an interface or slot where this cable is connected with.

</td></tr><tr><td>

Z end termination

</td><td>

Ending point such as an interface or slot where this cable is connected with.

</td></tr><tr><td>

A end connector

</td><td>

Type of physical cable connector that is used for the starting point of the cable. Select one of the following options:-   **BNC**

BNC connector is used for video and RF applications and found in the coaxial cable networks.

-   **SC**

A square-shaped snap-in connector.

-   **LC**

Small and a push-and-pull design with a latch mechanism.

-   **ST**

A bayonet-style twist lock and a long, cylindrical ferrule.

-   **Wire Wrap**

Wrapping a thin, stripped wire around a post or pin to establish a connection.

-   **RJ45**

Connectors have eight pins and are used on the ends of twisted-pair cables.


</td></tr><tr><td>

Z end connector

</td><td>

Type of physical cable connector that is used for the ending point of the cable. Select one of the following options:-   **BNC**

The Bayonet Neill Concelman \(BNC\) connector is used for video and RF applications and found in the coaxial cable networks.

-   **SC**

A square-shaped snap-in connector.

-   **LC**

Small and a push-and-pull design with a latch mechanism.

-   **ST**

A bayonet-style twist lock and a long, cylindrical ferrule.

-   **Wire Wrap**

Wrapping a thin, stripped wire around a post or pin to establish a connection.

-   **RJ45**

Connectors have eight pins and are used on the ends of twisted-pair cables.


</td></tr><tr><td>

Length

</td><td>

Total length of the cable.

</td></tr><tr><td>

Length unit

</td><td>

Unit of measure in which you’re expressing the route length of the cable. Select one of the following options:-   **--None--**

No distance measurement is expressed for the connection route length.

-   **Inches**

Distance is expressed in inch.

-   **Feet**

Distance is expressed in feet.

-   **Miles**

Distance is expressed in miles.

-   **Meters**

Distance is expressed in meters.

-   **Centimeters**

Distance is expressed in centimeters.

-   **Kilometers**

Distance is expressed in kilometers.


</td></tr><tr><td>

Comments

</td><td>

Free form text that is used to comment on a network asset. For example, `Duty tech is Rahul Dev`.

</td></tr><tr><td>

Operational status

</td><td>

Operational status of the network inventory asset.

</td></tr></tbody>
</table>**Parent Topic:**[Telecommunications Network Inventory reference](../concept/telecommunications-network-inventory-reference.md)

**Related topics**  


[Define the cable details](../task/define-cable.md)

