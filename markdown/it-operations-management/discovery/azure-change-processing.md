---
title: Azure change processing
description: The Azure change processing feature collects information about Microsoft Azure resources that have undergone a life-cycle state change or configuration change near real time. Then, it uses the collected information to update the Configuration Management Database \(CMDB\).
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [Azure, CMDB, ITOM]
breadcrumb: [Discovery for Microsoft Azure, Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Azure change processing

The Azure change processing feature collects information about Microsoft Azure resources that have undergone a life-cycle state change or configuration change near real time. Then, it uses the collected information to update the Configuration Management Database \(CMDB\).

The Azure Change Processing scheduled jobs query the Azure API and collect the resource change information. During each execution cycle, the scheduled job collects information about all the resources that have changed after the last Azure Change Processing cycle. After collecting the change information, the Azure Change Processing uses response mappings to update the change information in the CMDB. During the next discovery, Cloud Discovery triggers appropriate patterns, if available, and populates detailed resource information in the CMDB.

By default, the Azure change processing scheduled jobs run in every 5 minutes. If necessary, update the execution frequency of the schedule according to your needs. Set the execution frequency within the minimum value of one minute.

When you execute the Azure change processing for the first time, it may run a few hours due to processing resource changes that occurred in the last four hours. If you want to increase the default schedule execution period, ensure that enough worker nodes are available to execute the schedule.

During event processing, the Cloud Event Scheduler identifies the domain of the service account and assigns to the event. If an error occurs in identifying the domain before processing, the event can sometimes stay unassigned and become visible to all domains. To prevent the failed events visibility to all domains, you can set the **sn\_cmp.error\_events.default\_domain** property to sys\_id of the service-provider domain so that the failed events appears only to the service-provider domain administrator.

**Note:**

Azure change processing can fetch resource change information only from the service accounts created by the discovery\_admin or sn\_cmp.cloud\_admin.

Update your Discovery and Service Mapping Patterns plugin on ServiceNow Store to have at least 1.21.0 version of Azure Change Processing. See the upgrade scenario in [KB1705862](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1705862)

Starting in the Discovery and Service Mapping Patterns 1.21.0 version, the scheduled jobs were enhanced and renamed:

-   The **Azure Process Changes** scheduled job was renamed as **ACP Pull Changes**.
-   The **CPG Build Azure Changes IRE Payload** scheduled job was renamed as **ACP Process Changes**.

## ACP tables

Starting with Discovery and Service Mapping Patterns 1.21.0 version, Azure change processing enhancement populates the following tables:

-   **ACP Resource Type \[sn\_itom\_pattern\_acp\_supported\_resource\_types\]**

    You can use this table to review all supported resource types, add a resource type for change processing, and disable or enable the processing for a certain resource.

    For more information on adding support for an Azure resource type, see [Add change processing support for an Azure resource type](../task/add-change-processing-support-azure-resource-type.md).

    Key fields:

    -   Resource Type.
    -   Query: The resource graph query that retrieves changes from Azure.
    -   Active: Indicates if the resource type is actively being queried.
-   **ACP Order Status \[sn\_itom\_pattern\_acp\_order\_status\]**

    This table tracks the status of the Azure Resource Graph query for each resource type, based on the associated credentials that are used for querying Azure. You can use this table to review the processing status. For more information about the query, see [KB1705862](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1705862).

    Key fields:

    -   Resource Type.
    -   Credential: the specific credential used for pulling changes.
    -   Last Processed time.
    -   Status: Tracks the success or failure of the event pull process. After the next ACP Pull Changes scheduled job, this status will be updated based on the CMP Order status.
    -   CMP Order: Reference to the CMP Order \[sn\_cmp\_order\] field, which provides details about the current order progress and outcome.
-   **ACP Resource Change \[sn\_itom\_pattern\_acp\_resource\_change\]**

    This table records changes detected in Azure resources. The \[sn\_cmp\_resource\_changes\_payload\_info\] table that used to store this info before the 1.21.0 version is no longer available.

    Key fields:

    -   Resource ID: the unique identifier for the changed resource in Azure.
    -   Change Payload: a snapshot of the attributes of interest for the resource.
    -   Order: A reference to the CMP Order \[sn\_cmp\_order\] field that pulled the change.
    -   Resource Status: A reference to the ACP Resource Status table to track the processing status of the change.
    -   State: the current processing state of the change. If the state is marked as 'Error', review the associated Resource Status record for further details.
-   **ACP Resource Status \[sn\_itom\_pattern\_acp\_resource\_status\]**

    This table tracks the overall status of resource processing.

    Key fields:

    -   Resource ID: the identifier for the resource being processed.
    -   Status: the processing state. The states are: Ready, In Progress, Failure, and Success.
    -   Error Message: If the processing failed, this field contains details about the error.

## Supported Azure resource types and changes

Azure Change Processing tracks a set of resource properties for each supported resource type. When a change is detected in one of these properties, Azure Change Processing retrieves an updated snapshot of the resource from Azure, and processes it in the CMDB to reflect the change.

<table id="table_w3g_w23_5wb"><thead><tr><th>

Resource type

</th><th>

Resource Property

</th></tr></thead><tbody><tr><td>

Microsoft.Compute/virtualMachine

</td><td>

-   **CreateOrDeleteVm : properties.changeType in \('Create','Delete'\)**
-   **ChangeStatus: \(properties.extended.instanceView.powerState.code\) in \('PowerState/running', 'PowerState/stopped', 'PowerState/deallocated'\)\)**
-   **ChangeDisk: properties.storageProfile**
-   **ChangeTag: tags.\***
-   **ChangeNetworkInterface : properties.networkProfile.networkInterfaces**

