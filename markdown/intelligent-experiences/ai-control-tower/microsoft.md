---
title: AI Service Graph Connector for Microsoft
description: The AI Service Graph Connector for Microsoft enables you to discover and import AI assets from Azure AI Foundry and Microsoft Copilot Studio environments into ServiceNow AI Control Tower.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/microsoft.html
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower, Enable AI experiences]
---

# AI Service Graph Connector for Microsoft

The AI Service Graph Connector for Microsoft enables you to discover and import AI assets from Azure AI Foundry and Microsoft Copilot Studio environments into ServiceNow AI Control Tower.

The connector creates separate AI connections for each Microsoft platform, cataloging AI agents, models, and prompts. The usage information is consumed by the AI Control Tower value dashboard, providing comprehensive visibility and governance of your AI operations.

Key capabilities:

-   Discovery of Azure AI Foundry agents across ML Services, AI Services, and New Foundry variants
-   Discovery of Microsoft Copilot agents across single or multiple Power Platform environments
-   AI asset lineage and dependency tracking through sub-component relationships
-   Usage and execution metrics aggregated by agent, date, and session
-   Support for tenant-wide discovery or filtered discovery by resource and region \(Azure Foundry\)
-   Multi-environment discovery using a single Copilot connection

## Download apps from the store

Visit the  ServiceNow store website to download the [AI Service Graph Connector for Microsoft](https://store.servicenow.com/store/app/4bb87ac7874fb250a6c6fc48cebb357b)  application.

## Supported ServiceNow versions

|Release|Status|
|-------|------|
|Australia|Supported|
|Zurich|Supported|
|Yokohama Patch 11|Supported|

## User Roles

You must have one of the following roles assigned to complete the configuration task.

<table><tbody><tr><td>

Required Role

</td></tr><tr><td>

sn\_ai\_disc.discovery\_admin

</td></tr><tr><td>

sn\_cmdb\_int\_util.sgc\_admin

</td></tr></tbody>
</table>## ServiceNow Prerequisites

Complete the following setup steps once when configuring the connector for the first time.

**Note:** Updating data source access and clear cache is a prerequisite that needs to be completed only once, when setting up a new instance for the first time.

Update Data Source Access

The connector requires write permissions to the Data Source table to create data sources.

To enable data source creation:

1.  Select Global from the application picker.
2.  Navigate to Application Access.
3.  Select the Can create, Can update, and Can delete checkboxes.
4.  Select Update.
5.  Switch to the connector application scope.

Clear cache

Clear the cached data for the Data Source and Tables.

To clear the cache:

1.  Navigate to System Definition &gt; Background Scripts
2.  Paste the following script into the Run Script text box:

    ```
    GlideTableManager.invalidateTable('sys_data_source');
    GlideCacheManager.flushTable('sys_data_source');
    GlideTableManager.invalidateTable('sys_db_object');
    GlideCacheManager.flushTable('sys_db_object');
    
    ```

3.  Select Run Script.

    **Note:** The script may take several minutes to complete.

4.  After completion, switch to the connector application scope.

## Azure AI Foundry Prerequisites

Complete the following steps in your Azure environment before creating an Azure Foundry connection.

Configure OAuth Credentials

The connector uses OAuth to authenticate with Azure APIs. To obtain credentials, register an application in Microsoft Entra ID. For full instructions, refer to the [Azure documentation](https://learn.microsoft.com/en-us/rest/api/azure/#register-your-client-application-with-azure-ad)

The Azure client application requires the following roles:

-   Reader role at the subscription or resource group level to discover resources.
-   Azure AI Foundry User role on the Azure AI Foundry resources.

**Note:** Starting from March 2026, ServiceNow supports the New Azure AI Foundry alongside the original Foundry. The New Foundry treats each agent version as a distinct entity and adds support for MCP, OpenAPI, and A2A Preview tool types.

Discovery scope

Configure the scope of Azure Foundry discovery using the following options:

Tenant-wide discovery \(default\): Leave the Resource Name and Region fields empty to discover all Al agents across your entire Azure tenant.

Filter by resource \(optional\): To limit discovery to specific resources, enter resource names as comma-separated values \(e.g., resource1, resource2\).

Filter by region \(optional\): To limit discovery to specific Azure regions, enter region names as comma-separated values \(e.g., eastus, westus2\).

## Microsoft Copilot Studio Prerequisites

Complete the following steps in your Power Platform environment before creating a Copilot connection.

Register an Application in Microsoft Entra ID

Register an application to obtain OAuth credentials for the connector.

To register the application:

-   Follow the [Microsoft Entra app registration quickstart](https://learn.microsoft.com/en-us/entra/identity-platform/quickstart-register-app) to create a new application.
-   Record the Client ID and Client Secret from the registration.

Step 2: Grant application access to your Copilot environment

Configure the application as a user in your Copilot environment.

To configure application access:

1.  Open the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/home)
2.  Navigate to Environments and select your Copilot environment
3.  Go to Settings &gt; Users + Permissions &gt; Application users
4.  Select New App User and add your application using the Client ID from step 1
5.  Assign the following security roles to the application user
    -   Basic User
    -   System administrator

**Note:** You can obtain the Environment ID from Settings &gt; Session details &gt; Environment ID in your environment.

Multi-Environment Support

You can discover agents from multiple Copilot environments using a single connection. To configure multi-environment discovery:

-   Enter multiple environment IDs as comma-separated values in the Environment ID field \(eg.., env-id-1, env-id-2, env-id-3\)
-   The same OAuth credentials \(Client ID and Client Secret\) are used for all environments
-   Ensure the application user is configured in each environment with the required security roles
-   Each environment will be tested and discovered separately during the import process

