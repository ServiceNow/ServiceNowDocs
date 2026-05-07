---
title: Create a Tableau metadata collector
description: Create a collector to import metadata from Tableau.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Tableau metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Create a Tableau metadata collector

Create a collector to import metadata from Tableau.

## Before you begin

Before you begin, verify the following:

-   A MID Server is setup for the collectors. For more information, see [MID Server for metadata collectors](../concept/mid-server-for-metadata-collectors-dc.md).
-   All per-requisite tasks are completed. For more information, see [Prepare to run the Tableau collector](prepare-to-run-tableau-collector.md#).
-   Role required: connection-admin

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Workflow Data Fabric Home**.

2.  Select the Connect Hub ![Connect Hub icon](../../../build/workflow-data-fabric/image/wdf-connect-hub-icon.png) icon in the left sidebar.

3.  Select **Create** &gt; **Metadata collector**.

4.  From the System list, select **Tableau**.

5.  Complete the form.

    |Field|Description|
    |-----|-----------|
    |Connection name|Unique identifier for the connection. This field cannot be modified once the connection is established.|
    |Short description|Purpose and details of the connection.|

6.  Configure the API base URL and authentication options.

    |Field|Description|
    |-----|-----------|
    |Tableau API base URL|Base URL for the Tableau API. For example: `https://8bank/api/3.10/.`|

7.  Configure the authentication options.

<table id="table_v3l_mj3_53c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Authenticate using username and password

</td></tr><tr><td>

Username

</td><td>

Tableau user name for authentication.

</td></tr><tr><td>

Password

</td><td>

Tableau password for authentication.

</td></tr><tr><td class="sub-head" colspan="2">

Authenticate using a private access token \(PAT\)

</td></tr><tr><td>

Tableau personal access token name

</td><td>

Tableau personal access token name.

</td></tr><tr><td>

Personal Access Token Secret

</td><td>

Tableau personal access token secret.

</td></tr><tr><td class="sub-head" colspan="2">

Authenticate using JSON Web Tokens \(JWT\)

</td></tr><tr><td>

username

</td><td>

Username associated with the connected app for JWT authentication.

</td></tr><tr><td>

Connected App Client ID

</td><td>

Client ID of the connected app required for JWT authentication.

</td></tr><tr><td>

Connected App secret ID

</td><td>

Secret ID of the connected app required for JWT authentication.

</td></tr><tr><td>

Connected App Secret Value

</td><td>

Secret value of the connected app required for JWT authentication.

</td></tr><tr><td>

JWT Token Expiration Minutes

</td><td>

Number of minutes the JWT token remains valid.Default: 5 minutes

</td></tr></tbody>
</table>8.  Configure the harvesting scope and filtering options.

<table id="table_w4z_ctp_c3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Skip cataloging of preview images

</td><td>

Option to exclude preview images from cataloging.

</td></tr><tr><td>

Tableau site

</td><td>

ID or name of the Tableau site to catalog. Leave blank to catalog all accessible sites.

</td></tr><tr><td>

Tableau pagination size

</td><td>

Number of records per page for GraphQL queries.

</td></tr><tr><td>

Tableau project

</td><td>

ID or name of the Tableau project to catalog. Leave blank to catalog all projects.**Note:** Specify nested projects individually.

</td></tr><tr><td>

Exclude object types

</td><td>

Tableau object types to exclude from cataloging.Supported object types:

-   View
-   Dashboard
-   Database
-   PublishedDataSource
-   EmbeddedDataSource
-   CalculatedField
-   ColumnField
-   BinField
-   GroupField
-   DatasourceField
-   CustomSQLTable
-   Metric


</td></tr><tr><td>

Tableau project exclude

</td><td>

ID or name of a project to exclude from cataloging. This field overrides the **Tableau project** field.

</td></tr><tr><td>

Whether to include/exclude descendant projects

</td><td>

Option to apply project settings to descendant projects.

</td></tr></tbody>
</table>9.  Configure the content and data source options

    |Field|Description|
    |-----|-----------|
    |Catalog personal space workbooks|Option to catalog personal space workbooks. Personal space workbooks are workbooks that are not associated with a project.|
    |Convert Database Identifier|Option to convert database identifiers to the default case used by the target database \(for example, lowercase for PostgresSQL, uppercase for Oracle\).|
    |Exclude Unpublished Views|Option to exclude unpublished views and dashboards from cataloging.|
    |Hostname mapping file|If you have configured hostname mapping in the [hostnames.yaml](prepare-to-run-tableau-collector.md#) file, upload the file.|
    |Exclude Hidden Fields|Option to exclude hidden fields within published data sources from cataloging.|

10. Select **Save**.


## Result

The metadata collector is created and appears on the Connectors page with a Configured status. It is now ready to connect to the source system and harvest metadata.

## What to do next

After creating the collector, you can perform any of the following tasks:

-   Run the collector manually to harvest metadata immediately. See [Run metadata collectors manually](run_metadata-collectors-manually.md).
-   Automate metadata collection by scheduling regular collector runs. See [Schedule metadata collector runs](schedule-metadata-collector-runs.md).
-   Monitor execution status and troubleshoot issues by viewing the runtime logs. See [View runtime logs for collector runs](view-runtime-logs-for-collector-runs.md).
-   Discover and evaluate the harvested data assets in the Data Catalog. See [Governing the Data Catalog](../concept/manage-data-catalog.md).

**Parent Topic:**[Tableau metadata collector](../concept/tableau-metadata-collector.md)

