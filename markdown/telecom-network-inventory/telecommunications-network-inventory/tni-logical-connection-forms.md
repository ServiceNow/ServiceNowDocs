---
title: Logical Connection form
description: The Logical Connection form enables you to define a logical connection by describing its configuration and connection details.The Logical Connection form enables you to describe the details for a logical connection.The Configuration section in the Logical Connection form enables you to create a logical connection.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Reference, Telecommunications Network Inventory]
---

# Logical Connection form

The Logical Connection form enables you to define a logical connection by describing its configuration and connection details.

**Parent Topic:**[Telecommunications Network Inventory reference](../concept/telecommunications-network-inventory-reference.md)

## Logical Connection form

The Logical Connection form enables you to describe the details for a logical connection.

<table id="table_htp_wkd_wrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of this logical connection The ServiceNow AI Platform uses this name to identify it in your network inventory.

</td></tr><tr><td>

Max percent over subscription

</td><td>

Percent of subscription allowed for a logical connection with respect to the bandwidth.

</td></tr><tr><td>

Site A

</td><td>

Originating network site for this connection. Select the search icon \( ![Search icon.](../image/search.png)\) and select a network site. To learn more, see [6ae017e0af7d4246ad6f9813addb0b7ccaa73376.dita](../task/define-tni-sites.md).

</td></tr><tr><td>

Site Z

</td><td>

Destination network site for this connection. Select the search icon \( ![Search icon.](../image/search.png)\) and select a network site. To learn more, see [6ae017e0af7d4246ad6f9813addb0b7ccaa73376.dita](../task/define-tni-sites.md).

</td></tr></tbody>
</table>**Related topics**  


[Define the logical connection details](../task/define-tni-logical-connections.md)

## Logical Connection form - Configuration

The Configuration section in the Logical Connection form enables you to create a logical connection.

<table id="table_f3c_dmd_wrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Port A

</td><td>

Network interface that is used in the Port A connection. Select the search icon \( ![Search icon.](../image/search.png)\) and select a network interface. To learn more, see [Define the network interface details](../task/define-tni-interfaces.md).

</td></tr><tr><td>

Bandwidth AtoZ

</td><td>

Total bandwidth capacity from Site A to Site Z for this network connection.

</td></tr><tr><td>

Planned date

</td><td>

Projected date for the implementation.

</td></tr><tr><td>

Framing type

</td><td>

Type of frame used in the connection. Select one of the following:-   None
-   AMI \(Alternate Mark Inversion\) - A line coding scheme where zeros are represented by no voltage, and ones are represented by alternating positive and negative voltages.
-   B4ZS \(Bipolar with Four-Zero Substitution\) - A technique that replaces sequences of four consecutive zeros in a digital signal with a special pattern to maintain synchronization.
-   B8ZS \(Bipolar with Eight-Zero Substitution\) - Similar to B4ZS, but it replaces sequences of eight consecutive zeros with a special pattern to maintain synchronization in high-speed digital signals.

</td></tr><tr><td>

Protocol version

</td><td>

Protocol version number.

</td></tr><tr><td>

Endpoint role

</td><td>

Endpoint role that is associated with the service endpoint for this network asset. An endpoint role is the function that is served by the endpoint of the service that you’re providing. Select one of the following options:

-   **ROOT** or **LEAF** endpoint role, as defined by the Metro Ethernet Forum \(MEF\).
-   **--None--** for no assigned endpoint role.

</td></tr><tr><td>

Port Z

</td><td>

Network interface that is used in the Port Z connection. Select the search icon \(![Search icon.](../image/search.png)\) and select a network interface. To learn more, see [Define the network interface details](../task/define-tni-interfaces.md).

</td></tr><tr><td>

Bandwidth ZtoA

</td><td>

Total bandwidth capacity from Site Z to Site A for this network connection.

</td></tr><tr><td>

Cost

</td><td>

Cost of this network asset.

</td></tr><tr><td>

Distance

</td><td>

Route length of this connection, expressed in the unit of measure that you select in the **Unit** field.

</td></tr><tr><td>

Unit

</td><td>

Unit of measure in which you’re expressing the route length of the connection in the **Distance** field. Select one of the following options:

-   **--None--**

No distance measurement expressed for the connection route length.

-   **Miles**

Distance is expressed in miles.

-   **Kilometers**

Distance is expressed in kilometers.

-   **Feet**

Distance is expressed in feet.

-   **Meters**

Distance is expressed in meters.


</td></tr></tbody>
</table>**Note:** To learn about the remaining configuration fields that are common to most of the Inventory menu forms, see [Commonly used network asset instance configuration fields](commonly-used-tni-configuration-fields.md).

**Related topics**  


[Define the logical connection details](../task/define-tni-logical-connections.md)

