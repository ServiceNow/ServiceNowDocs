---
title: Request client software distribution
description: Client software distribution requires the Orchestration - Client Software Distribution plugin \(com.snc.orchestration.client\_sf\_distribution\), which is available by request with a subscription to Orchestration.
locale: en-US
release: yokohama
product: Orchestration
classification: orchestration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Client Software Distribution, Orchestration applications, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Request client software distribution

Client software distribution requires the Orchestration - Client Software Distribution plugin \(com.snc.orchestration.client\_sf\_distribution\), which is available by request with a subscription to Orchestration.

## Before you begin

Role required: admin

## About this task

The Orchestration - Client Software Distribution plugin activates the [Orchestration - System Center Configuration Manager](t_ActivateSysCentrConfigMgrActiv.md) plugin that contains the custom SCCM activities used to deploy or revoke software using an SCCM server. For additional plugin dependencies, see [Plugins installed with client software distribution](../reference/r_IWClientSWDist.md#).

**Note:** The Orchestration - Client Software Distribution plugin runs in its own application scope.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Select **Request plugin** to open the **Activate Plugin** form on Now Support.

    ![Admin view of the Application Manager interface with the Request plugin option highlighted.](../../../reuse/images/request-plugin.png)

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

    ![Admin view of the form requesting the Event Management plugin on a selected instance. For the text description, refer to the Activate Plugin form table.](../../../reuse/images/activate-plugin-form.png "Completed Activate Plugin form")

4.  Select **Submit**.

    After the maintenance window, the system installs the plugin on your instance. To confirm the installation, go to the Installed tab in the Application Manager.


**Parent Topic:**[Client Software Distribution](../concept/c_ClientSoftwareDistribution.md)

