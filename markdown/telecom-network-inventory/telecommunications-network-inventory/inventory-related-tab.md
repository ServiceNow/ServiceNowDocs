---
title: Related tabs in the Network inventory forms
description: The related tabs in the Network Inventory forms display the related records that dynamically change based on the connection and relationships with the other network assets. You can selectively view, modify, or update these records.
locale: en-US
release: yokohama
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Telecommunications Network Inventory reference, Telecommunications Network Inventory]
---

# Related tabs in the Network inventory forms

The related tabs in the Network Inventory forms display the related records that dynamically change based on the connection and relationships with the other network assets. You can selectively view, modify, or update these records.

<table id="table_tni_change_request_field"><thead><tr><th>

Tab

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Overview

</td><td>

Snapshot of some of the information about the telco equipment. The **Overview** tab displays the following sections:

-   **Usage**

Number of slots, interface cards, and interfaces that are open in the telco equipment.

-   **Images**

Image of the telco equipment. You can select the image to see a preview in a separate page.

-   **Relations**

Relationship with the associated network inventories. The Relations section shows all the child hierarchies that are associated with the telco equipment. You can only view the relations in the workspace.


 **Note:** This tab is available only for the Telco Equipment form.

</td></tr><tr><td>

Rack Equipment Placement

</td><td>

Details of the rack slot where this equipment is positioned. You can always update the details by selecting the text link displayed under the **Exclusively Used** column.**Note:** This field is applicable only for all equipment, IP routers, IP switches, IP firewalls, and cards.

</td></tr><tr><td>

Child Site

</td><td>

List of the child inventory sites that are associated with the parent site.**Note:** This tab is available only for the Network Site form.

</td></tr><tr><td>

Telco equipment

</td><td>

List of the telco equipment that is associated with the network inventory.**Note:** This tab is available only for the Network Site form.

</td></tr><tr><td>

Incidents

</td><td>

List of the incident records that are related to the network inventory.**Note:** This tab is available only for the Network Site form.

</td></tr><tr><td>

Change Requests

</td><td>

List of the Change Request records. To learn more about the change requests, see [Create a change request from Network Inventory Workspace](../task/create_a_change_request_in_tni.md).**Note:** This tab is available only for the Network Site, Telco Equipment, and Physical Connections forms.

</td></tr><tr><td>

Teams

</td><td>

List of the teams that are associated with the network inventory.

</td></tr><tr><td>

Physical Connections

</td><td>

List of the physical connections that are associated with the network inventory.**Note:** This tab is available only for the Telco Equipment form.

</td></tr><tr><td>

Logical Connections

</td><td>

List of the logical connections that are associated with the network inventory.**Note:** This tab is available only for the Telco Equipment form.

</td></tr><tr><td>

Order information

</td><td>

List of the order information that is related to the network inventory instance.**Note:** This tab is available only for the Network Interface, Physical Connections, and Logical Connections forms.

</td></tr><tr><td>

Number Elements

</td><td>

List of the number elements that are associated with your virtual local area network \(VLAN\) or link aggregation group \(LAG\). To learn more about the number elements fields, see [Commonly used network asset instance identification fields](commonly-used-tni-identification-fields.md).**Note:** This tab is available only for the Telco Equipment, Network Interface, Physical Connections, Logical Connections, and Inventory Number forms.

</td></tr><tr><td>

Physical connection elements

</td><td>

List of the connection elements that are added for the physical connections.**Note:** This tab is available only for the Physical Connections form.

</td></tr><tr><td>

Connection elements

</td><td>

List of the connection elements that are added for the logical connections. These elements should be the valid logical connections between the sites when the computation performs the path search. After creating a connection element, a relationship is created between the logical or physical connection and the next element under its default relationship type. To learn more about the connection element fields, see [Connection Element form](connection-element-form.md).

 **Note:**

-   This tab is available only for the logical connections.
-   The relationship gets updated if its connection element is modified or deleted. For example, the relationship gets deleted if you delete its connection element. To change the default relationship type, navigate to **System Definition** &gt; **Decision tables** &gt; **TNI CI Relationship Definition Policy**, and under **Decision table**, update the **CI Relationship Type** against the CI class.

</td></tr><tr><td>

Inventory Numbers

</td><td>

List of the inventory numbers that are associated with your network inventory. To learn more about the number elements, see [Define your inventory numbering](../task/define-tni-inventory-numbers.md).**Note:** This tab is available only for the Inventory Number form.

