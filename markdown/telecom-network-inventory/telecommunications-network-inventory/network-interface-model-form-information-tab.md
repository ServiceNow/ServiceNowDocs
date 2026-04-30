---
title: Network Interface Model form - Information tab
description: The information section in the model form enables you to create, review, and modify the details of a model.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, Telecommunications Network Inventory]
---

# Network Interface Model form - Information tab

The information section in the model form enables you to create, review, and modify the details of a model.

<table id="table_dgj_v3g_dtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Power \(watts\)

</td><td>

Electrical power of the network asset in watts.

</td></tr><tr><td>

Weight \(lbs\)

</td><td>

Weight of the network asset in pounds \(lbs\).

</td></tr><tr><td>

Virtual

</td><td>

Option to verify whether the network interface is physical or virtual.

**Note:** If you select **Virtual**, then the **Connector Type** field doesn’t appear.

</td></tr><tr><td>

Connector Type

</td><td>

Type of physical cable connector that is used for the connection of the cable to the network interface. Select one of the following options:

-   BNC \(Bayonet Neill-Concelman\) - Type of miniature radio frequency connector used for coaxial cables.
-   SC \(Square Connector\)- Square, common type of Fiber optic connector used as push-pull latch, to align the optical fibers for efficient light transmission.
-   LC \(Lucent Connector\)- Another version of the SC connector designed for high-density applications.
-   ST \(Straight Trip\)- a type of fiber optic connector commonly used for connecting optical fibers in telecommunications and data communication applications.
-   Wire Wrap -A technique for creating electrical connections on circuit boards.
-   RJ45 - Also known as 8P8C \(8 Position 8 Contact\) connector, is widely used type of connector for wired Ethernet networks.

</td></tr><tr><td>

Max physical connection support

</td><td>

Maximum number of physical connections that is supported by this model.

</td></tr><tr><td>

Port bandwidth

</td><td>

Measured bandwidth for the ports on this network interface. Select the search icon \( ![Search icon.](../image/search.png)\) and select a bandwidth.

</td></tr><tr><td>

Directionality

</td><td>

Type of the connections between the nodes of a network. Select one of the following options:

-   Tx- TX stands for Transmit. It refers to the direction in which data is being sent from a device.
-   Rx- RX signifies the endpoint that receives data. It's the input side for receiving information transmitted from another source, often labeled as TX \(Transmit\).
-   Tx/Rx
-   Bus- Bus directionality refers to the flow of data on a communication channel.
-   Broadcast- Broadcast directionality refers to the nature of signal transmission and reception in a broadcast system.

</td></tr><tr><td>

Interface Type

</td><td>

Type of port on the network interface. Select one of the following options:

-   Ethernet- Physical connection and speed capabilities of a device for connecting to a network. It involves cable type, speed, and standard.
-   Optical- specific design of a connector used in an optical transceiver. There are various types of optical interfaces, each with different shapes and data speed capabilities.
-   Serial- A serial interface transmits data one bit at a time, in contrast to a parallel interface that sends multiple bits simultaneously.

</td></tr><tr><td>

Port position

</td><td>

Position of a physical or logical port on an equipment.

</td></tr></tbody>
</table>**Parent Topic:**[Telecommunications Network Inventory reference](../concept/telecommunications-network-inventory-reference.md)

**Related topics**  


[Create a network interface model](../task/create-network-interface-model.md)

