---
title: Available activity packs
description: Activity packs are available with your subscription to Orchestration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/orchestration/t\_ActivateAnActivityPack.html
release: australia
product: Orchestration
classification: orchestration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Activate Orchestration, Classic Orchestration, Workflow Data Fabric]
---

# Available activity packs

Activity packs are available with your subscription to Orchestration.

## Before you begin

Role required: admin

## About this task

The following activity packs are available and active with your Orchestration subscription:

-   Orchestration - Active Directory \(com.snc.orchestration.ad\)
-   [Orchestration - Azure Active Directory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/orchestration/c_AzureADActivityPack.md) \(com.snc.orchestration.azure.ad\)
-   [Orchestration - Exchange](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/orchestration/c_OrchestrationExchangeActivities.md) \(com.snc.orchestration.exchange\)
-   [Orchestration - SFTP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/orchestration/c_OrchestrationSFTPActivityPack.md) \(com.snc.orchestration.sftp\)
-   [Orchestration - Infoblox DDI Activity Pack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/orchestration/c_InfobloxDDIActivityPack.md) \(com.snc.orchestration.infoblox\)
-   [F5 Network Management activity pack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/orchestration/c_OrchF5LoadBalancerActivities.md) \(com.snc.orchestration.f5\)
-   [Orchestration - SSH](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/orchestration/c_OrchestrationSSHCustomActivities.md) \(com.snc.orchestration.ssh\)
-   [Orchestration - PowerShell](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/orchestration/c_OrchestrPwrshellActivityPack.md) \(com.snc.orchestration.powershell\)
-   [Orchestration - System Center Configuration Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/orchestration/t_ActivateSysCentrConfigMgrActiv.md) \(com.snc.orchestration.sccm\_mgnt\)

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


**Parent Topic:**[Activate Orchestration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/orchestration/t_ActivateOrchestration.md)

