---
title: AI Service Graph Connector for GCP Vertex AI
description: The AI Service Graph Connector for GCP Vertex AI enables you to discover and import AI assets from your Google Cloud environment into ServiceNow AI Control Tower.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ai-control-tower/gcp-vertex-ai.html
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower, Enable AI experiences]
---

# AI Service Graph Connector for GCP Vertex AI

The AI Service Graph Connector for GCP Vertex AI enables you to discover and import AI assets from your Google Cloud environment into ServiceNow AI Control Tower.

The connector integrates with your Google Cloud Platform account to catalog AI systems, agents, models, and prompts. Usage data is automatically collected and populated into the AI Control Tower value dashboard, providing comprehensive visibility and governance of your AI operations.

## Download apps from the Store

Visit the  ServiceNow store website to download the [AI Service Graph Connector for GCP Vertex AI](https://store.servicenow.com/store/app/5b3cfb8a87e7fa14a6c6fc48cebb3512) application.

## Supported ServiceNow versions

This connector is supported on the following ServiceNow releases:

|Release|Status|
|-------|------|
|Australia|Supported|
|Zurich|Supported|
|Yokohama|Supported|

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

## GCP Vertex AI Prerequisites

Follow the setup instructions to create a service account, assign roles, bind roles to the service account, and enable APIs. To create a JKS file, a JSON file is required. If a JSON file is available, skip the JKS file creation step. After completing setup, register the connector in your ServiceNow instance. For setup instructions and API details, see the [Service Graph connector for GCP Vertex AI- Setup Instructions \[KB2731256\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB2731256) KB article.

## Data Mapping

The following table lists the data sources, the staging tables, and the target tables  CMDB CI classes and non-CMDB classes where data is stored for a  GCP Vertex AI  project.

<table id="table_pps_vnk_m3c"><thead><tr><th>

Data source

</th><th>

Staging table

</th><th>

Target tables

</th></tr></thead><tbody><tr><td>

SG-GCPVertexAI-Execution

</td><td>

sn\_ai\_disc\_gcp\_sgc\_sg\_gcp\_execution

</td><td>

sn\_ai\_disc\_ai\_usage

</td></tr><tr><td>

SG-GCPVertexAI-System

</td><td>

sn\_ai\_disc\_gcp\_sgc\_sg\_gcp\_ai\_system

</td><td>

cmdb\_ai\_system\_component\_product\_model alm\_ai\_system\_digital\_asset

 cmdb\_ci\_function\_ai

 cmdb\_rel\_asset\_ci

</td></tr><tr><td>

SG-GCPVertexAI-Model

</td><td>

sn\_ai\_disc\_gcp\_sgc\_sg\_gcp\_ai\_model

</td><td>

cmdb\_ai\_model\_product\_model alm\_ai\_model\_digital\_asset

</td></tr><tr><td>

SG-GCPVertexAI-Tool

</td><td>

sn\_ai\_disc\_gcp\_sgc\_sg\_gcp\_ai\_tool

</td><td>

sn\_ent\_ai\_tool

</td></tr><tr><td>

SG-GCPVertexAI-Prompt

</td><td>

sn\_ai\_disc\_gcp\_sgc\_sg\_gcp\_ai\_prompt

</td><td>

cmdb\_ai\_prompt\_product\_model alm\_ai\_prompt\_digital\_asset

</td></tr><tr><td>

SG-GCPVertexAI-System Subcomponent M2M

</td><td>

sn\_ai\_disc\_gcp\_sgc\_sg\_gcp\_ai\_system\_subcomponent\_m2m

</td><td>

sn\_ent\_ai\_system\_subcomponent\_m2m

</td></tr></tbody>
</table>