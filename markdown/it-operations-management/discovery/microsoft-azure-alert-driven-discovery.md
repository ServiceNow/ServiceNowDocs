---
title: Microsoft Azure Alert driven discovery
description: The Microsoft Azure Alert service can raise alerts for any changes in the life-cycle state or the configuration of a cloud resource. You can configure the service to auto-update the latest resource information in the Configuration Management Database \(CMDB\) without waiting for the next scheduled Cloud Discovery to run. Configure the Microsoft Azure Alert service to auto-update the Configuration Management Database \(CMDB\) without waiting for the next scheduled Cloud Discovery to run.Enable alert-driven discovery for a new Microsoft Azure alert type by adding it to the Azure Alert Rules \[azure\_alert\_rule\] table.The base system Cloud Discovery supports alert driven discovery for several Microsoft Azure alert types. The Azure Alert Rules \[azure\_alert\_rule\] table contains the supported alert types.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Azure Cloud Discovery, Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Microsoft Azure Alert driven discovery

The Microsoft Azure Alert service can raise alerts for any changes in the life-cycle state or the configuration of a cloud resource. You can configure the service to auto-update the latest resource information in the Configuration Management Database \(CMDB\) without waiting for the next scheduled Cloud Discovery to run.

**Important:** The Azure change processing offers an optimal performance when compared to the Microsoft Azure alert-driven discovery that uses a legacy form of authentication and should no longer be used. Starting with the Discovery and Service Mapping Patterns app version 1.1.0, the Azure change processing has replaced the Microsoft Azure alert-driven discovery. Use the new secure webhook or migrate to [Azure change processing](azure-change-processing.md) for additional performance gains. For more information, see on the secure webhook, see the knowledge base article [Azure Alert service to auto-update the CMDB has webhook url without credentials in the azure portal](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=1bf707c5938fe550d9743f986cba10b9).

During event processing, the Cloud Event Scheduler identifies the domain of the service account and assigns to the event. If an error occurs in identifying the domain before processing, the event can sometimes stay unassigned and become visible to all domains. To prevent the failed events visibility to all domains, you can set the **sn\_cmp.error\_events.default\_domain** property to sys\_id of the service-provider domain so that the failed events appears only to the service-provider domain administrator.

You can configure the Cloud Event Scripted REST API to receive alerts from the Microsoft Azure Alert service. For each alert—also called an event—the API creates a record in the Cloud Events \[sn\_cmp\_cloud\_event\] table. The Cloud Event Scheduler reads the events from the \[sn\_cmp\_cloud\_event\] table for batch processing. The scheduler invokes the pattern to process the events that are in ready state. The patterns discover the affected resource and add or update its details in the CMDB. This method helps to update the CMDB Configuration Item \(CI\) data and view the latest data in the Cloud User portal.

**Important:** If you're using domain separation for Cloud Discovery, the events are also domain-separated. Therefore, you can view the details of a processed event only if it belongs to your domain. If an event is not associated with any service account, then it is associated with the global domain.

For each event, the Cloud Event Scripted REST API stores the following information \[sn\_cmp\_cloud\_event\] table:

-   **Source**: This field is always set to `azure activity log`.
-   **Event Name**: Name of the event received from the Microsoft Azure console.
-   **Resource ID**: ID of the affected resource. If there are VM events, Cloud Discovery uses this information to identify the VM.
-   **Resource Type**: Resource type of the affected resource.

## Configure the Microsoft Azure Alert service to auto-update the CMDB

 Configure the Microsoft Azure Alert service to auto-update the Configuration Management Database \(CMDB\) without waiting for the next scheduled Cloud Discovery to run.

### Before you begin

-   Ensure that either Discovery or Cloud Provisioning and Governance is activated in the instance.
-   -   An active MID Server with Microsoft Azure discovery capability is available.

    **Note:** The alert configuration continues to ping alerts even when the MID Server is down. Which in turn leads to a high number of errors in the ECC queue. If no MID Server is available, you must manually deactivate the Microsoft Azure alert rule. The Azure Alert Rules \[azure\_alert\_rule\] table contains all the Microsoft Azure alert rules.


