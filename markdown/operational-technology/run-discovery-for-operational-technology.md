---
title: Create an OT Discovery schedule and run the Discovery process
description: Define Operational Technology \(OT\) Discovery schedules that orchestrate how and when the Discovery for an OT function should run. You can also perform an immediate Quick Discovery or an actual OT Discovery run.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [IT Discovery for Operational Technology \(OT\) Networks, Operational Technology Discovery, Operational Technology]
---

# Create an OT Discovery schedule and run the Discovery process

Define Operational Technology \(OT\) Discovery schedules that orchestrate how and when the Discovery for an OT function should run. You can also perform an immediate Quick Discovery or an actual OT Discovery run.

## Before you begin

Do the following actions before you run IT Discovery for OT Networks:

-   Install and configure the standard Discovery application. To learn more, see [Discovery setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/discovery-setup.md).
-   Install the CMDB CI Class Models plugin. To learn more, see [Operational Technology \(OT\) extension classes installation](install-operation-technology-ot-extension-classes.md).
-   Install the Mid Server. To learn more, see [Installing the MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-installation.md).

Role required: ot\_discovery\_admin

## Procedure

1.  Navigate to **All** &gt; **OT Discovery** &gt; **OT Discovery Schedules**.

2.  Run Quick Discovery or select or create an OT discovery schedule.

<table id="choicetable_dcf_hl5_vpb"><thead><tr><th align="left" id="d26525e142">

Task

</th><th align="left" id="d26525e145">

Description

</th></tr></thead><tbody><tr><td id="d26525e151">

**Run an immediate Quick Discovery**

</td><td>

Click **Quick Discovery** and do the following actions:1.  In the **Target IP** field, enter the IP address in which the Discovery for the OT process should run.
2.  In the **MID Server** field, select the MID Server in which the Discovery process should run.
3.  Click **OK**.


</td></tr><tr><td id="d26525e193">

**Select or create an OT discover schedule**

</td><td>

1.  Select an existing OT discovery schedule or click **New** to create a new one.
2.  Perform the steps that follow to create the OT discovery schedule record in the OT Discovery Schedule form.


</td></tr></tbody>
</table>3.  In the form, fill in the OT Discovery Schedule fields.

<table id="choicetable_fxf_qpx_nsb"><thead><tr><th align="left" id="d26525e226">

Field

</th><th align="left" id="d26525e229">

Description

</th></tr></thead><tbody><tr><td id="d26525e235">

**Name**

</td><td>

Unique, descriptive name for your OT discovery schedule.

</td></tr><tr><td id="d26525e244">

**Discover**

</td><td>

Scan type for the OT discovery schedule.-   **Configuration items**

Uses Discovery identifiers to match devices with configuration items \(CIs\) in the CMDB and to update the CMDB. Perform a simple discovery by selecting a specific MID Server to scan for all protocols \(SSH, WMI, and SNMP\) or perform advanced discoveries with discovery behaviors. When you select a behavior, the MID Server field is not available.

-   **IP addresses**

Scans devices without the use of credentials. These scans discover all the active IP addresses in the specified range and create device history records, but do not update the CMDB. IP address scans also show multiple IP addresses that are running on a single device. Identify devices by class and by type, such as Windows computers and Cisco network gear.

</td></tr><tr><td id="d26525e296">

**Default Purdue level**

</td><td>

Purdue level that you want the OT discovery schedule to run in or select **--None--** for all Purdue levels.**Note:** To learn more about Purdue levels, see [https://subscription.packtpub.com/book/networking\_and\_servers/9781788395151/1/ch01lvl1sec10/the-purdue-model-for-industrial-control-systems](https://subscription.packtpub.com/book/networking_and_servers/9781788395151/1/ch01lvl1sec10/the-purdue-model-for-industrial-control-systems).

</td></tr></tbody>
</table>    Most of the fields on this form are identical to or operate in the same manner as the standard Discovery form. Only those fields that differ from the standard Discovery scheduling appear in this topic. To learn more about the remaining fields, see [Schedule a horizontal discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/t_CreateADiscoverySchedule.md)

4.  Run the Discovery process right away, or save the OT discovery schedule to run at the times you designated in the record.

    |Task|Description|
    |----|-----------|
    |**Run Discovery immediately**|Click the **Discover now** related link.|
    |**Run Discovery at the time designated in the OT discovery schedule**|Click **Update**.|


## Result

When the IT Discovery for OT Networks process runs, it creates a history record in the Discovery Status related list.