</td></tr><tr><td>

Channels

</td><td>

List of logical connections with the **Behaviour** field set to **Channel**.

</td></tr><tr><td>

IP Address

</td><td>

List of the IP addresses that are associated with your network inventory.**Note:** This additional tab is available for the equipment, interface card, network interface, and logical connection.

</td></tr><tr><td>

Inventory Groups

</td><td>

List and details of all the inventory groups.**Note:** This tab is available for the network site, equipment holder, equipment, interface card, network interface, physical connection, and logical connection.

</td></tr><tr><td>

DNS Name

</td><td>

List of all the DNS names of the IP addresses.**Note:** This listing is available only for IP addresses.

</td></tr><tr><td>

CMDB Group Contains Configuration Items

</td><td>

List of all the configuration items \(CIs\) that you want to add to this inventory group. You can't duplicate a CI but you can add a CI in different inventory groups. To prioritize a CI, select one of the following values in the **Member Role** field when you’re creating the CI:-   Main
-   Primary
-   Secondary
-   Tertiary
-   Load Balancing
-   Active
-   Passive

 **Note:** Only the inventory agent and the inventory administrator can review, create, update, or delete the CI items.

</td></tr><tr><td>

Parent Inventory Groups

</td><td>

List of all the parent inventory groups.

</td></tr><tr><td>

Child Inventory Groups

</td><td>

List of all the child inventory groups.

</td></tr><tr><td>

IP Pools

</td><td>

List of all the child IP pools of this parent pool.

</td></tr><tr><td>

IP Subnetwork

</td><td>

List of all the child IP subnetworks of this IP pool.

</td></tr><tr><td>

Telephone Numbers

</td><td>

List of all the telephone numbers that you want to assign to this telephone block.

</td></tr><tr><td>

Telephone Number Allocations

</td><td>

List of the telephone number allocations that you want to assign to this telephone block. This list is auto-generated. By default, the availability is true and the status is New.

</td></tr><tr><td>

CMDB 360 Data

</td><td>

List of all discovery sources at the CI attribute level. To learn more, see [CMDB 360/Multisource CMDB](https://www.servicenow.com/docs/access?context=multisource-cmdb&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Inventory Revision Histories

</td><td>

List of all revised CIs of the selected connection.**Note:** This tab is available only for physical and logical connection.

</td></tr><tr><td>

Asset

</td><td>

List of all assets of the inventory.

</td></tr><tr><td>

Model Component

</td><td>

List of the model components of this inventory. You can mark the component as mandatory or optional.

</td></tr><tr><td>

Vendor Catalog Items

</td><td>

List of all vendor catalogs of this inventory. To learn more, see [Vendor Catalog Items](https://servicenow.com/docs/bundle/washingtondc-it-asset-management/page/product/product-catalog/concept/c_ManageVendorCatalogItems.html).

</td></tr><tr><td>

Hardware Model Lifecycles

</td><td>

Hardware model lifecycle details of this inventory

</td></tr><tr><td>

Network Model Relationships

</td><td>

List of all model relationships associated with this inventory

</td></tr><tr><td>

Packs

</td><td>

List of all added packs. To learn more, see [Attribute packs](../concept/telecommunication-network-inventory-pack.md).

</td></tr><tr><td>

Capacity Metrics

</td><td>

List of capacity metric records that are associated with the network inventory record. To learn more see, [View a capacity metric](../task/modify-capacity-metric.md).**Note:** This tab is available only for equipment, rack, slot, cabinet, card and interface records.

</td></tr><tr><td>

Strands

</td><td>

List of strand records that are associated with the cable record.**Note:** This tab is available only for card records.

</td></tr><tr><td>

Protection paths

</td><td>

List of protection paths that are associated with logical connection record.**Note:** This tab is available only for physical and logical connection records.

</td></tr><tr><td>

Network Topology Root Nodes

</td><td>

List of root node records that are associated with network topology record.**Note:** This tab is available only for network topology records.

</td></tr><tr><td>

Media

</td><td>

List of media records that are associated with the network inventory records.

</td></tr><tr><td>

Places

</td><td>

List of place records.

</td></tr></tbody>
</table>**Parent Topic:**[Telecommunications Network Inventory reference](../concept/telecommunications-network-inventory-reference.md)

**Related topics**  


[Reviewing and updating your network inventory with the Network Inventory Workspace](../concept/tni-workspace.md)

