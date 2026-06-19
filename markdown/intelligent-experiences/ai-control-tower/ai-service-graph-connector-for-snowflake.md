---
title: AI Service Graph Connector for Snowflake
description: The AI Service Graph Connector for Snowflake enables you to discover and import AI assets from your Snowflake environment into ServiceNow AI Control Tower.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ai-control-tower/ai-service-graph-connector-for-snowflake.html
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-05-01"
reading_time_minutes: 3
breadcrumb: [Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower, Enable AI experiences]
---

# AI Service Graph Connector for Snowflake

The AI Service Graph Connector for Snowflake enables you to discover and import AI assets from your Snowflake environment into ServiceNow AI Control Tower.

The connector integrates with your Snowflake account to catalog AI systems, agents, models, and prompts. Usage data is automatically collected and populated into the AI Control Tower value dashboard, providing comprehensive visibility and governance of your AI operations.

Key Capabilities:

-   Automated discovery of Cortex agents and models
-   Fine-tuning job monitoring and metadata capture
-   AI asset lineage and dependency tracking
-   Usage analytics and session monitoring
-   Integration with ServiceNow CMDB for comprehensive asset management
-   Support for multi-account Snowflake deployments

## Download apps from the Store

Visit the ServiceNow store website to download the [AI Service Graph Connector for Snowflake](https://store.servicenow.com/store/app/d637f5ab47e84f90d0e19fe1516d43e2) application.

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

## Snowflake Prerequisites

Complete the following configuration steps in your Snowflake environment before creating a connection.

Network Configuration

**Note:** The outbound integration IP addresses for your ServiceNow instance must be allowed in your Snowflake network policies. See the [How to find IP address and datacenter information for your instance \[KB0538621\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0538621) article in the Now Support Knowledge Base.

Account Identifier Format

**Note:** The Snowflake Statements API requires account identifiers in LDF \(Lowercase-Digit-Hyphen\) format in the connection URL. Account identifiers with uppercase letters or special characters must be converted to lowercase or replaced with the account locator.

Use the following format for your connection URL: https://&lt;account\_locator&gt;.snowflakecomputing.com and don't use this format: https://&lt;account\_identifier&gt;.snowflakecomputing.com.

If your account identifier contains uppercase letters or special characters, use your account locator \(for example, xy12345\) instead. Your account locator is always LDF-safe.

## Service Account and Role Configuration

Create a dedicated service account in Snowflake with least-privilege access. The connector requires specific permissions to query Cortex agents, models, and observability data.

Create a Role with Required Privileges

Create a new role for the connector and grant the following privileges:

Core Discovery Access:

-   GRANT USAGE ON DATABASE &lt;database\_name&gt;
-   GRANT USAGE ON SCHEMA &lt;schema\_name&gt;

Cortex access

-   GRANT MANAGE ACCOUNTS
-   GRANT DATABASE ROLE SNOWFLAKE.CORTEX\_USER

Create a Service Account

Create a service account user and assign the connector role:

-   CREATE USER &lt;service\_account\_name&gt; TYPE=SERVICE
-   GRANT ROLE &lt;connector\_role&gt; TO USER &lt;service\_account\_name&gt;
-   ALTER USER &lt;service\_account\_name&gt; SET DEFAULT\_WAREHOUSE = &lt;warehouse\_name&gt;

Configure JWT Key-Pair Authentication

The connector uses JWT key-pair authentication to securely connect to Snowflake.

For detailed steps on generating RSA key pairs and configuring key-pair authentication in Snowflake, see the [Configuring Keystore for Snowflake Keypair authentication \[KB2834688\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB2834688) article in the Now Support Knowledge Base.

## Data Mapping

The connector maps Snowflake AI assets to ServiceNow CMDB tables and custom tables for comprehensive asset management.

.

<table id="table_ktv_2nr_djc"><tbody><tr><td>

Data Source

</td><td>

Staging Table

</td><td>

Target CMDB Tables

</td></tr><tr><td>

Snowflake Agents

</td><td>

sn\_ai\_disc\_sgc\_sno\_sgc\_snowflake\_agents

</td><td>

cmdb\_ci\_function\_ai, alm\_ai\_system\_digital\_asset, alm\_ai\_model\_digital\_asset, sn\_ai\_disc\_ai\_usage

</td></tr><tr><td>

Snowflake Usage

</td><td>

sn\_ai\_disc\_sgc\_sno\_sgc\_snowflake\_usage

</td><td>

sn\_ai\_disc\_ai\_usage

</td></tr></tbody>
</table>