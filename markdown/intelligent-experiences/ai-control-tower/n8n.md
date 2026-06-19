---
title: AI Service Graph Connector for n8n
description: The AI Service Graph Connector for n8n enables you to discover and import AI assets from your n8n environment into ServiceNow AI Control Tower.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ai-control-tower/n8n.html
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower, Enable AI experiences]
---

# AI Service Graph Connector for n8n

The AI Service Graph Connector for n8n enables you to discover and import AI assets from your n8n environment into ServiceNow AI Control Tower.

The connector integrates with your n8n instance to catalog AI systems, agents, models, and prompts. The information is consumed by the AI Control Tower value dashboard, providing comprehensive visibility and governance of your AI operations.

## Download apps from the Store

Visit the  ServiceNow store website to download the [AI Service Graph Connector for n8n](https://store.servicenow.com/store/app/8ee0b14b93fe32107b73393d6cba10d6) application.

## Supported ServiceNow versions

This connector is supported on the following ServiceNow releases:

|Release|Status|
|-------|------|
|Australia|Supported|
|Zurich|Supported|
|Yokohama Patch 13|Supported|

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

## n8n Prerequisites

Before creating a connection, generate an API key in your n8n instance. Refer to the [n8n API Key](https://docs.n8n.io/api/authentication/) documentation to learn about creating a n8n API Key.

**Note:** The role required to generate an API key in n8n is admin