</td></tr><tr><td>

Microsoft.Compute/disks

</td><td>

-   **CreateOrDeleteDisk : properties.changeType in \('Create','Delete'\)**
-   **ChangeState : properties.diskState**
-   **ChangeSize : properties.storageProfile**
-   **ChangeTag : tags.\***

</td></tr><tr><td>

Microsoft.Network/networkSecurityGroups

</td><td>

-   **CreateOrDeleteNsg : properties.changeType in \('Create','Delete'\)**
-   **ChangeTag : tags.\***

</td></tr><tr><td>

Microsoft.Network/networkinterfaces

</td><td>

-   **CreateOrDeleteNic : properties.changeType in \('Create','Delete'\),**
-   **changePrimary : properties. properties.primary**
-   **ChangeIp : properties.ipConfigurations\[0\]'**
-   **ChangeTag : tags.\***

</td></tr><tr><td>

Microsoft.Network/publicIPAddresses

</td><td>

-   **CreateOrDeleteIp : properties.changeType in \('Create','Delete'\),**
-   **ChangeIpAddress : 'properties.ipaddress',**
-   **ChangeFqdn : properties.dnsSettings.fqdn**
-   **ChangeIpConfig : properties.ipConfiguration**
-   **ChangeTag : tags.\***

</td></tr></tbody>
</table>## Advantages of the Azure change processing

The Azure change processing offers the following advantages over the Microsoft Azure alert-driven discovery:

-   Improved performance and reduced probability of Azure API throttling
-   Simple setup

-   **Improved performance and reduced probability of Azure API throttling**

    The Microsoft Azure alert-driven discovery triggers a targeted discovery for each affected resource. Therefore, when the ServiceNow AI Platform receives a huge number of alerts, the targeted discovery may cause the Azure APIs to throttle. As a result, the alert processing performance of the ServiceNow AI Platform may decline. In contrast, the Azure change processing doesn’t trigger targeted discovery for each affected resource. Instead, it uses response mappings to update the CMDB per the available change information. During the next discovery, Cloud Discovery triggers appropriate patterns, if available, and populates detailed resource information in the CMDB. Therefore, Azure change processing improves the change handling performance of the ServiceNow AI Platform and reduces the probability of Azure API throttling.

-   **Simple setup**

    The Microsoft Azure alert-driven discovery uses a webhook to send the alerts to the ServiceNow AI Platform. As the Azure cloud generates alerts at the subscription level, the Microsoft Azure alert-driven discovery needs a webhook for each subscription you want to monitor. In contrast, Azure change processing uses CAPI and MID Server to interact with the Azure resource changes API. The API can provide change information at the management group level. Therefore, Azure change processing removes the need for webhooks and simplifies the setup.


You can [configure Azure change processing](../task/configure-azure-change-processing.md) to get resource change information from the Microsoft Azure cloud and use it to update the CMDB.

If you’re using the Microsoft Azure alert-driven discovery, then you can [migrate to Azure change processing](../task/migrate-to-azure-change-processing.md) to improve the change processing performance of the ServiceNow AI Platform and take advantage of the simplified setup.

**Related topics**  


[https://support.servicenow.com/kb?id=kb\_article\_view&amp;sysparm\_article=KB1705862](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1705862)

[Microsoft Azure Cloud discovery using patterns](../../service-mapping/reference/azure-cloud-discovery-patterns.md)

