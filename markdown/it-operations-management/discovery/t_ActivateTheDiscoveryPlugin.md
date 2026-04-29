---
title: Request Discovery
description: Request and activate the Discovery \(com.snc.discovery\) plugin to enable Discovery capabilities on your instance.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Request Discovery

Request and activate the Discovery \(com.snc.discovery\) plugin to enable Discovery capabilities on your instance.

## Before you begin

To purchase a Discovery subscription, contact your ServiceNow account manager or sales representative.

Role required: admin

## About this task

Discovery is available as a separate subscription from the rest of the ServiceNow AI Platform and requires the Discovery \(com.snc.discovery\) plugin. When the Discovery plugin is activated, several plugins and applications are also installed. For more information, see [Plugins or applications installed with ITOM Visibility](../../it-operations-management/reference/plugin-app-itom-visibility.md). For additional details about plugins, see [Requesting a Plugin from the Service Catalog \[KB0751715\] article in the Now Support Knowledge Base.](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0751715)

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

 **Note:** If the system doesn't list the plugin you want or if you're activating the plugin on an OEM or on-premise instance, select the **Plugin I'm looking for is not listed** check box and then enter the name of the plugin.

</td></tr><tr id="date-time"><td>

Select Maintenance Date and Time

</td><td>

Select the date and time to activate the plugin.

</td></tr></tbody>
</table>    For example, see the following form to activate the Event Management plugin on an instance named SNC Instance.

4.  Select **Submit**.

    After the maintenance window, the system installs the plugin on your instance. To confirm the installation, go to the Installed tab in the Application Manager.


**Related topics**  


[Discovery setup](../concept/discovery-setup.md)

[Discovery monitoring and issue resolution](../concept/c_DiscoveryTroubleshooting.md)

