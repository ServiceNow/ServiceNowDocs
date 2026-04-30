---
title: Inventory Model form - Information
description: The Information section of the Inventory Model form enables you to create, review, and modify the network asset details of a model.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 11
breadcrumb: [Inventory Model forms, Reference, Telecommunications Network Inventory]
---

# Inventory Model form - Information

The Information section of the Inventory Model form enables you to create, review, and modify the network asset details of a model.

<table id="table_dgj_v3g_dtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Height \(U\)

</td><td>

Number of rack units required for the model.**Note:** This field is only applicable to the equipment models.

</td></tr><tr><td>

Power

</td><td>

Electrical power, in watts.

</td></tr><tr><td>

Sound power

</td><td>

Noise measurement, in bels \(1 bel=10 decibels\).

</td></tr><tr><td>

Connection type

</td><td>

Type of connection:

-   **Cable**

Multi-colored cable connection.

-   **Connection**

Standard connection that you establish with a piece of equipment. For example, the connection between a monitor and a computer.

-   **Strand**

Multi-strand fiber connection.

-   **Wireless**

3G, 4G, or 5G wireless connection.


</td></tr><tr><td>

Power unit

</td><td>

Units in which the power of the asset is measured. Select any one of the following unit.-   Watts \(W\)
-   Kilowatts \(KW\)
-   Megawatts \(MW\)
-   Horsepower \(HP\)

</td></tr><tr><td>

Rated Power

</td><td>

Maximum power allotted to the asset.

</td></tr><tr><td>

Unit of Measurement System

</td><td>

Measurement type based on which the **Max weight capacity unit** is fetched. Select any one of the following measurement type.-   Metric
-   US Imperial

</td></tr><tr><td>

Weight unit

</td><td>

Unit in which weight of the asset is measured. Select any one of the following.-   Grams \(g\)

**Note:** This field is only accessible when the Metric system is used for unit of measurement.

-   Kilograms \(kg\)

**Note:** This field is only accessible when the Metric system is used for unit of measurement.

-   Ounces \(oz\)

**Note:** This field is only accessible when the US Imperial system is used for unit of measurement.

-   Pounds \(lbs\)

**Note:** This field is only accessible when the US Imperial system is used for unit of measurement.


</td></tr><tr><td>

Weight

</td><td>

Maximum weight of the rack or cabinet or slot or subslot.

</td></tr><tr><td>

Slot naming pattern

</td><td>

Name patterns that are used to define the names that are generated for the slots and interfaces that are on the equipment or card. Because these name patterns are at the model level, they’re applied by default to every template of that model. These name patterns are editable for the different instances of the same model. To learn more about the naming convention, see [Naming convention for associated templates](name-convention-templates.md).

 Although the names are generated automatically, you can manually edit the names of the templates.

 **Note:**

1.  This field is applicable for the equipment models and the interface card models.
2.  The generated name remains empty if the following occurs:
    -   The variable names are misspelled.
    -   You use the parent\_slot or equipment\_slot information for the interfaces or slots that are in the equipment.
3.  If this field is left empty, then the default naming pattern is considered. Here, the default naming is Slot-001, where 001 is the slot start number.

This field is applicable for the equipment models and the interface card models.

</td></tr><tr><td>

Interface naming pattern

</td><td>

Name patterns that are used to define the names that are generated for the slot and Interfaces on the equipment or card. Because these name patterns are at the model level, they’re applied by default to every template of that model. These name patterns are editable for the different instances of the same model. To learn more about the naming convention, see [Naming convention for associated templates](name-convention-templates.md).

 Although the names are generated automatically, you can manually edit the names of the templates.

 **Note:**

-   This field is available only for **Equipment models** and **Interface card models**.
-   The generated name remains empty if the following occurs:
    -   The variable names are misspelled.
    -   You use the parent\_slot or equipment\_slot information for the interfaces or slots that are in the equipment.
-   If this field is left empty, then the default naming pattern is considered. Here, the default naming is Port-001, where 001 is the interface start number.

This field is available only for the equipment models and interface card models.

</td></tr><tr><td>

Dimensions unit

</td><td>

Unit in which the physical dimensions of the asset are measured. Select one from the following:-   Inches \(in\)
-   Feet \(ft\)
-   Miles \(mi\)

