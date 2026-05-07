---
title: Define the network interface details
description: Review, update, or create a network instance for a network interface that controls the signaling and management functions between your networks. You define these attributes so that you can track and manage your network instances in the Telecommunications Network Inventory application.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Manually creating and reviewing your network asset instances, Define inventory records, Use, Telecommunications Network Inventory]
---

# Define the network interface details

Review, update, or create a network instance for a network interface that controls the signaling and management functions between your networks. You define these attributes so that you can track and manage your network instances in the Telecommunications Network Inventory application.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent

## About this task

Network interfaces are used for the interconnection of signaling, or for the Internet Protocol \(IP\) or ATM networks. When you create a network interface record, it creates a corresponding configuration item \(CI\) record in the Network Interface \[cmdb\_ci\_interface\] table. To learn more, see [Data model](../concept/uses-for-network-inventory-data.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  From the list icon \(![List](../../tmt-assurance-workflows/image/lists_icon-proactive.png)\)\(, go to **Inventory** &gt; **Network Interfaces**.

3.  Select **New**.

4.  On the **Details** tab, in the Network Interface section, fill in the general information for the network interface.

    The fields in the following table are unique to the Network Interface form.

    To learn about the remaining identification fields that are common to most of the Inventory and Inventory number allocation menu forms, see [Commonly used network asset instance identification fields](../reference/commonly-used-tni-identification-fields.md).

    |Field|Description|
    |-----|-----------|
    |Name|Name of the network interface. The ServiceNow AI Platform uses this name to identify it in your network inventory.|

5.  On the **Details** tab, in the Configuration section, fill in the configuration information for the network interface.

    The following table lists the fields that are unique to the Configuration section.

    To learn about the remaining configuration fields that are common to most of the Inventory menu forms, see [Commonly used network asset instance configuration fields](../reference/commonly-used-tni-configuration-fields.md).

<table id="table_inq_wc2_wrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Equipment

</td><td>

Device that provides the technical functionality to a network.

</td></tr><tr><td>

Management option

</td><td>

Attribute that indicates who or what is responsible for managing this endpoint.

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


</td></tr><tr><td>

Port Type

</td><td>

Types of port on the network interface. Select one of the following options:

-   Ethernet- Physical connection and speed capabilities of a device for connecting to a network. It involves cable type, speed, and standard.
-   Optical- specific design of a connector used in an optical transceiver. There are various types of optical interfaces, each with different shapes and data speed capabilities.
-   Serial- A serial interface transmits data one bit at a time, in contrast to a parallel interface that sends multiple bits simultaneously.


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

Port Bandwidth

</td><td>

Measured bandwidth for the ports on this network interface. Select the search icon \( ![Search icon.](../image/search.png)\) and select a bandwidth.

</td></tr><tr><td>

Endpoint role

</td><td>

Endpoint role that is associated with the service endpoint for this network asset. An endpoint role is the function that is served by the endpoint of the service that you’re providing. Select one of the following options:

-   **ROOT** or **LEAF** endpoint role, as defined by the Metro Ethernet Forum \(MEF\).
-   **--None--** for no assigned endpoint role.


</td></tr><tr><td>

Virtual

</td><td>

Option to verify whether the network interface is physical or virtual.

**Note:** If you select **Virtual**, then the **Connector Type** field doesn’t appear.

</td></tr><tr><td>

Cabled

</td><td>

Option to verify if the interface is pre-cabled or not.

</td></tr><tr><td>

Wavelength

</td><td>

Optical wavelength of a port.

</td></tr></tbody>
</table>6.  To create the Telecommunications Network Inventory attributes for the Network Interface form, click **Set Inventory Attributes**.

    When you click the **Set Inventory Attributes** button, it creates the TNI CI Attributes record in the CI table as well as the Telecommunications Network Inventory CI Attributes tables and makes a relationship with the CI record.

    **Note:**

    If you click **Save** without clicking **Set Inventory Attributes**, it creates a CI record but not a Telecommunications Network Inventory CI record. In the network inventory workspace, the **Set Inventory Attributes** is visible only for the Telecommunications Network Inventory roles.

7.  On the TNI CI Attributes form, fill in the fields.

    To learn more about the Telecommunications Network Inventory attribute fields, see [TNI CI Attributes form](../reference/ci-attribue-form.md).

8.  Click **Save**.

    The Telecommunications Network Inventory attribute fields are displayed on the Network Interface form after you save the TNI CI Attributes form. The **Set Inventory Attributes** doesn’t appear when you reopen the CI record.

9.  To add the attachments, such as graphics or documents, click the attachment icon \(![Attachment icon.](../image/attachments-icon.png)\) in the right panel.

10. To view the Dependency views map, select the more options icon \(![More Options icon.](../image/options-icon.png)\) and then select **Dependency View**.

    The Dependency Views map graphically displays the CIs that support the specific network asset and the relationships between the CIs.

11. Select the more options icon \(![More Options icon.](../image/options-icon.png)\) and then select **Add Packs** to capture the attributes for a configuration item \(CI\) record.

    To learn more, see [Attribute pack for CI records](../concept/using-pack-table-ci-record.md).

12. Select the more options icon \(![More Options icon.](../image/options-icon.png)\) and then select **Decommission** to decommission a CI record.

    To learn more, see [Decommission an inventory record](decommision-an-inventory-record.md).

13. Click **Save**.

    The related tabs appear on the form. You can view or modify the related tab information. To learn more about the related tabs, see [Related tabs in the Network inventory forms](../reference/inventory-related-tab.md).

14. To view the associated network inventories, click the brick icon \(![Brick icon.](../image/infrastructure-relashionship.png)\).

    The Infrastructure Relationships section shows all the associated network inventories grouped by the individual network instances.


## What to do next

-   If you want to establish relationships with the other network assets, enter the details in the related tabs. To learn more, see [Related tabs in the Network inventory forms](../reference/inventory-related-tab.md).

-   To delete an inventory record, see [Delete a record](delete-inventory-record.md).

**Parent Topic:**[Manually creating and reviewing your network asset instances](../concept/creating-telecommunications-network-inventory.md)

**Related topics**  


[Modeling your workflow](../concept/telecommunications-network-inventory-workflow.md)

