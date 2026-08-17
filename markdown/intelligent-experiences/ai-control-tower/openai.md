---
title: AI Service Graph Connector for OpenAI
description: The AI Service Graph Connector for OpenAI enables you to discover and import AI models and track model usage from your OpenAI environment into ServiceNow AI Control Tower.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/openai.html
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-06-30"
reading_time_minutes: 1
breadcrumb: [Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower \(legacy\), Enable AI experiences]
---

# AI Service Graph Connector for OpenAI

The AI Service Graph Connector for OpenAI enables you to discover and import AI models and track model usage from your OpenAI environment into ServiceNow AI Control Tower.

## Download apps from the Store

Visit the [ServiceNow store](https://store.servicenow.com/store) website to download the AI Service Graph Connector for OpenAI application.

## Supported ServiceNow versions

This connector is supported on the following ServiceNow releases:

|Release|Status|
|-------|------|
|Australia|Supported \(Patch 4\)|
|Zurich|Supported \(Patch 11\)|

## User Roles

You must have one of the following roles assigned.

|Required Roles|
|--------------|
|sn\_ai\_disc.discovery\_admin|
|sn\_cmdb\_int\_util.sgc\_admin|

## ServiceNow Prerequisites

Complete the following setup steps once when configuring the connector for the first time.

**Note:** Updating data source access and clear cache is a prerequisite that needs to be completed only once, when setting up a new instance for the first time.

Update Data Source Access:

The connector requires write permissions to the Data Source table to create data sources.

To enable data source creation:

1.  Select **Global** from the application picker.
2.  Navigate to **Application Access**.
3.  Select the **Can create**, **Can update**, and **Can delete** check boxes.
4.  Select **Update**.
5.  Switch to the connector application scope.

Clear the cached data for the Data Source and Tables.

To clear the cache:

1.  Navigate to **System Definition** &gt; **Background Scripts**.
2.  Enter the following script in the **Run Script** text box:

    ```
    GlideTableManager.invalidateTable('sys_data_source');
    GlideCacheManager.flushTable('sys_data_source');
    GlideTableManager.invalidateTable('sys_db_object');
    GlideCacheManager.flushTable('sys_db_object');
    
    ```

3.  Select **Run Script**.

    **Note:** The script might take several minutes to complete. After completion, switch to the connector application scope.


## OpenAI Prerequisites

Before proceeding, ensure you have:

-   OpenAI Account
-   Credentials:
    -   OpenAI Standard API key- Required for AI Models information. Unique to each projects created in Open AI.
    -   OpenAI Admin API key- Required for AI models usage.

For OpenAI Setup documentation, see [OpenAI resources](https://developers.openai.com/api/reference/overview#authentication) and use these OpenAI resources to setup credentials.

