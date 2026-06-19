---
title: Request the legacy Oracle Process Pack
description: The legacy Software Asset Management - Oracle Process Pack \(com.snc.sam.oracle.pp\) plugin can no longer be activated upon request. If the legacy plugin has already been activated on your ServiceNow instance, you can continue to use the legacy Oracle Process Pack.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/software-asset-management/t\_ActivateSWAssetMgmtOraclProcPac.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Legacy Oracle process pack, Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Request the legacy Oracle Process Pack

The legacy Software Asset Management - Oracle Process Pack \(com.snc.sam.oracle.pp\) plugin can no longer be activated upon request. If the legacy plugin has already been activated on your ServiceNow instance, you can continue to use the legacy Oracle Process Pack.

## Before you begin

Role required: admin

## About this task

The legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin activates all related plugins.

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


**Parent Topic:**[Legacy Oracle process pack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/software-asset-management/c_OracleProcessPack.md)

**Related topics**  


[bundle-platadm.list-of-plugins]

