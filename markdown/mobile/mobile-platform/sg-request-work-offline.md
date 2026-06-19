---
title: Request offline mode
description: Activate offline mode for mobile by requesting the activation of the SG Offline support plugin \(com.glide.sg.offline\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/mobile-platform/sg-request-work-offline.html
release: australia
product: Mobile Platform
classification: mobile-platform
topic_type: task
last_updated: "2026-06-09"
reading_time_minutes: 1
breadcrumb: [Install and enable, Offline mode setup options, Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Request offline mode

Activate offline mode for mobile by requesting the activation of the SG Offline support plugin \(com.glide.sg.offline\).

## Before you begin

**Note:** Offline mode is supported on on-premise instances.

Role required: mobile\_admin, admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Select **Request plugin** to open the **Activate Plugin** form on Now Support.

3.  On the **Activate Plugin** form, provide the following information.

<table id="table_awx_bhf_ygb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr id="target-instance"><td>

What is your target instance

</td><td>

Select the instance that you want to activate the plugin on.

</td></tr><tr><td>

Which plugin would you like to activate

</td><td>

Select the name of the plugin to activate.

 **Note:** If the plugin isn't listed, or if you're activating on an OEM or on-premise instance, select the **Plugin I'm looking for is not listed** check box. Enter the plugin name in the field that appears.

</td></tr><tr id="date-time"><td>

Select Maintenance Date and Time

</td><td>

Select the date and time to activate the plugin.

</td></tr></tbody>
</table>    For example, see the following form to activate the Event Management plugin on an instance named SNC Instance.

4.  Select **Submit**.

    After the maintenance window, the system installs the plugin on your instance. To confirm the installation, go to the Installed tab in the Application Manager.


**Parent Topic:**[Install and enable offline capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/enable-offline.md)

**Related topics**  


[bundle-platadm.list-of-plugins]

