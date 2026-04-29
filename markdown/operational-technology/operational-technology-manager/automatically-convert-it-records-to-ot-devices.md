---
title: Automatically convert your IT records to OT devices
description: Create a scheduled job that automatically converts your IT hardware to Operational Technology \(OT\) devices by using the Bulk Update Ruleset for Reassigning IT to OT feature. This scheduled job adds OT entity details to all the IT hardware that you want to convert at once.
locale: en-US
release: australia
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Use, Operational Technology Manager, Operational Technology]
---

# Automatically convert your IT records to OT devices

Create a scheduled job that automatically converts your IT hardware to Operational Technology \(OT\) devices by using the Bulk Update Ruleset for Reassigning IT to OT feature. This scheduled job adds OT entity details to all the IT hardware that you want to convert at once.

## Before you begin

Role required: admin or cmdb\_ot\_admin

## About this task

You may have configuration items \(CIs\) classed as IT hardware that you want to create OT entity records for. Follow these general guidelines:

-   Make sure that the fields you use apply to the filter criteria conditions in steps 3 to 4. Verify that the data set doesn’t exceed 1 million records so that you can avoid performance-related issues.
-   Create separate scheduled job definitions for the separate CI classes in steps 3 to 6. This way, you can filter each CI level and define the OT entity default values.
-   Use the Class field in the filter to query only specific CI classes in step 3.

    **Note:** Only the hardware class and its extended classes are used in the source table.

-   Use the **Preview** button to verify the records selected for further review in step 4.
-   Verify the data in the **OT Entity Default Configuration** tab in step 5. The OT entity records are created using these default values.

You can also manually convert the IT hardware to the OT devices. For more information, see [Convert IT hardware to OT devices in a bulk edit](bulk-edit-to-convert-it-records-into-ot-records.md).

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace Admin** &gt; **OT Manager Admin** &gt; **Automated IT OT Bulk Contextualization**.

2.  Select **New**.

3.  On the **Filter Criteria - OT Devices** tab, set the source table and filter criteria to identify the CIs that you need to convert.

    For example, if you want to add the OT entity details for all computers that are imported into the system that have a prefix of COMP, select the source table as **cmdb\_ci\_computer** and then add the filter criteria as **\[Name\] \[starts with\] \[COMP\]**, **\[Class\] \[is\] \[Computer\]**, and **\[OT device details\] \[is empty\]**.

    You can also use CMDB groups to group IT CIs based on additional information, such as Software Installed, so that you can convert them to OT devices. For more information, see [Use CMDB groups to add OT context to IT CIs](use-cmdb-groups-it-ot-conversion.md).

    **Note:** If you're using a CMDB group, the **Filter Criteria - OT Devices** tab shown in this step isn't visible.

4.  Verify the number of records that were chosen from the filter condition you set by selecting the **Preview** button.

    The OT entity details are added for these records, such as OT Device Type and Device Criticality.

5.  On the **OT Entity Default Configuration** tab, fill in the fields.

    The fields in the following table provide the default values that are added to the OT entity records or the OT-related metadata.

<table id="table_ntp_yzn_qxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

OT Device Type

</td><td>

Category type that the OT device is classified as. The device type is also the function that the device plays on the OT network. For example, an IT device, such as a server, can be converted to an OT device, and the function it plays on the network is an HMI. Its class is server and its device type is HMI.

 **Note:** In some cases, OT devices have no OT function or the device type is unknown. Where the OT devices have no OT function, select **No OT Function**. Where the OT devices have an unknown device type, select **Unknown**.

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

Area within the site location that the device is assigned to.

</td></tr><tr><td>

Site

</td><td>

Top-level parent entity, or industrial site, where the device is located or assigned to.

</td></tr></tbody>
</table>6.  In the **Run** field, select a scheduled time for this job to run.

7.  Select the check box next to the **Active** field.

8.  Select **Submit**.

9.  To run the job immediately, select **Execute Now** in the record.

    When you select **Execute Now**, a confirmation modal is shown to ensure you want to create OT entity records from the table specified in the **Filter Criteria - OT Devices** tab. For example if you're creating a scheduled job for the source table cmdb\_ci\_computer, you will see the following message:

    This action will trigger the scheduled job which creates OT entity records for 3 records from "cmdb\_ci\_computer" table as per the query condition. Are you sure to want to proceed?

10. Select **Proceed**.


**Parent Topic:**[Using the Operational Technology Manager](../concept/using-operational-technology-manager.md)

