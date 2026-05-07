---
title: Create a dbt Cloud metadata collector
description: Create a collector to import metadata from dbt Cloud.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [dbt Cloud metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Create a dbt Cloud metadata collector

Create a collector to import metadata from dbt Cloud.

## Before you begin

Before you begin, verify the following:

-   A MID Server is setup for the collectors. For more information, see [MID Server for metadata collectors](../concept/mid-server-for-metadata-collectors-dc.md).
-   All per-requisite tasks are completed. For more information, see [Prepare to run the dbt Cloud collector](prepare-to-run-dbt-cloud-collector.md#).
-   Role required: connection-admin

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Workflow Data Fabric Home**.

2.  Select the Connect Hub ![Connect Hub icon](../../../build/workflow-data-fabric/image/wdf-connect-hub-icon.png) icon in the left sidebar.

3.  Select **Create** &gt; **Metadata collector**.

4.  From the System list, select **dbt Cloud**.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection name|Unique identifier for the connection. This field cannot be modified once the connection is established.|
    |Short description|Purpose and details of the connection.|

6.  Enter the dbt Cloud configuration details.

    |Field|Description|
    |-----|-----------|
    |dbt Cloud API key|A dbt cloud-issued API key with permissions to access the specified account.|
    |dbt Cloud host|The host for your organization's account on dbt cloud. If left unspecified, the default host is assumed as cloud.getdbt.com.|
    |dbt cloud account ID|The dbt cloud account that owns the project from which to harvest dbt metadata artifacts.|
    |dbt Cloud project|The name or numeric identifier of the project from which to harvest dbt metadata artifacts.|
    |dbt cloud run ID|The numeric identifier of the run that produced the artifacts to be harvested. If not specified, the most recent successful run that produced artifacts within the project is harvested.|
    |dbt Cloud environment|The dbt Cloud environment \(ID or name\) used to filter the job runs from which to harvest dbt metadata artifacts.|
    |dbt Cloud job|The dbt Cloud job \(ID or name\) used to filter the job runs from which to harvest dbt metadata artifacts.|

7.  Enter the target database details.

    **Note:** You must set the **Target database** to **Snowflake overrides** to harvest Snowflake lineage relationships between columns specified through views.

<table id="table_u5c_5nv_33c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Target database

</td><td>

Option to override the database connection information configured on the Project in dbt cloud -   **No Target database overrides**: Enables the collector to skip connecting to a data warehouse and only harvest dbt assets. No lineage is available for views
-   **Snowflake overrides**: Select to harvest Snowflake lineage relationships between columns specified through views


</td></tr><tr><td class="sub-head" colspan="2">

Authentication \(Snowflake overrides\)

</td></tr><tr><td>

Authentication

</td><td>

Authentication method to use if **Snowflake overrides** is selected -   **No Snowflake authentication overrides**
-   **Snowflake username and password overrides**
-   **Snowflake private key file overrides**
**Note:** If you select Snowflake overrides and don't provide any authentication details, the collector obtains connection information \(Snowflake account, role, and warehouse\) from the identified dbt Cloud run.

</td></tr><tr><td class="sub-head" colspan="2">

Snowflake username and password overrides

</td></tr><tr><td>

Database username

</td><td>

User credential to use in connecting to the target database

</td></tr><tr><td>

Database password

</td><td>

Password credential to use in connecting to the target database

</td></tr><tr><td class="sub-head" colspan="2">

Snowflake private key file overrides

</td></tr><tr><td>

Database username

</td><td>

Username to use in connecting to the target database

</td></tr><tr><td>

Snowflake key file path

</td><td>

Private key file to use for authentication with Snowflake \(for example rsa\_key.p8\). Use this option to override the dbt profile

</td></tr><tr><td>

Snowflake key file password

</td><td>

Password for the private key file if the key is encrypted and a password was set. Use this option to override the dbt profile or cloud configuration

</td></tr><tr><td class="sub-head" colspan="2">

Other optional settings

</td></tr><tr><td>

Snowflake application

</td><td>

Application connection parameter to use in connecting to the target Snowflake database. Use this option to override the dbt profile or cloud configuration Default: datadotworld

</td></tr><tr><td>

Snowflake account

</td><td>

Snowflake account or tenant

</td></tr><tr><td>

Snowflake role

</td><td>

Role to use in connecting to the target Snowflake database. Use this option to override the dbt profile or cloud configuration. This field is case-insensitive

</td></tr><tr><td>

Snowflake warehouse

</td><td>

Warehouse to use in connecting to the target Snowflake database. Use this option to override the dbt profile or cloud configuration. This field is case-insensitive

</td></tr></tbody>
</table>8.  Enter the advanced options.

<table id="table_yhb_plp_33c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Max retries

</td><td>

The number of times the system retries a failed API call.Default: 5

</td></tr><tr><td>

Retry delay

</td><td>

The number of seconds to wait between retry attempts for a failed API call.Default: 2 seconds

</td></tr><tr><td>

API HTTP header

</td><td>

Name-value pairs included as HTTP headers in API calls made by the collector. Add one value per line to specify multiple headers.

</td></tr><tr><td>

JDBC driver properties

</td><td>

JDBC driver properties to pass through to driver connection. Specify multiple JDBC driver properties by adding one value per line.If you are using the NTLM authentication, you must set two JDBC properties as:

-   integratedSecurity=true
-   authenticationScheme=NTLM


</td></tr></tbody>
</table>9.  Select **Save**.


## Result

The metadata collector is created and appears on the Connectors page with a Configured status. It is now ready to connect to the source system and harvest metadata.

## What to do next

After creating the collector, you can perform any of the following tasks:

-   Run the collector manually to harvest metadata immediately. See [Run metadata collectors manually](run_metadata-collectors-manually.md).
-   Automate metadata collection by scheduling regular collector runs. See [Schedule metadata collector runs](schedule-metadata-collector-runs.md).
-   Monitor execution status and troubleshoot issues by viewing the runtime logs. See [View runtime logs for collector runs](view-runtime-logs-for-collector-runs.md).
-   Discover and evaluate the harvested data assets in the Data Catalog. See [Governing the Data Catalog](../concept/manage-data-catalog.md).

**Parent Topic:**[dbt Cloud metadata collector](../concept/dbt-cloud-metadata-collector.md)

