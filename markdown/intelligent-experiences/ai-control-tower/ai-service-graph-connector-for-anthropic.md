---
title: AI Service Graph Connector for Anthropic
description: The AI Service Graph Connector for Anthropic discovers and imports AI Models and tracks usage data \(per-user AI asset cost\) into ServiceNow AI Control Tower.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/ai-service-graph-connector-for-anthropic.html
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-07-14"
reading_time_minutes: 1
breadcrumb: [Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower \(legacy\), Enable AI experiences]
---

# AI Service Graph Connector for Anthropic

The AI Service Graph Connector for Anthropic discovers and imports AI Models and tracks usage data \(per-user AI asset cost\) into ServiceNow AI Control Tower.

## Download apps from the Store

Visit the [ServiceNow store](https://store.servicenow.com/store) website to download the AI Service Graph Connector for Anthropic application.

## Supported ServiceNow versions

This connector is supported on the following ServiceNow releases:

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


## Anthropic Prerequisites

The Al Service Graph Connector for Anthropic automatically imports Al data from your Anthropic environment into the ServiceNow CMDB. This playbook will guide you through configuring the connection and credentials.

Before proceeding, confirm you have:

-   Anthropic Account: A Claude Console account
-   Credentials:
    -   Anthropic API key- Required for Al Models discovery. See [Anthropic API key](https://platform.claude.com/docs/en/manage-claude/authentication#api-keys) to generate API key.
    -   Anthropic Analytics API key- Required for Anthropic Product usage per user \(Available in Anthropic Enterprise plan\). See, [Anthropic Analytics API key](https://platform.claude.com/docs/en/api/admin/analytics) to generate API key.

