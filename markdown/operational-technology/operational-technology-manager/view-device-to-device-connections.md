---
title: View and edit device to device connections
description: View and edit device-to-device connections for your Operational Technology \(OT\) devices using the Device to Device Connections list in the Industrial Workspace.
locale: en-US
release: zurich
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2026-02-09"
reading_time_minutes: 2
breadcrumb: [OT device related items and related lists, Edit or view OT devices after import or discovery, Use, Operational Technology Manager, Operational Technology]
---

# View and edit device to device connections

View and edit device-to-device connections for your Operational Technology \(OT\) devices using the Device to Device Connections list in the Industrial Workspace.

## Before you begin

-   Ensure you have the Industrial Core \[sn\_ot\_core\] plugin installed.
-   Role required:

    |Role|Description|
    |----|-----------|
    |cmdb\_ot\_viewer|Required to read or view device to device connections.|
    |cmdb\_ot\_editor, cmdb\_ot\_isa\_editor|Required to edit, create, or delete device to device connections.|


## About this task

The Device to Device Connections uses the `OTNetworkUtils` script include for the OT device look-up logic. The look-up logic identifies the corresponding Source and Destination CIs based on IP addresses, sites, and managed networks.

The Device to Device Connections list shows fields from both the OT Device Network Connection \[sn\_ot\_device\_network\_connection\] table and the CI relationships \[cmdb\_rel\_ci\] table.

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace**.

2.  Select the **List** \(![List icon](../../../common/image/icon-list.png)\) icon.

3.  Under the **OT Network** module, select the **Device to Device Connections** list.

4.  If needed, edit the following fields by selecting the checkbox next to an device to device connection and clicking **Edit**.

<table id="table_ydg_5sp_sfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Parent

</td><td>

Configuration item \(CI\) record of the source device.

</td></tr><tr><td>

Child

</td><td>

CI record of the destination device.

</td></tr><tr><td>

Source IP Address

</td><td>

IP address assigned to the source device.

</td></tr><tr><td>

Source Device CI

</td><td>

CI record of the source device.

</td></tr><tr><td>

Source MAC Address

</td><td>

MAC address of the source device.

</td></tr><tr><td>

Destination IP Address

</td><td>

IP address assigned to the destination device.

</td></tr><tr><td>

Destination Device CI

</td><td>

CI record of the destination device.

</td></tr><tr><td>

Destination MAC Address

</td><td>

MAC address of the destination device.

</td></tr><tr><td>

Destination Port

</td><td>

Network port used by the destination device for communication.

</td></tr><tr><td>

Last Communication Time stamp

</td><td>

Date and time when the devices last communicated.**Note:** Any device-to-device connection record with a Last Communication Time stamp of 90 days or longer is deleted.

To edit the Last Communication Time stamp, perform the following actions.

1.  Navigate to **All** &gt; **Instance Scan** &gt; **Table Cleanup**.
2.  In the sn\_ot\_device\_network\_connection record, edit the **Age in seconds** field as needed. The default is `7,776,000`.


</td></tr><tr><td>

Transport Protocol

</td><td>

Protocol used for data transfer. For example, TCP, UDP.

</td></tr><tr><td>

Application Protocol

</td><td>

Application-level protocol used. For example, HTTP, Modbus, FTP.

</td></tr><tr><td>

Source Managed Network

</td><td>

Managed network segment where the source device resides.

</td></tr><tr><td>

Destination Managed Network

</td><td>

Managed network segment where the destination device resides.

</td></tr><tr><td>

Discovery Source

</td><td>

Source that's providing the connection information.

</td></tr></tbody>
</table>5.  Select **Save**.


## Result

To view a device-to-device connection for an OT device, you can access the Device to Device Connections related list in the OT device record. For more information about related items and related lists for OT devices, see [Edit or view OT devices after import or discovery](view-ot-assets.md).

**Parent Topic:**[OT device related items and related lists](../reference/ot-assets-related-links-and-lists.md)

