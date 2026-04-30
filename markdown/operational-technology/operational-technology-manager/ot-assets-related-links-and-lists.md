---
title: OT device related items and related lists
description: The All OT Devices, All OT Devices by IP Address, and All OT Devices by CI menu options contain several related items and lists.
locale: en-US
release: zurich
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Edit or view OT devices after import or discovery, Use, Operational Technology Manager, Operational Technology]
---

# OT device related items and related lists

The All OT Devices, All OT Devices by IP Address, and All OT Devices by CI menu options contain several related items and lists.

## Related items

This section lists any related or subordinate items that are associated with this OT device.

**Note:** Not all OT devices display the following related lists. For OT devices in an Operational Technology class or extended class, the following related lists are displayed. For OT devices categorized in a different hardware class, such as Windows Server, an instance admin must add the related lists to the form.

1.  To view the related records, click the name of the related item \(for example, Memory Modules\).
2.  To add a configuration item \(CI\) relationship for this OT device, click the add CI relationships icon \(![Add CI relationships icon.](../image/add-ci-relationships-icon.png)\). Use the search field to find the CI item that you want to create a relationship for.
3.  To access the Dependency View form to see a pictorial depiction of the OT device relationships, click the show dependency views icon \(![Show dependency views icon.](../image/show-dependency-views-icon.png)\).
4.  To change the settings that govern how the related items appear and are filtered, click the settings icon \(![Settings icon.](../image/settings-icon.png)\).

<table id="table_opr_3t1_vxb"><thead><tr><th>

Related list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

IP Address

</td><td>

The IP addresses, IP versions, net masks, network partition identifiers, NIC numbers, and configuration items that are associated with the OT device.

</td></tr><tr><td>

Network Adapters

</td><td>

The names, MAC addresses, IP addresses, Netmasks, MAC manufacturers, and Dynamic Host Configuration Protocol \(DHCP\)-enabled indicators. It includes statuses of the network adapters that are associated with the OT device.

</td></tr><tr><td>

Serial Numbers

</td><td>

The serial numbers, validity indicators, and serial number types that are associated with the OT device.

</td></tr><tr><td>

Equipment Model Entities

</td><td>

The equipment model entities that are automated by the OT device.

</td></tr><tr><td>

OT Subnet Mappings

</td><td>

The subnet mapping that associates an OT device with an equipment model entity.

</td></tr><tr><td>

OT Control Modules

</td><td>

The control modules that are associated with the OT device of type OT control system or extended classes \(for example, PLC\).

 Each OT control module that has an "Owned by: Owns" relationship with the OT Control System record that is displayed.

 In the platform, the user can create an OT Control module.

 You can choose from the following Input/Output values depending on the **Module type** field:

-   None
-   Local
-   Remote
-   Distributed

</td></tr><tr><td>

CMDB 360

</td><td>

The related CMDB 360 data in the CMDB 360 \[cmdb\_multisource\_data\] table.

</td></tr><tr><td>

Memory Modules

</td><td>

The serial numbers, validity indicators, and serial number types for the memory modules that are associated with the OT device.

</td></tr><tr><td>

Software Installed

</td><td>

The application software, if any, that is installed for the OT device.

</td></tr><tr><td>

OT Vulnerable Items

</td><td>

The vulnerable items that are associated with the OT device.

</td></tr><tr><td>

OT Incidents

</td><td>

The OT incidents that are associated with the OT device.

</td></tr><tr><td>

OT Change Requests

</td><td>

The OT Change requests that are associated with the OT device.

</td></tr><tr><td>

External System Metadata

</td><td>

The URL of the device in the source system, discovery source, and updated devices that are associated with the CI.

 The URL is automatically populated by the source system through the service graph connector.

</td></tr><tr><td>

OT Protocols

</td><td>

This is applicable for protocol converter class.

 The protocols, description, vendor, and version that are associated with the protocol converter class.

</td></tr><tr><td>

Backup Information

</td><td>

The Backup Information object associated with the current CI.

</td></tr><tr><td>

Device to Device Connections

</td><td>

Shows the network connections an OT device has with other devices.

</td></tr><tr><td>

IP Network Subnets

</td><td>

Shows all subnets the device is associated with.

</td></tr><tr><td>

Key Value

</td><td>

Additional information related to the OT device that's populated with the available OT integrations and captured as Key value pairs.

</td></tr><tr><td>

Software Instance

</td><td>

Captures the software installed on the OT device if Software Asset Management isn't available. **Note:** If Software Asset Management is installed and entitled, the software installed data is available in the Software Installation related list.

</td></tr><tr><td>

Firmware Installation

</td><td>

Firmware associated with the OT device.

</td></tr><tr><td>

VLAN Configurations

</td><td>

Captures the following VLAN information associated with the OT device.-   VLAN ID
-   VLAN Tag
-   Subnet
-   VLAN Type

</td></tr></tbody>
</table>-   **[Operational Technology device form](ot-assets-form.md)**  
Use the Operational Technology \(OT\) device form to edit the detailed information for the OT devices in your enterprise.
-   **[Convert an IT hardware device to an OT device](../task/convert-it-asset-into-ot-asset.md)**  
If you've identified IT hardware devices that belong to the OT network, you can convert these IT Configuration Items \(CI\) into OT devices.
-   **[Convert IT hardware to OT devices in a bulk edit](../task/bulk-edit-to-convert-it-records-into-ot-records.md)**  
Choose multiple IT hardware devices and convert them to OT devices in a bulk edit so that you can edit your records more quickly and efficiently.
-   **[Convert your OT devices to IT hardware devices in a bulk edit](../task/bulk-edit-ot-records.md)**  
Bulk edit your Operational Technology \(OT\) devices to remove the OT device details. Then convert your OT devices to IT hardware devices.
-   **[Map IP addresses to OT devices](../task/map-ip-addresses-to-ot-devices.md)**  
You can use the `SyncIPAddressToOT` scheduled job to update and synchronize the IP address information for all the available OT devices. The `SyncIPAddressToOT` scheduled job acquires the IP address information from the IP address \(cmdb\_ci\_ip\_address\) table and adds it to the IP address field of the CI.
-   **[View and edit device to device connections](../task/view-device-to-device-connections.md)**  
View and edit device-to-device connections for your Operational Technology \(OT\) devices using the Device to Device Connections list in the Industrial Workspace.

**Parent Topic:**[Edit or view OT devices after import or discovery](../task/view-ot-assets.md)

