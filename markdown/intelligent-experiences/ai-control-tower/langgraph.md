---
title: AI Service Graph connector for LangGraph
description: The AI Service Graph Connector for LangGraph enables you to discover and import AI assets from your LangGraph environment into ServiceNow AI Control Tower.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ai-control-tower/langgraph.html
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower, Enable AI experiences]
---

# AI Service Graph connector for LangGraph

The AI Service Graph Connector for LangGraph enables you to discover and import AI assets from your LangGraph environment into ServiceNow AI Control Tower.

The connector integrates with the LangSmith API to catalog AI systems, agents, models,and prompts. Usage data is automatically collected and populated into the AI Control Tower value dashboard, providing comprehensive visibility and governance of your AI operations.

## Download apps from the Store

Visit the ServiceNow store website to download the [AI Service Graph Connector for LangGraph](https://store.servicenow.com/store/app/19b23dd3537e7a9072c95a01a0490e4f) application.

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

## LangGraph Prerequisites

Before creating a connection, generate an API key in your LangGraph instance. Refer to the [Create an account and API key with LangGraph](https://docs.langchain.com/langsmith/create-account-api-key) documentation to learning about creating an API Key in LangGraph.

**Note:** To access the latest and most comprehensive guidelines for managing API keys, see [About LangGraph](https://docs.langchain.com/)

## Data Mapping

The following table lists the data sources, the staging tables, and the target tables  CMDB CI classes and non-CMDB  classes where data is stored for LangGraph project.

<table id="table_s1w_52q_m3c"><tbody><tr><td>

Data Source

</td><td>

Import Set Table

</td><td>

Target Table\(s\)

</td></tr><tr><td>

SG-LangGraph Agents

</td><td>

sn\_langgraph\_integ\_agents

</td><td>

alm\_ai\_system\_digital\_asset

 alm\_ai\_prompt\_digital\_asset

 cmdb\_ci\_function\_ai

</td></tr><tr><td>

SG-LangGraph Usage

</td><td>

sn\_langgraph\_integ\_usage

</td><td>

alm\_ai\_model\_digital\_asset

 sn\_ai\_disc\_ai\_usage

</td></tr></tbody>
</table>