---
title: Task attributes in Create logical connection form
description: The Task attributes in Create logical connection form enables you to create a logical connection between network interfaces in the Telecommunications Network Inventory application.
locale: en-US
release: yokohama
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2025-07-16"
reading_time_minutes: 1
breadcrumb: [Telecommunications Network Inventory reference, Telecommunications Network Inventory]
---

# Task attributes in Create logical connection form

The Task attributes in Create logical connection form enables you to create a logical connection between network interfaces in the Telecommunications Network Inventory application.

<table id="table_g1h_xdv_xfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Logical Connection Model

</td><td>

Logical connection model where this logical connection is configured.**Note:** The topology connection models are not listed if you are creating a logical connection in a change request.

</td></tr><tr><td>

Logical Connection Template

</td><td>

List of all templates based on the selected logical connection model.

</td></tr><tr><td>

Bandwidth AtoZ

</td><td>

Total bandwidth capacity from Site A to Site Z for this network connection.

</td></tr><tr><td>

Bandwidth ZtoA

</td><td>

Total bandwidth capacity from Site A to Site Z for this network connection.

</td></tr><tr><td>

A end Site

</td><td>

Starting network site where this logical connection is configured.

</td></tr><tr><td>

Z end Site

</td><td>

Ending network site where this logical connection is configured.

</td></tr><tr><td>

A end Equipment

</td><td>

Starting network equipment where this logical connection is configured.

</td></tr><tr><td>

Z end Equipment

</td><td>

Ending network equipment where this logical connection is configured.

</td></tr><tr><td>

Parent Port A

</td><td>

Network interface on which the new logical interface is representing the **Port A** of the connection.**Note:** A new logical interface is created by default based on the selected logical/physical connection model and is populated in the port A field under **Configuration** section of the logical or physical connection. The logical interface indicates the port name and number of child ports plus one of the selected port.

</td></tr><tr><td>

Parent Port Z

</td><td>

Network interface on which new logical interface is representing the **Port Z** of the connection.**Note:** A new logical interface is created by default based on the selected logical/physical connection model and is populated in the port Z field under **Configuration** section logical or physical connection. The logical interface indicates the port name and number of child ports plus one of the selected ports.

</td></tr></tbody>
</table>**Parent Topic:**[Telecommunications Network Inventory reference](../concept/telecommunications-network-inventory-reference.md)

**Related topics**  


[Create logical connection record using design and assign](../task/create-logical-connection-record-using-design-assign.md)