**Note:** This field is applicable for the equipment models, the equipment holder models, and the physical connection models.

</td></tr><tr><td>

Height

</td><td>

Height of the network asset, expressed in the unit of measure that you designate in the **Units** field.

-   For example, enter `60` if the height of the asset is 60 inches and you've selected `Inches` as the unit of measure in the **Units** field.
-   The ServiceNow AI Platform uses this information to calculate the cubic dimensions of the asset to determine its physical placement within its designated network site.

 **Note:** This field is applicable for the equipment models and the equipment holder models.

</td></tr><tr><td>

Width

</td><td>

Length of the network asset, expressed in the unit of measure that you designate in the **Units** field.

-   For example, enter `12` if the asset is one foot, or enter `60` if the asset is 60 inches and you've selected `Inches` as the unit of measure in the **Units** field.
-   The ServiceNow AI Platform uses this information to calculate the cubic dimensions of the asset to determine its physical placement within the designated network site.

 **Note:** This field is applicable for the equipment models and the equipment holder models.

</td></tr><tr><td>

Depth

</td><td>

Depth of the network asset that is expressed in the unit of measure that you designate in the **Units** field.**Note:** This field is applicable for the equipment models and equipment holder models.

</td></tr><tr><td>

RU numbering direction

</td><td>

Numbering sequence of rack units in the Rack view. Select one of the following.-   Top to bottom - Numbering sequence that starts at the top of a list.
-   Bottom to top - Numbering sequence that starts at the bottom of a list.

</td></tr><tr><td>

Slot start number

</td><td>

The first number to assign to the slots in this model. The slot names are generated automatically depending on the starting number. **Note:**

-   The entered value doesn’t affect the unit position. The unit position always starts from 1 and is used in the slot naming pattern.
-   This field is applicable for the equipment models and the interface card models.

</td></tr><tr><td>

Interface start number

</td><td>

Starting number that you assign to the interfaces of the equipment or the card. For example, if the starting number is 10 for 20 interfaces, then the interface numbers start from 10, such as Port-010, Port-011, and so on to Port-029. **Note:**

-   The interface numbers are generated automatically based on the entered value. The unit position isn’t affected. The unit position always starts from 1 and is used in the interface naming pattern.
-   This field is applicable for Equipment models and Interface card models.

</td></tr><tr><td>

CLEI code

</td><td>

Assigned Common Language Equipment Identification \(CLEI\) for this network asset. CLEI codes are globally unique, 10-character alphanumeric intelligent codes that identify the equipment in a structured naming format. There’s a one-to-one relationship between a CLEI code and a manufacturer's product code, which is a part number that includes the hardware version.

 **Note:** This field is applicable for all types of models except the physical connection models, the logical connection models, and the network interface models.

</td></tr><tr><td>

Connector type

</td><td>

Type of physical cable connector that is used for the connection of the cable to the network interface. Select one of the following options:

-   BNC \(Bayonet Neill-Concelman\) - Type of miniature radio frequency connector used for coaxial cables.
-   SC \(Square Connector\)- Square, common type of Fiber optic connector used as push-pull latch, to align the optical fibers for efficient light transmission.
-   LC \(Lucent Connector\)- Another version of the SC connector designed for high-density applications.
-   ST \(Straight Trip\)- a type of fiber optic connector commonly used for connecting optical fibers in telecommunications and data communication applications.
-   Wire Wrap -A technique for creating electrical connections on circuit boards.
-   RJ45 - Also known as 8P8C \(8 Position 8 Contact\) connector, is widely used type of connector for wired Ethernet networks.

 **Note:** This field is only applicable to Network interface models.

</td></tr><tr><td>

Slots occupied

</td><td>

Number of slots that are occupied in the card.**Note:** This field is only applicable to the interface card models.

</td></tr><tr><td>

Length

</td><td>

Length of the network asset, expressed in the unit of measure that you designate in the **Units** field.

-   For example, enter `12` if the asset is one foot, or enter `60` if the asset is 60 inches and you've selected `Inches` as the unit of measure in the **Units** field.
-   The ServiceNow AI Platform uses this information to calculate the cubic dimensions of the asset to determine its physical placement within the designated network site.

