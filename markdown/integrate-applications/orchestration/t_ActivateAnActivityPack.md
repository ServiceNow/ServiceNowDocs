---
title: Available activity packs
description: Activity packs are available with your subscription to Orchestration.
locale: en-US
release: yokohama
product: Orchestration
classification: orchestration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Activate Orchestration, Classic Orchestration, Data and Automation]
---

# Available activity packs

Activity packs are available with your subscription to Orchestration.

## Before you begin

Role required: admin

## About this task

The following activity packs are available and active with your Orchestration subscription:

-   [Orchestration - Active Directory](https://www.servicenow.com/docs/access?context=c_OrchActiveDirectoryActivities&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) \(com.snc.orchestration.ad\)
-   [Orchestration - Azure Active Directory](../concept/c_AzureADActivityPack.md) \(com.snc.orchestration.azure.ad\)
-   [Orchestration - Exchange](../concept/c_OrchestrationExchangeActivities.md) \(com.snc.orchestration.exchange\)
-   [Orchestration - SFTP](../concept/c_OrchestrationSFTPActivityPack.md) \(com.snc.orchestration.sftp\)
-   [Orchestration - Infoblox DDI Activity Pack](../concept/c_InfobloxDDIActivityPack.md) \(com.snc.orchestration.infoblox\)
-   [F5 Network Management activity pack](../concept/c_OrchF5LoadBalancerActivities.md) \(com.snc.orchestration.f5\)
-   [Orchestration - SSH](../concept/c_OrchestrationSSHCustomActivities.md) \(com.snc.orchestration.ssh\)
-   [Orchestration - PowerShell](../concept/c_OrchestrPwrshellActivityPack.md) \(com.snc.orchestration.powershell\)
-   [Orchestration - System Center Configuration Manager](../../../product/orchestration/task/t_ActivateSysCentrConfigMgrActiv.md) \(com.snc.orchestration.sccm\_mgnt\)

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


**Parent Topic:**[Activate Orchestration](../../../product/orchestration/task/t_ActivateOrchestration.md)

