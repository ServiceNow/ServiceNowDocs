---
title: Operational Technology device form
description: Use the Operational Technology \(OT\) device form to edit the detailed information for the OT devices in your enterprise.
locale: en-US
release: zurich
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [OT device related items and related lists, Edit or view OT devices after import or discovery, Use, Operational Technology Manager, Operational Technology]
---

# Operational Technology device form

Use the Operational Technology \(OT\) device form to edit the detailed information for the OT devices in your enterprise.

<table id="table_plx_mm1_vxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

OT display name

</td><td>

The name of the OT device displayed in the record.**Note:** You can add any string value to this field. Multiple devices can have the same OT display name. This is meant for easier understanding of the OT device and is different from the unique CI name generated when you import OT devices from the staging table.

</td></tr><tr><td>

OT device type

</td><td>

The category type that the OT device is classified as. The device type is also the function that the device plays on the OT network. For example:

 An IT device, such as a server, can be converted to an OT device, and the function it plays on the network is an HMI. Therefore, its class is **server** and its device type is **HMI**.

 **Note:** In some cases, there are OT devices with no OT function or OT devices where the device type is unknown. For OT devices with no OT function, select **No OT Function**. For OT devices where the device type is unknown, select **Unknown**.

</td></tr><tr><td>

Device criticality

</td><td>

The measure of the relative risk to the site process of failure of the device. For example:-   1 - Most critical
-   4 - Not critical

</td></tr><tr><td>

Site

</td><td>

The top-level parent entity, or industrial site, where the device is located or assigned to.

</td></tr><tr><td>

Purdue level

</td><td>

The assigned Purdue level. Ranges 0–5. **Note:** To learn more about Purdue levels in Industrial Control Systems, see [https://subscription.packtpub.com/book/networking\_and\_servers/9781788395151/1/ch01lvl1sec10/the-purdue-model-for-industrial-control-systems](https://subscription.packtpub.com/book/networking_and_servers/9781788395151/1/ch01lvl1sec10/the-purdue-model-for-industrial-control-systems).

</td></tr><tr><td>

Zone

</td><td>

The area within the site location that the device is assigned to.

</td></tr><tr><td>

Class

</td><td>

The name of the assigned class for the OT device.**Note:** For a listing and explanation of CI classes, see [Operation Technology \(OT\) extension classes](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models-operation-technology&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Status

</td><td>

Status of the OT device:-   **--None--**

No assigned status.

-   **Absent**

OT device is absent in your facilities.

-   **In Maintenance**

OT device is in maintenance and currently is off line.

-   **In stock**

OT device is in stock in your facilities.

-   **Installed**

OT device is installed in your facilities.

-   **Pending Install**

OT device is pending installation in your facilities.

-   **Pending repair**

OT device is pending repair but is not online yet.

-   **Retired**

OT device is retired.

-   **Stolen**

OT device has been stolen.


</td></tr><tr><td>

Discovery source

</td><td>

The Discovery source for the OT device data. For example, SG-OT Excel Import, if you imported the OT device from a Microsoft Excel spreadsheet using the Integration Hub ETL. To learn more, see [Service Graph Connector for Microsoft Excel](../concept/service-graph-connector-for-OT-excel.md).

</td></tr><tr><td>

Infrastructure Relationships

</td><td>

Shows the relationship of OT device with other the OT devices and the equipment model entities.

</td></tr><tr><td>

Service Relationships

</td><td>

Shows the relationship of OT device with the equipment model entities.

</td></tr><tr><td>

CI Timeline

</td><td>

Shows the timeline of OT incidents, OT change, and audit history associated with the OT device.

</td></tr><tr><td colspan="2">

The following fields only apply to the Programmable Logic Controller \(PLC\) Class Records:

</td></tr><tr><td>

Key switch

</td><td>

The Key switch modes:-   **Remote mode**

You can change the configuration of the PLC.

-   **Local mode**

By default mode, you can’t change the configuration of the PLC.


</td></tr><tr><td>

Switch position

</td><td>

The Switch position of the PLC has the following positions:-   **Run**
-   **Program**
-   **Remote**
-   **Stop**
-   **Test**

 By default, the switch position is set to **None**.

 When the switch position is set to **Remote**, the Switch remote modes are enabled.

</td></tr><tr><td>

Switch remote mode

</td><td>

The Switch remote of the PLC has the following modes:-   **Run**
-   **Program**
-   **Test**
-   **None**

</td></tr><tr><td>

Asset

</td><td>

When configuration items \(CIs\) are created in the Configuration Management Database \(CMDB\), asset records are created. The asset record contains the model category of the CI. For more information about the model categories for Operational Technology \(OT\), see [Model categories for Operational Technology](model-categories-for-ot.md). To view the model category for an OT device, complete the following:1.  Navigate to **All** &gt; **Operational Technology \(OT\)** &gt; **All OT Devices**.
2.  Select the OT device that you want to view the asset record for.
3.  Next to the **Asset** field, select the **Preview this record** \(![Preview this record icon](../image/preview-record-icon.png)\) icon.
4.  Select **Open Record**.

</td></tr><tr><td colspan="2">

The following fields only apply to the following class records.-   OT Supervisory System
-   OT Control System
-   OT Field Device
-   Unclassed OT Device

</td></tr><tr><td>

Is Virtual

</td><td>

If selected, indicates that the OT device is virtual.

</td></tr></tbody>
</table>**Parent Topic:**[OT device related items and related lists](ot-assets-related-links-and-lists.md)

