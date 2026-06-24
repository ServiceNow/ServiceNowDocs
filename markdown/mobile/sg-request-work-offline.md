---
title: Request offline mode
description: To activate this feature, request activation of the SG Offline support plugin \(com.glide.sg.offline\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/mobile/sg-request-work-offline.html
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Offline mode, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Request offline mode

To activate this feature, request activation of the SG Offline support plugin \(com.glide.sg.offline\).

## Before you begin

**Note:** Offline mode is supported on on-premise instances.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Select **Request plugin** to open the **Activate Plugin** form on Now Support.

    \[Omitted image "request-plugin.png"\] Alt text: Admin view of the Application Manager interface with the Request plugin option highlighted.

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

 **Note:** If the system doesn't list the plugin you want or if you're activating the plugin on an OEM or on-premise instance, select the **Plugin I'm looking for is not listed** check box and then enter the name of the plugin.

</td></tr><tr id="date-time"><td>

Select Maintenance Date and Time

</td><td>

Select the date and time to activate the plugin.

</td></tr></tbody>
</table>    For example, see the following form to activate the Event Management plugin on an instance named SNC Instance.

    \[Omitted image "activate-plugin-form.png"\] Alt text: Admin view of the form requesting the Event Management plugin on a selected instance. For the text description, refer to the Activate Plugin form table.

4.  Select **Submit**.

    After the maintenance window, the system installs the plugin on your instance. To confirm the installation, go to the Installed tab in the Application Manager.


**Parent Topic:**[Offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/mobile/mobile-offline-mode.md)

**Related topics**  


[List of plugins \(Yokohama\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ai-platform-administration/list-of-plugins.md)

