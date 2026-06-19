---
title: AI Service Graph Connector for Databricks
description: The AI Service Graph Connector for Databricks enables you to discover and import AI assets from your Databricks environment into ServiceNow AI Control Tower.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/ai-service-graph-connector-for-databricks.html
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-05-03"
reading_time_minutes: 3
breadcrumb: [Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower, Enable AI experiences]
---

# AI Service Graph Connector for Databricks

The AI Service Graph Connector for Databricks enables you to discover and import AI assets from your Databricks environment into ServiceNow AI Control Tower.

The connector integrates with your Databricks account to catalog AI systems, agents, models, and prompts. Usage data is automatically collected and populated into the AI Control Tower value dashboard, providing comprehensive visibility and governance of your AI operations.

## Download apps from the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to download the AI Service Graph Connector for Databricks application.

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

## Databricks Prerequisites

The Al Service Graph Connector for Databricks automatically imports data from your Databricks into the ServiceNow CMDB. This playbook will guide you through configuring the connection and credentials.

Before proceeding, verify you have:

Databricks Workspace: An active workspace \(Azure, AWS, or GCP\) with administrative access to the resources you intend to sync.

Authentication Method: A valid OAuth credentials with sufficient scopes to read workspace metadata.

Required Permissions

These permissions are managed via the Databricks Admin console or Account console under the User Management or Service Principal sections:

Service Principal / User Access: The identity used for the connection must have the Admin or Workspace Access entitlement.

Resource-Specific Permissions

Compute/Clusters: Can View permissions for all clusters to be imported.

Unity Catalog: USE CATALOG and USE SCHEMA permissions if importing data lineage or metadata from the Unity Catalog.

SQL Warehouses: Can Use permissions if tracking SQL endpoint utilization.

For information on Databricks resources to generate credentials and configure workspace access, see [Databricks- Configure OAuth for Service Principals](https://docs.databricks.com/aws/en/dev-tools/auth/oauth-m2m) and [https://docs.databricks.com/aws/en/admin/users-groups](https://docs.databricks.com/aws/en/admin/users-groups)

## Data Mapping

Agents: alm\_ai\_system\_digital\_asset -&gt; Model table \(cmdb\_ai\_system\_component\_product\_model\)

<table><tbody><tr><td>

Required Fields

</td><td>

ServiceNow \(Target\)

</td><td>

Databricks \(Staging\)

</td></tr><tr><td>

Model ID

</td><td>

Model

</td><td>

ai\_system\_product\_model

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

u\_id

</td></tr><tr><td>

Status

</td><td>

State \(install\_status\)

</td><td>

install\_status

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

vendor\_ref

</td></tr><tr><td>

Company

</td><td>

Company

</td><td>

cleansed\_manufacturer\_ref

</td></tr><tr><td>

 

</td><td>

AI Models

</td><td>

ai\_models

</td></tr><tr><td>

Source System

</td><td>

Source System

</td><td>

vendor\_name

</td></tr><tr><td>

Asset Type

</td><td>

Model Category

</td><td>

asset\_type

</td></tr></tbody>
</table>Models: AI Model Digital Asset \(alm\_ai\_model\_digital\_asset\):

<table><tbody><tr><td>

Required Fields

</td><td>

ServiceNow \(Target\)

</td><td>

Databricks \(Model Staging\)

</td></tr><tr><td>

 

</td><td>

Model Category

</td><td>

asset\_type

</td></tr><tr><td>

 

</td><td>

External record reference

</td><td>

 u\_id

</td></tr><tr><td>

Model Id

</td><td>

Model

</td><td>

 ai\_product\_model

</td></tr><tr><td>

 

</td><td>

State

</td><td>

 install\_status

</td></tr><tr><td>

Provider

</td><td>

Company

</td><td>

 cleanse\_manufacturer\_ref

</td></tr><tr><td>

Vendor

</td><td>

Vendor

</td><td>

 vendor\_ref

</td></tr><tr><td>

 

</td><td>

Source System

</td><td>

 vendor\_name

</td></tr><tr><td>

 

</td><td>

Quantity

</td><td>

 quantity

</td></tr></tbody>
</table>Tools: AI Tool \(sn\_ent\_ai\_tool\)

<table><tbody><tr><td>

Required Fields

</td><td>

ServiceNow

</td><td>

Databricks

</td></tr><tr><td>

Name

</td><td>

Name

</td><td>

Tool Name

</td></tr><tr><td>

 

</td><td>

 Type

</td><td>

Tool Type

</td></tr><tr><td>

Description

</td><td>

 Description

</td><td>

Tool Description

</td></tr><tr><td>

Source Information

</td><td>

 Source Information

</td><td>

Vendor Name

</td></tr></tbody>
</table>AI Agents Usage: sn\_ai\_disc\_ai\_usage -&gt; AI system/Model table \(alm\_ai\_system\_digital\_asset\)

<table><tbody><tr><td>

Required Fields

</td><td>

ServiceNow \(Target\)

</td><td>

Databricks \(Staging\)

</td></tr><tr><td>

User

</td><td>

User

</td><td>

User ID

</td></tr><tr><td>

Time

</td><td>

Time

</td><td>

Timestamp

</td></tr><tr><td>

Parent ID

</td><td>

Session ID

</td><td>

Session ID

</td></tr><tr><td>

Total Invocations

</td><td>

Count

</td><td>

Invocation count

</td></tr><tr><td>

AI system

</td><td>

AI system

</td><td>

Agent ID

</td></tr><tr><td>

 

</td><td>

Type

</td><td>

Type

</td></tr></tbody>
</table>