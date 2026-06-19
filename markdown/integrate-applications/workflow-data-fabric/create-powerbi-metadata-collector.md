---
title: Create a PowerBI metadata collector
description: Create a collector to import metadata from PowerBI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/create-powerbi-metadata-collector.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [PowerBI metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Create a PowerBI metadata collector

Create a collector to import metadata from PowerBI.

## Before you begin

Before you begin, verify the following:

-   A MID Server is setup for the collectors. For more information, see [MID Server for metadata collectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/mid-server-for-metadata-collectors-dc.md).
-   All per-requisite tasks are completed. For more information, see [Prepare to run the PowerBI collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/prepare-to-run-powerbi-collector.md).
-   Role required: connection-admin

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Workflow Data Fabric Home**.

2.  Select the Connect Hub \[Omitted image "wdf-connect-hub-icon.png"\] Alt text: Connect Hub icon icon in the left sidebar.

3.  Select **Create** &gt; **Metadata collector**.

4.  From the System list, select **PowerBI**.

5.  From the Connection type list, select one of the following:

    1.  Select **New connection** to configure a new connection.

    2.  Select **Existing connection** to reuse an existing connection and select an existing connection from the **Connections** list.

        The configuration form is filled with details from the existing connection. The name is appended with the word Copy and sensitive details like password aren't copied.

6.  Complete the form.

    |Field|Description|
    |-----|-----------|
    |Connection name|Unique identifier for the connection. This field can't be modified once the connection is established.|
    |Short description|Purpose and details of the connection.|

7.  Configure the authentication options.

    |Field|Description|
    |-----|-----------|
    |Authenticate using Azure username and password|Azure Active Directory username and password. Set the Azure Tenant ID if you want to specify the Azure tenant ID while using the user name and password authentication.|
    |Authenticate using Azure Service principal|Azure Active Directory application tenant ID for Power BI app. To find the tenant ID, select the question mark in the Power BI app and then choose About Power BI. The tenant ID is found at the end of the Tenant URL.|

8.  Configure the client ID and client secret details.

    |Field|Description|
    |-----|-----------|
    |Microsoft Entra client ID|Application client ID for the PowerBI app.|
    |Microsoft Entra client secret|Application client secret for the PowerBI app.|

9.  Configure the workspace scope and filters options.

<table id="table_qpw_5xc_j3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Disable Lineage collection

</td><td>

Option to skip harvesting lineage metadata from Power BI source expressions.

</td></tr><tr><td>

Catalog contents of user's My Workspace

</td><td>

Option to catalog the contents of a user's My Workspace in Power BI. Default: Skip the user's workspace.

</td></tr><tr><td>

Catalog all workspaces and apps in tenant

</td><td>

Option to catalog all workspaces and apps in a tenant, rather than only the workspaces and apps the credentials have explicit access to. Admin privileges are required for the credentials used.

</td></tr><tr><td>

Include Power BI workspace\(s\)

</td><td>

Workspaces to collect. Enter the exact workspace name or a regular expression to match. **Note:** If a workspace name includes special characters \[. , + , \* , ? , ^ , $ , \( , \) , \[ , \] , \{ , \} , \| , \\\], escape each special character with a backslash \(\\\). For example, enter Workspace \\\(Dev\\\) for Workspace \(Dev\).

</td></tr><tr><td>

Exclude Power BI Workspaces

</td><td>

Power BI workspaces and their contents to exclude from cataloging. Enter the exact workspace name or a regular expression to match. If both Include Workspaces and Exclude Workspaces are configured, Include Workspaces takes precedence. **Note:** If a workspace name includes special characters \[. , + , \* , ? , ^ , $ , \( , \) , \[ , \] , \{ , \} , \| , \\\], escape each special character with a backslash \(\\\). For example, enter Workspace \\\(Dev\\\) for Workspace \(Dev\).

</td></tr></tbody>
</table>10. Configure the connection and reliability options.

<table id="table_yhb_plp_33c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Maximum Power BI Expression Length

</td><td>

Maximum number of characters in a Power BI expression that is parsed for lineage metadata. Expressions longer than this value are skipped. Default: 32000

</td></tr><tr><td>

Datasource Name Mapping File

</td><td>

File that maps ODBC source details configured in the [datasources.yml](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/prep-to-run-powerbi-collector-lineage-mapping.md)file. Upload the file if you have configured ODBC source details.

</td></tr><tr><td>

Catalog report preview images

</td><td>

Option to catalog preview images. Default: false

</td></tr><tr><td>

Disable max requests wait

</td><td>

Option to disable waiting for the Power BI API to reset throttling limits \(error code 429\). When not selected, the collector retries every 5 minutes for up to an hour. When selected, the Max retries and Retry delay settings are used instead.

</td></tr><tr><td>

Max retries

</td><td>

Number of times the system retries a failed API call. Default: 5

</td></tr><tr><td>

Retry delay

</td><td>

Number of seconds to wait between retry attempts for a failed API call. Default: 2 seconds

</td></tr></tbody>
</table>11. Select **Save**.


## Result

The metadata collector is created and appears on the Connectors page with a Configured status. It is now ready to connect to the source system and harvest metadata.

## What to do next

After creating the collector, you can perform any of the following tasks:

-   Run the collector manually to harvest metadata immediately. See [Run metadata collectors manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/run_metadata-collectors-manually.md).
-   Automate metadata collection by scheduling regular collector runs. See [Schedule metadata collector runs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/schedule-metadata-collector-runs.md).
-   Monitor execution status and troubleshoot issues by viewing the runtime logs. See [View runtime logs for collector runs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/view-runtime-logs-for-collector-runs.md).
-   Discover and evaluate the harvested data assets in the Data Catalog. See [Governing the Data Catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/manage-data-catalog.md).

**Parent Topic:**[PowerBI metadata collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/powerbi-metadata-collector.md)