Role required:

-   ServiceNow role: sn\_cmp.cloud\_event\_integration
-   Microsoft Azure roles:

    -   Microsoft Azure credentials with the Reader role
    -   Microsoft Azure custom role with the following permissions:

        ```
        "permissions": [
                    {
                        "actions": [
                            "Microsoft.Insights/ActionGroups/Write",
                            "Microsoft.Insights/ActionGroups/Delete",
                            "Microsoft.Insights/ActionGroups/Read",
                            "Microsoft.Insights/ActivityLogAlerts/Write",
                            "Microsoft.Insights/ActivityLogAlerts/Delete",
                            "Microsoft.Insights/ActivityLogAlerts/Read",
                            "Microsoft.Insights/ActivityLogAlerts/Activated/Action",
                            "Microsoft.Insights/AlertRules/Write",
                            "Microsoft.Insights/AlertRules/Delete",
                            "Microsoft.Insights/AlertRules/Read",
                            "Microsoft.Resources/deployments/write",
                            "Microsoft.Resources/deployments/delete",
                            "Microsoft.Resources/deployments/read"
                        ],
        ```

    **Note:** To set up the alert-driven discovery, you can use a Microsoft Azure service principal with the reader role only. For more information, see the community article [Azure alert driven discovery with reader privileges](https://community.servicenow.com/community?id=community_article&sys_id=32edaa41db2fa090679499ead39619a1).


### About this task

After you configure the alert service, it facilitates tracking of the life-cycle state and configuration of the Microsoft Azure cloud resources.

**Important:** You can use a secure webhook to forward the Microsoft Azure alerts to the ServiceNow AI Platform. For more information, see [Use a secure webhook to forward the Microsoft Azure alerts to the ServiceNow AI Platform \[KB1208357\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1208357).

### Procedure

1.  Disable authentication for the Cloud Event Scripted REST API, because the Microsoft Azure Alert doesn't support basic authentication.

    1.  As an administrator, navigate to **Scripted Web Services** &gt; **Scripted REST APIs**.

    2.  Open the Cloud Event record.

    3.  From the **Resources** tab, open the Cloud Config Event Post record.

    4.  Set the application scope to **Global**.

    5.  On the **Security** tab, clear the **Requires Authentication** check box.

        **Important:** The ServiceNow instance uses a webhook URL for the alert-driven discovery. However, the Microsoft Azure alert configuration of the ServiceNow instance doesn't support authentication for creating the webhook. You can enable authentication by providing the user name and password in the webhook URL. For more information, see [KB0963526](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0963526).

2.  Navigate to **Discovery** &gt; **Cloud Alerts** &gt; **Azure Alert Configurations**.

    **Note:** If you have Discovery activated in the instance, you can navigate directly to **Alert Configurations** using your instance URL. For example,

    ```
    https://{instancename}.service-now.com/sn_cmp_azure_alert_configuration_list.do
    ```

3.  On the **Azure** tab, select **New**.

4.  On the form, fill in the fields.

<table id="table_dw1_vs1_qz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service Account

</td><td>

Microsoft Azure service account for which you want to create the Azure alert configuration.Make sure that Cloud Discovery has discovered all the Logical Datacenters \(LDC\) associated with the cloud account.

</td></tr><tr><td>

Resource Group

</td><td>

Resource group that contains the alert rules. Select the Microsoft Azure service account. For more information on adding a Microsoft Azure service account, see [Add an Azure service account](../../cloud-management-v2-setup/task/azure-service-account-cloud-mgt.md).

 The instance creates the alert rules for all the resources that are available in the service account.

</td></tr><tr><td>

Activate

</td><td>

Option to indicate the status of the alert configuration.This option is selected by default.

</td></tr><tr><td>

User

</td><td>

User name of a ServiceNow user having the sn\_cmp.cloud\_event\_integration role.

</td></tr><tr><td>

Password

</td><td>

ServiceNow user account password.

</td></tr></tbody>
</table>5.  Select **Submit**.

    On successfully configuring the Microsoft Azure Alert service, the status of the alert configuration changes from **None** to **Activated**.


## Add a Microsoft Azure alert rule

Enable alert-driven discovery for a new Microsoft Azure alert type by adding it to the Azure Alert Rules \[azure\_alert\_rule\] table.

### Before you begin

Role required: admin

### About this task

The Azure Alert Rules \[azure\_alert\_rule\] table contains all the supported alert types. For more information, see [Supported Microsoft Azure alert types](microsoft-azure-alert-driven-discovery.md#). The Microsoft Azure Alert service uses the information stored in the Azure Alert Rules \[azure\_alert\_rule\] table to raise the alerts. Cloud Discovery also supports all the alerts generated for the members of the resource group specified in the Microsoft Azure alert configuration.

### Procedure

1.  Navigate to the Azure Alert Rules \[azure\_alert\_rule\] table by entering the following URL in the navigation bar of the browser:

    `https://<instance name>.service-now.com/azure_alert_rule_list.do`

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_rgb_cff_15b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Rule name

</td><td>

Name of the Microsoft Azure alert type.

</td></tr><tr><td>

Action

</td><td>

Microsoft Azure resource operation API path.For more information on the Microsoft Azure resources for which you can raise alerts, go to the [Microsoft Azure](https://docs.microsoft.com/en-us/azure/?product=popular) documentation and see "Azure resource provider operations".

</td></tr><tr><td>

Active

</td><td>

Option to indicate the status of the Microsoft Azure alert type.This option is selected by default.

</td></tr></tbody>
</table>4.  Select **Submit**.


## Supported Microsoft Azure alert types

The base system Cloud Discovery supports alert driven discovery for several Microsoft Azure alert types. The Azure Alert Rules \[azure\_alert\_rule\] table contains the supported alert types.

The base system Cloud Discovery supports the following Microsoft Azure alert types:

```
Microsoft.Compute/virtualMachines/deallocate/action 
Microsoft.Network/privateDnsZones/delete 
Microsoft.Compute/availabilitySets/write 
Microsoft.Network/loadBalancers/write 
Microsoft.Network/connections/delete 
Microsoft.Network/publicIPAddresses/delete 
Microsoft.Storage/storageAccounts/write 
Microsoft.Network/virtualNetworks/delete 
Microsoft.Sql/servers/databases/delete 
Microsoft.Network/expressRouteCircuits/write 
Microsoft.Network/localnetworkgateways/delete 
Microsoft.Network/networkInterfaces/delete 
Microsoft.Compute/virtualmachines/write 
Microsoft.Network/expressRouteCircuits/delete 
Microsoft.Network/natGateways/write 
Microsoft.Network/loadBalancers/delete 
Microsoft.Compute/virtualMachineScaleSets/delete 
Microsoft.Network/virtualNetworks/virtualNetworkPeerings/delete 
Microsoft.Storage/storageAccounts/delete 
Microsoft.Compute/availabilitySets/delete 
Microsoft.Network/connections/write 
Microsoft.Compute/virtualMachines/start/action 
Microsoft.Compute/virtualMachines/restart/action 
Microsoft.Sql/servers/databases/write 
Microsoft.Compute/virtualMachines/delete 
Microsoft.Network/networkInterfaces/write 
Microsoft.Network/privateDnsZones/write 
Microsoft.Network/localnetworkgateways/write 
Microsoft.Network/natGateways/delete 
Microsoft.Compute/virtualMachines/stop/action 
Microsoft.Network/publicIPAddresses/write 
Microsoft.Compute/virtualMachineScaleSets/write 
Microsoft.Network/virtualNetworks/virtualNetworkPeerings/write 
Microsoft.Network/virtualNetworks/write 
Microsoft.Sql/servers/delete 
Microsoft.Sql/servers/write 
```

