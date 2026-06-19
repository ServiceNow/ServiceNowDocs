---
title: AI Service Graph Connector for Hugging Face
description: The AI Service Graph Connector for Hugging Face enables you to discover and import AI assets from your Hugging Face environment into ServiceNow AI Control Tower.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/ai-service-graph-connector-for-hugging-face.html
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-04-30"
reading_time_minutes: 3
breadcrumb: [Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower, Enable AI experiences]
---

# AI Service Graph Connector for Hugging Face

The AI Service Graph Connector for Hugging Face enables you to discover and import AI assets from your Hugging Face environment into ServiceNow AI Control Tower.

The connector integrates with your Hugging Face account to catalog AI systems, agents, models, and prompts from Hugging Face Spaces. Usage data is automatically collected and populated into the AI Control Tower value dashboard, providing comprehensive visibility and governance of your AI operations.

## Download apps from the Store

Visit the ServiceNow store website to download the [AI Service Graph Connector for Hugging Face](https://store.servicenow.com/store/app/201bf3c397c04310f17933e11153af96) application.

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

1.  Select Global from the application picker
2.  Navigate to Application Access
3.  Select the Can create, Can update, and Can delete checkboxes.
4.  Select Update
5.  Switch to the connector application scope

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

4.  After completion, switch to the connector application scope

## Hugging Face Prerequisites

Complete the following steps in your Hugging Face environment before creating a connection.

-   Hugging Face account \(If you don't have a Hugging Face account, create one at https://huggingface.co\).
-   Generate API Tokens

## Discovery Scope

The Hugging Face connector discovers AI components from Hugging Face Spaces by analyzing Python files using pattern matching. The following AI asset types are identified during discovery:

<table><tbody><tr><td>

Asset Type

</td><td>

Description

</td></tr><tr><td>

AI Agents / Systems

</td><td>

Applications and agent implementations identified in Space code.

</td></tr><tr><td>

AI Models

</td><td>

Language models, embeddings, and other ML models referenced in code.

</td></tr><tr><td>

AI Tools

</td><td>

Function definitions and tool implementations.

</td></tr><tr><td>

AI Prompts

</td><td>

Prompt templates and configuration strings.

</td></tr></tbody>
</table>The discovery process follows these stages:

-   Space Discovery – Identifies Hugging Face Spaces based on organization membership or public visibility.
-   Code Analysis – Downloads and analyzes Python files from each Space.
-   Pattern Matching – Identifies these components:
    -   Agent implementations \(for example, LangChain agents, custom frameworks\)
    -   Model references \(for example, model\_id parameters, API calls\)
    -   Tool definitions \(for example, function decorators, tool classes\)
    -   Prompt templates \(for example, PromptTemplate, string templates\)
-   Relationship Mapping – Links AI systems to their sub-components such as models, tools, and prompts.
-   Incremental Updates – Processes only Spaces modified since the last successful import.

**Note:** The connector performs incremental discovery, only processing spaces that have been modified since it's last successful import.

## Data Mapping

The connector maps Hugging Face AI assets to ServiceNow staging tables and target CMDB tables for comprehensive asset management.

|Data Source|Staging Table|Target Table|Description|
|-----------|-------------|------------|-----------|
|SG-HuggingFace-Discovery|sn\_ai\_hf\_disc\_ai\_discovery\_staging|Parent data source|Discovers HuggingFace Spaces and feeds other staging tables|
|SG-HuggingFace-System|sn\_ai\_hf\_disc\_ai\_system\_staging|alm\_ai\_system\_digital\_asset|Imports AI systems and applications|
|SG-HuggingFace-Model|sn\_ai\_hf\_disc\_ai\_model\_staging|alm\_ai\_model\_digital\_asset|Imports AI models and embeddings|
|SG-HuggingFace-Prompt|sn\_ai\_hf\_disc\_ai\_prompt\_staging|alm\_ai\_prompt\_digital\_asset|Imports prompt templates|
|SG-HuggingFace-Tool|sn\_ai\_hf\_disc\_ai\_tool\_staging|sn\_ent\_ai\_tool|Imports tool and function definitions|
|SG-HuggingFace-SubComponents M2M|sn\_ai\_hf\_disc\_ai\_m2m\_staging|sn\_ent\_ai\_system\_subcomponent\_m2m|Imports relationships between AI systems and their components|

## Target Tables

The Hugging Face connector populates the following target tables in ServiceNow.

Digital Asset Tables

-   alm\_ai\_system\_digital\_asset – Stores AI System digital assets discovered from Hugging Face Spaces.
-   alm\_ai\_model\_digital\_asset – Stores AI Model digital assets including language models and embeddings.
-   alm\_ai\_prompt\_digital\_asset – Stores AI Prompt digital assets including prompt templates and configurations.

Entity Tables

-   sn\_ent\_ai\_tool: Stores AI Tools including function definitions and tool implementations
-   sn\_ent\_ai\_system\_subcomponent\_m2m: Stores many-to-many relationships between AI systems and their subcomponents \(models, tools, prompts\)

**Note:** The Hugging Face connector currently focuses on discovery of AI assets. Usage and execution tracking capabilities may be added in future versions.

## Data Flow Architecture

The Hugging Face connector follows this data flow:

<table><tbody><tr><td>

Stage

</td><td>

Description

</td></tr><tr><td>

Data Source

</td><td>

The connector calls Hugging Face APIs to discover Spaces based on organization or public visibility settings.

</td></tr><tr><td>

Staging Tables

</td><td>

Raw data is loaded into import set staging tables for processing.

</td></tr><tr><td>

Transform Maps

</td><td>

Data is transformed, validated, and mapped to target table schema.

</td></tr><tr><td>

Target Tables

</td><td>

Cleaned and structured data is inserted into the final destination tables in the ServiceNow CMDB.

</td></tr></tbody>
</table>