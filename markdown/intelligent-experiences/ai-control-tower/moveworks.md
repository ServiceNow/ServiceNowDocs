---
title: AI Service Graph Connector for Moveworks
description: The AI Service Graph Connector for Moveworks enables you to discover and import AI assets from Moveworks environments into ServiceNow AI Control Tower.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/moveworks.html
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-05-26"
reading_time_minutes: 1
breadcrumb: [Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower, Enable AI experiences]
---

# AI Service Graph Connector for Moveworks

The AI Service Graph Connector for Moveworks enables you to discover and import AI assets from Moveworks environments into ServiceNow AI Control Tower.

The connector integrates with your Moveworks account to catalog AI systems, agents, models, and prompts. Usage data is automatically collected and populated into the AI Control Tower value dashboard, providing comprehensive visibility and governance of your AI operations.

## Download apps from the Store

Visit the  [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to download the AI Service Graph Connector for Moveworks application.

## Supported ServiceNow versions

|Release|Status|
|-------|------|
|Australia|Supported|
|Zurich|Supported|

## User Roles

You must have one of the following roles assigned.

|Required Roles|
|--------------|
|sn\_ai\_disc.discovery\_admin|
|sn\_cmdb\_int\_util.sgc\_admin|

## ServiceNow Prerequisites

Complete the following setup steps once when configuring the connector for the first time.

**Note:** Updating data source access and clear cache is a prerequisite that needs to be completed only once, when setting up a new instance for the first time.

Update Data Source Access

The connector requires write permissions to the Data Source table to create data sources.

To enable data source creation:

1.  Select Global from the application picker.
2.  Navigate to Application Access.
3.  Select the Can create, Can update, and Can delete check boxes.
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

## Moveworks Prerequisites

Movework Setup Instructions:

An API key is required to integrate with Moveworks. Refer to the [Moveworks API reference documentation](https://help.moveworks.com/api-reference/api-credentials#rotation--revocation) for instructions on how to create an API key.

The API key must contain the following scopes:

-   Conversations
-   Interactions
-   Plugin Calls

Additionally, the Organization Name is required to register your Moveworks connection. Refer to the [Moveworks organization information documentation](https://docs.moveworks.com/service-management/administration/organization-information) for instructions on how to view the Organization Name.

