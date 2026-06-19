---
title: AI Service Graph Connector for Salesforce
description: The AI Service Graph Connector for Salesforce enables you to discover and import AI assets from your Salesforce environment into ServiceNow AI Control Tower.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/salesforce.html
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower, Enable AI experiences]
---

# AI Service Graph Connector for Salesforce

The AI Service Graph Connector for Salesforce enables you to discover and import AI assets from your Salesforce environment into ServiceNow AI Control Tower.

The connector integrates with your Salesforce account to catalog AI systems, agents, models, and prompts. Usage data is automatically collected and populated into the AI Control Tower value dashboard, providing comprehensive visibility and governance of your AI operations.

## Download apps from the Store

Visit the ServiceNow store website to download the [AI Service Graph Connector for Salesforce](https://store.servicenow.com/store/app/2f89f78a47e73a50cbbce551336d43a3) application.

## Supported ServiceNow versions

This connector is supported on the following ServiceNow releases:

|Release|Status|
|-------|------|
|Australia|Supported|
|Zurich|Supported|
|Yokohama patch 11|Supported|

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

## Data Mapping

AI Agents: alm\_ai\_system\_digital\_asset -&gt; Model table \(cmdb\_ai\_system\_component\_product\_model\)

<table id="table_xn2_xps_m3c"><tbody><tr><td>

Required Fields

</td><td>

ServiceNow \(Target\)

</td><td>

Salesforce \(Staging\)

</td></tr><tr><td>

Model ID

</td><td>

Model

</td><td>

model\_id

</td></tr><tr><td>

Agent ID

</td><td>

Product instance identifier

</td><td>

agent\_id

</td></tr><tr><td>

Version

</td><td>

External record reference

</td><td>

version\_id

</td></tr><tr><td>

Status

</td><td>

State \(install\_status\)

</td><td>

u\_status

</td></tr><tr><td>

Quantity

</td><td>

Quantity

</td><td>

quantity

</td></tr><tr><td>

Vendor

</td><td>

Vendor

</td><td>

u\_vendor

</td></tr><tr><td>

Company

</td><td>

Company

</td><td>

cleansed\_manufacturer\_ref

</td></tr><tr><td>

Source System

</td><td>

Source System

</td><td>

vendor

</td></tr><tr><td>

Asset Type

</td><td>

Model Category

</td><td>

asset\_type

</td></tr></tbody>
</table>AI Models: alm\_ai\_model\_digital\_asset -&gt; Model table \(cmdb\_ai\_model\_product\_model\)

<table id="table_yn2_xps_m3c"><tbody><tr><td>

Required Fields

</td><td>

ServiceNow \(Target\)

</td><td>

Salesforce \(Staging\)

</td></tr><tr><td>

Asset Type

</td><td>

Model category

</td><td>

asset\_type

</td></tr><tr><td>

Foundation Model ID

</td><td>

Base model

</td><td>

foundation\_model\_identifier

</td></tr><tr><td>

Model

</td><td>

Model

</td><td>

base\_model

</td></tr><tr><td>

Status

</td><td>

State \(install\_status\)

</td><td>

u\_status

</td></tr><tr><td>

External Reference ID

</td><td>

External record reference

</td><td>

id

</td></tr><tr><td>

Vendor

</td><td>

Vendor

</td><td>

cleansed\_vendor\_ref

</td></tr><tr><td>

Quantity

</td><td>

Quantity

</td><td>

quantity

</td></tr></tbody>
</table>AI Tools: AI subcomponent reference table \(sn\_ent\_ai\_tool\) -&gt; sn\_ent\_ai\_system\_subcomponent\_m2m-&gt; AI system/Model table \(alm\_ai\_system\_digital\_asset\)

<table id="table_zn2_xps_m3c"><tbody><tr><td>

Required Fields

</td><td>

ServiceNow \(Target\)

</td><td>

Salesforce \(Staging\)

</td></tr><tr><td>

Description

</td><td>

Description

</td><td>

description

</td></tr><tr><td>

Type

</td><td>

Type

</td><td>

type

</td></tr><tr><td>

Source Information

</td><td>

Source information

</td><td>

source

</td></tr><tr><td>

Name

</td><td>

Name

</td><td>

developername

</td></tr><tr><td>

Table Name

</td><td>

Target document table

</td><td>

tablename

</td></tr></tbody>
</table>AI Prompts: alm\_ai\_prompt\_digital\_asset -&gt; Model table \(cmdb\_ai\_prompt\_product\_model\)

<table id="table_a42_xps_m3c"><tbody><tr><td>

Required Fields

</td><td>

ServiceNow \(Target\)

</td><td>

Salesforce \(Staging\)

</td></tr><tr><td>

Model Name

</td><td>

Model

</td><td>

model

</td></tr><tr><td>

Description

</td><td>

Prompt information

</td><td>

description

</td></tr><tr><td>

Table Name

</td><td>

ServiceNow table

</td><td>

table\_name

</td></tr><tr><td>

ID

</td><td>

External record reference

</td><td>

id

</td></tr></tbody>
</table>AI Agents Usage: sn\_ai\_disc\_ai\_usage -&gt; AI system/Model table \(alm\_ai\_system\_digital\_asset\)

<table id="table_b42_xps_m3c"><tbody><tr><td>

Required Fields

</td><td>

ServiceNow \(Target\)

</td><td>

Salesforce \(Staging\)

</td></tr><tr><td>

User

</td><td>

User

</td><td>

user

</td></tr><tr><td>

Time

</td><td>

Time

</td><td>

timestamp

</td></tr><tr><td>

Parent ID

</td><td>

Session ID

</td><td>

parentid

</td></tr><tr><td>

Total Invocations

</td><td>

Count

</td><td>

totalinvocations

</td></tr><tr><td>

Conversion Definition ID

</td><td>

AI system

</td><td>

conversationdefinitionid

</td></tr></tbody>
</table>