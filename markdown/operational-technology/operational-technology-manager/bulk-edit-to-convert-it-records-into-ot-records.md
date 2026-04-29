---
title: Convert IT hardware to OT devices in a bulk edit
description: Choose multiple IT hardware devices and convert them to OT devices in a bulk edit so that you can edit your records more quickly and efficiently.
locale: en-US
release: australia
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [OT device related items and related lists, Edit or view OT devices after import or discovery, Use, Operational Technology Manager, Operational Technology]
---

# Convert IT hardware to OT devices in a bulk edit

Choose multiple IT hardware devices and convert them to OT devices in a bulk edit so that you can edit your records more quickly and efficiently.

## Before you begin

Role required: cmdb\_ot\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace Admin** &gt; **Industrial Workspace**.

2.  In the Industrial Workspace, navigate to the All IT Hardware list.

3.  If you want to filter the All IT Hardware list, do the following actions:

    -   Select the filter ![Filter icon.](../../mftg-manufacturing-process-mgr/image/filter-list-icon.png) icon.
    -   Add the filter that you want applied to the list.
    -   Select **Update**.
4.  Select the check box next to each of the IT hardware devices that you want to convert.

    If you want to select all IT hardware devices in the list, select the check box next to the Name column.

5.  Select the **Convert to OT devices** button.

6.  On the form, fill in the fields.

<table id="table_ntp_yzn_qxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

OT Device Type

</td><td>

The category type that the OT device is classified as. The device type is also the function that the device plays on the OT network. For example:

 An IT device, such as a server, can be converted to an OT device, and the function it plays on the network is an HMI. Therefore, its class is **server** and its device type is **HMI**.

 **Note:** In some cases, there are OT devices with no OT function or OT devices where the device type is unknown. For OT devices with no OT function, select **No OT Function**. For OT devices where the device type is unknown, select **Unknown**.

</td></tr><tr><td>

Device Criticality

</td><td>

Measure of the relative risk to the site process if the device fails:-   1 - Most critical
-   4 - Not critical


</td></tr><tr><td>

Purdue Level

</td><td>

Assigned Purdue level. The level ranges are 0–5.

**Note:** To learn more about the Purdue levels in Industrial Control Systems, see [https://subscription.packtpub.com/book/networking\_and\_servers/9781788395151/1/ch01lvl1sec10/the-purdue-model-for-industrial-control-systems](https://subscription.packtpub.com/book/networking_and_servers/9781788395151/1/ch01lvl1sec10/the-purdue-model-for-industrial-control-systems).

</td></tr><tr><td>

Zone

</td><td>

area within the site location that the device is assigned to.

</td></tr><tr><td>

Site

</td><td>

Top-level parent entity, or industrial site, where the device is located or assigned to.

</td></tr></tbody>
</table>7.  Select **Convert**.

    A banner appears to notify that the process has started. To check the All OT Devices list for updates, you can select the link in the banner.


## Result

The selected IT hardware devices have been converted into OT devices.

You can also use the Bulk Update Ruleset for Reassigning IT to OT feature to create a scheduled job that automatically converts IT hardware to OT devices. For more information, see [Automatically convert your IT records to OT devices](automatically-convert-it-records-to-ot-devices.md).

**Parent Topic:**[OT device related items and related lists](../reference/ot-assets-related-links-and-lists.md)