</td></tr><tr><td>

Enable Interconnect

</td><td>

Option that you can select so that all the interfaces on the equipment are interconnected to each other.**Note:**

-   The default algorithm for the interconnection is `(N/2) +1`, where `N` is the total number of interfaces on the equipment, is applied. For the odd port numbers, the system takes `N` as the previous number `(N-1)` and creates the interconnections. For example, let's say that you have a piece of equipment that has 10 interfaces. If you select this option, the first interface is interconnected with the sixth interface, 2–7, 3-8, 4-9, and 5–10.
-   This field is only applicable to the equipment models.

All the created interconnections are listed as a configuration item \(CI\) relationship.

</td></tr><tr><td>

Orientation

</td><td>

Physical orientation of the slots in this network asset:

-   **--None--**

No specific physical slot orientation.

-   **Horizontal**

Horizontal slot orientation.

-   **Vertical**

Vertical slot orientation.


 **Note:** This field is only applicable to the equipment holder models.

</td></tr><tr><td>

Virtual

</td><td>

Option to verify whether the network interface is physical or virtual.

**Note:** If you select **Virtual**, then the **Connector Type** field doesn’t appear.

This field is applicable only for Network interface models.

</td></tr><tr><td>

Max physical connection support

</td><td>

Maximum connections that can be connected to this interface model. By default, it’s considered as 1.**Note:** This field is only applicable to the network interface models.

</td></tr><tr><td>

Port bandwidth

</td><td>

Measured bandwidth for the ports on this network interface. Select the search icon \( ![Search icon.](../image/search.png)\) and select a bandwidth.

 **Note:** This field is only applicable to the network interface models.

</td></tr><tr><td>

Directionality

</td><td>

Type of the connections between the nodes of a network. Select one of the following options:

-   Tx- TX stands for Transmit. It refers to the direction in which data is being sent from a device.
-   Rx- RX signifies the endpoint that receives data. It's the input side for receiving information transmitted from another source, often labeled as TX \(Transmit\).
-   Tx/Rx
-   Bus- Bus directionality refers to the flow of data on a communication channel.
-   Broadcast- Broadcast directionality refers to the nature of signal transmission and reception in a broadcast system.

 **Note:** This field is only applicable to the network interface models.

</td></tr><tr><td>

Interface type

</td><td>

Type of port on the network interface. Select one of the following options:

-   Ethernet- Physical connection and speed capabilities of a device for connecting to a network. It involves cable type, speed, and standard.
-   Optical- specific design of a connector used in an optical transceiver. There are various types of optical interfaces, each with different shapes and data speed capabilities.
-   Serial- A serial interface transmits data one bit at a time, in contrast to a parallel interface that sends multiple bits simultaneously.

 **Note:** This field is only applicable to the network interface models.

</td></tr><tr><td>

Behavior

</td><td>

Option to choose the mode of connection. Select one of the following options:

-   Channel
-   Connection

 **Note:** This field is only applicable to the logical connection models.

</td></tr><tr><td>

Routing behavior

</td><td>

Routing behavior attribute that controls routing enforcement. -   Select **No route** if no route is required for this connection type, or
-   Select **Parallel sequential** to enable multi-route connection resources that are used to route a connection. Here, path elements are required for the routed connections.

 **Note:** This field is only applicable to the logical connection models.

</td></tr><tr><td>

Logical Interface Model

</td><td>

List of all the logical interface models for the selected logical connection model.**Note:** During the creation of a logical connection, the logical interfaces for port A and port Z are created based on the selected logical interface model.

</td></tr><tr><td>

RU naming pattern

</td><td>

Naming pattern for the rack templates.

**Note:**

-   By default the naming pattern is "RU-"+position.
-   This field is visible only for **Equipment rack** model category.

</td></tr><tr><td>

Post type

</td><td>

Select any one of the following type

-   **2 Post**: Select if your rack has two vertical supports.
-   **4 Post**: Select if your rack has four vertical supports.

**Note:** This field is applicable only if the selected **Model categories** is **Equipment rack**.

</td></tr></tbody>
</table>**Parent Topic:**[Inventory Model forms](tni-model-forms.md)

**Related topics**  


[Create inventory models](../concept/creating-your-inventory-models.md)

