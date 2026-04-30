---
title: Install and configure the Microsoft Azure Sentinel integration
description: Install and configure the Microsoft Azure Sentinel integration from the ServiceNow Store on your ServiceNow AI Platform instance to start ingesting Azure Sentinel incidents.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Microsoft Azure Sentinel integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Install and configure the Microsoft Azure Sentinel integration

Install and configure the Microsoft Azure Sentinel integration from the ServiceNow Store on your ServiceNow AI Platform instance to start ingesting Azure Sentinel incidents.

## Before you begin

**Important:**

Microsoft has extended the deprecation of the Azure Sentinel experience in the Azure portal from March 2026 to March 2027.

If you are currently using the Azure Sentinel integration with Security Incident Response \(SIR\), we strongly recommend migrating to the new Defender portal integration as soon as possible. The Defender integration includes a built-in migration utility that automatically converts your existing Sentinel profiles into Defender profiles, while ensuring continuity of incidents created through Sentinel after the transition. For more information, see [Microsoft Sentinel to Defender Migration Guide](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2795226).

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

## Procedure

1.  Download the Microsoft Azure Sentinel integration from the ServiceNow Store and install it.

2.  Navigate to **Security Operations** &gt; **Integrations** &gt; **Integration Configurations**.

3.  Search for the Microsoft Azure Sentinel tile and click **Configure**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name for the Microsoft Azure Cloud instance configuration.|
    |Identity URL|Identity URL for the Microsoft Azure Cloud tenant. For example, `login.microsoftonline.com`. For additional information, see [Microsoft Azure documentation](https://learn.microsoft.com/en-us/azure/azure-government/compare-azure-government-global-azure).|
    |Azure Resource Manager|Azure Resource Manager Endpoint for Microsoft Azure Cloud tenant. For example, `management.azure.com`. For additional information, see [Microsoft Azure documentation](https://learn.microsoft.com/en-us/azure/azure-government/compare-azure-government-global-azure).|
    |Tenant ID|Microsoft Azure Sentinel Tenant ID. This is the instance from which all the incidents in the Microsoft Azure portal are retrieved.|
    |Client ID|Client ID for the application that you’ve registered in the Microsoft Azure portal.|
    |Client Secret|Client secret for your registered application.|
    |Subscription ID|Subscription ID for your registered application.|
    |Resource Group Name|Resource group name for your registered application.|
    |Workspace Name|Workspace name for your registered application.|

5.  Click **Submit**.


## Result

After you successfully validate and submit the configuration, each incident ingestion server configuration is saved on the Security Integrations page as a tile.

