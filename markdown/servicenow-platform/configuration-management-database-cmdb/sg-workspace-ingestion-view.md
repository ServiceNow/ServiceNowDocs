---
title: Ingestion view in Service Graph Workspace
description: The Overview page in the Ingestion view in Service Graph Workspace provides a centralized dashboard view for administrators to monitor the installation, performance, and error handling of Service Graph Connectors.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/sg-workspace-ingestion-view.html
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 10
breadcrumb: [Explore, Service Graph Workspace, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Ingestion view in Service Graph Workspace

The Overview page in the Ingestion view in Service Graph Workspace provides a centralized dashboard view for administrators to monitor the installation, performance, and error handling of Service Graph Connectors.

## Access

Navigate to **Workspaces** &gt; **Service Graph Workspace**, and then in the navigation panel, select the Ingestion icon.

Role required: sgc\_admin, cmdb\_inst\_admin, or admin

## Overview page features

Use the Overview page to monitor and troubleshoot your Service Graph Connectors connections through dedicated sections, filters, indicators, and visual reports and gain insights on the performance of Service Graph Connectors.

|Feature|Description|
|-------|-----------|
|[Connections overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/sg-workspace-ingestion-view.md)|Displays the current state of your configured Service Graph Connector connections, including status, execution results, and error summaries.|
|[Ingested and processed data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/sg-workspace-ingestion-view.md)|Displays key metrics related to the data imported and processed from third-party applications.|
|[Data processing performance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/sg-workspace-ingestion-view.md)|Displays how many configuration items \(CIs\) were added or updated over time, in addition to the number of processing errors.|
|[Filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/sg-workspace-ingestion-view.md)|Enables narrowing the data shown in graphs and metrics based on connector type, connection, data source, or date range.|
|[Indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/sg-workspace-ingestion-view.md)|Enables viewing of high-level metrics that reflect the volume and quality of imported data and help identify issues such as incomplete or failed import set processing.|
|[Reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/sg-workspace-ingestion-view.md)|Enables real-time visualizations that provide insights into data ingestion, processing trends, and error categorization across your Service Graph Connector connections.|

## Connections overview

Displays the current state of your configured Service Graph Connector connections, including status, execution results, and error summaries.

<table id="table_cxr_ztm_22c"><thead><tr><th>

Card

</th><th>

Description

</th><th>

Card summary table

</th></tr></thead><tbody><tr><td>

Connection status

</td><td>

Percentage of connections tested successfully based on connection status, with the count of success, error, and unknown statuses.

</td><td>

The connection status summary table displays the following details:-   **Connection**

Displays the name of the configured Service Graph Connector. Each entry links to more details about the connection.

-   **Connector type**

Displays the Service Graph Connector type as the integration source or platform for the connection.

-   **Connection status**

Displays the current state of each connection. Valid values include:

    -   **Success**

All connections were configured and tested without errors.

    -   **Error**

Connection configuration issues encountered during setup.

-   **Error summary**

Provides a short description of the most recent connection error, if any.

-   **Updated on**

Displays the timestamp of the last connection status update for each connection in the following format: `YYYY-MM-DD HH:MM:SS`.


</td></tr><tr><td>

Processing status

</td><td>

Percentage of connections for which all data import runs in the last import execution were successful, with the count of success and error statuses.**Note:**

Only import sets that encountered errors during their last execution are counted as processing errors and shown on the card.

</td><td>

The processing status summary table displays the following details:-   **Connection**

Displays the name of the configured Service Graph Connector. Each entry links to more details about the connection.

-   **Last processing status**

Indicates the result of the most recent processing run. Valid values include:

    -   **Success**

All scheduled jobs completed without errors.

    -   **Error**

One or more jobs encountered issues during processing.

-   **Activated schedules**

Indicates the number of scheduled jobs that are activated for importing the data using the connection.

-   **Processed**

Indicates the total number of import set runs that were executed for the connection.

-   **Success**

Indicates how many of the processed import set runs completed successfully.

-   **Error**

Displays the number of import set runs that ended in an error, including those import sets that were canceled.

-   **Error summary**

Provides a short description of the most recent error, if any. The summary includes error type and cause. A **View details** link may be available for diagnosing a processing error. To learn more, see [Diagnose a processing error in SGC Central](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/sgcc-diagnose-proc-errors.md).

-   **Last processed on**

Displays the timestamp of the last processing activity for the import set of the connection, including both successful and failed runs in the following format: `YYYY-MM-DD HH:MM:SS`.


</td></tr><tr><td>

Ongoing executions

</td><td>

Number of connections where data import execution is in progress.

</td><td>

The ongoing execution status summary table displays the following details:-   **Connection**

Displays the name of the configured Service Graph Connector. Each entry links to more details about the connection.

-   **Activated schedules**

Indicates the number of scheduled jobs that are activated for importing the data using the connection.

-   **In progress**

Displays how many scheduled jobs are currently running for the connection.

-   **Processed**

Displays the number of completed executions, where data has been collected and processed according to the configured scheduled job.

-   **Processing time**

Indicates the total duration taken by the most recent completed import set execution in the following format `YYYY-MM-DD HH:MM:SS`.


</td></tr></tbody>
</table>## Ingested and processed data

Displays key metrics related to the data imported and processed from third-party applications.

<table id="table_f1x_35w_x2c"><thead><tr><th>

Card

</th><th>

Description

</th><th>

Indicators

</th></tr></thead><tbody><tr><td>

Import sets

</td><td>

Number of import sets processed by data sources based on the [selected filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/sg-workspace-ingestion-view.md), with the count of success, partial, and error statuses.Select the **View all import sets** link to view a complete list of processed import sets.

</td><td>

[SGC.Integrations.ImportSet](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/sg-workspace-ingestion-view.md)

 [SGC.Fully.successful.ImportSet](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/sg-workspace-ingestion-view.md)

 [SGC.Part.success.ImportSet](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/sg-workspace-ingestion-view.md)

 [SGC.Fully.error.ImportSet](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/sg-workspace-ingestion-view.md)

</td></tr><tr><td>

Imported rows

</td><td>

Count of rows imported across all import sets based on the [selected filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/sg-workspace-ingestion-view.md).Select the **View all latest import set rows ingested** link to view a complete list of import set rows ingested.

</td><td>

[SGC.Integrations.Importset.rows.ingested](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/sg-workspace-ingestion-view.md)

</td></tr><tr><td>

CIs

</td><td>

Total CIs processed based on the [selected filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/sg-workspace-ingestion-view.md), with the count of added and updated CIs.Select the **View all inserted and updated records** link to view a complete list of inserted and updated CIs.

</td><td>

None

</td></tr><tr><td>

Partial or incomplete CIs

</td><td>

Total CIs that are partial payloads based on the [selected filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/sg-workspace-ingestion-view.md), with the count of partial and incomplete categories.Select the **View all partial and incomplete records** link to view a complete list of partial and incomplete CIs.

</td><td>

None

</td></tr></tbody>
</table>## Data processing performance

Displays how many configuration items \(CIs\) were added or updated over time, in addition to the number of processing errors.

<table id="table_o2r_n5w_x2c"><thead><tr><th>

Card

</th><th>

Description

</th><th>

Indicators

</th></tr></thead><tbody><tr><td>

CIs and errors trends

</td><td>

Daily trends for CIs that were added, updated, and any data processing errors occurred during data import process based on the [selected filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/sg-workspace-ingestion-view.md).

</td><td>

[Records added](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/sg-workspace-ingestion-view.md)

 [Records updated](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/sg-workspace-ingestion-view.md)

 [Errors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/sg-workspace-ingestion-view.md)

</td></tr><tr><td>

Processing time

</td><td>

Top 10 connections by the latest import set processing time. Select the **View all latest import sets** link to view a complete list of import sets.

</td><td>

None

</td></tr><tr><td>

Processing errors

</td><td>

Top 10 connections with the highest number of data processing errors, with a breakup by data source, connection, and credential issues.Select the **View all latest errors** link to view a complete list of processing errors.

</td><td>

None

</td></tr></tbody>
</table>## Filters

Enables narrowing the data shown in graphs and metrics based on connector type, connection, data source, or date range.

|Name|Type|Description|
|----|----|-----------|
|Connector type|List|Filters a list of installed Service Graph Connectors.|
|Connection|List|Filters a list of connection records for the Service Graph Connectors.|
|Data source|List|Filters a list of data sources for the Service Graph Connectors.|
|Date range|Date|Filters the SGC Central dashboard data based on the date range selected.|

## Indicators

Enables viewing of high-level metrics that reflect the volume and quality of imported data and help identify issues such as incomplete or failed import set processing.

-   **Records added**

    Total number of records that were inserted into the system on the previous day, as recorded in the sn\_cmdb\_int\_util\_cmdb\_integration\_execution\_audit table. The score is calculated by counting the number of records updated on the specified day, based on operations that were marked as inserted in the audit log.

-   **Records updated**

    Total number of records that were updated in the system on the previous day, as recorded in the sn\_cmdb\_int\_util\_cmdb\_integration\_execution\_audit table. The score is calculated by counting the number of records updated on the specified day, based on operations that were marked as Updated in the audit log.

-   **Records added or updated**

    Total number of records that were added or updated in the system on the previous day, as recorded in the sn\_cmdb\_int\_util\_cmdb\_integration\_execution\_audit table. The score is calculated by counting the number of records inserted or updated on the specified day, based on operations that were marked as Inserted or Updated in the audit log.

-   **Errors**

    Total number of errors categorized under credentials, data source, or connection issues that occurred during integration executions on the previous day, as recorded in the sn\_cmdb\_int\_util\_cmdb\_integration\_execution\_error table. The score is calculated by counting the number of errors on the specified day.

-   **SGC.processing.errors**

    Number of processing errors categorized under data source issues that occurred during integration executions on the previous day, as recorded in the sn\_cmdb\_int\_util\_cmdb\_integration\_execution\_error table. The score is calculated by counting the number of errors on the specified day.

-   **SGC.connection.errors**

    Total number of errors categorized under credentials or connection issues that occurred during integration executions on the previous day, as recorded in the sn\_cmdb\_int\_util\_cmdb\_integration\_execution\_error table. The score is calculated by counting the number of errors on the specified day.

-   **SGC.Integrations.ImportSet**

    Total number of import sets that were either completed successfully or encountered errors during their transformation process on the previous day, as recorded in the sn\_cmdb\_int\_util\_cmdb\_integration\_execution\_import\_set table. The score is calculated by counting the total number of import sets on the specified day.

-   **SGC.Fully.successful.ImportSet**

    Total number of import sets that were completed successfully during their transformation process on the previous day, as recorded in the sn\_cmdb\_int\_util\_cmdb\_integration\_execution\_import\_set table. The score is calculated according to this formula: `Count of import sets with Errors = 0`.

-   **SGC.Fully.error.ImportSet**

    Total number of import sets that completed with errors during their transformation process on the previous day, as recorded in the sn\_cmdb\_int\_util\_cmdb\_integration\_execution\_import\_set table. The score is calculated according to this formula: `Count of import sets with Errors ≠ 0 and Rows = Errors`.

-   **SGC.Part.success.ImportSet**

    Total number of import sets that completed with some errors where the number of rows processed differs from the number of errors reported on the previous day, as recorded in the sn\_cmdb\_int\_util\_cmdb\_integration\_execution\_import\_set table. The score is calculated according to this formula: `Count of import sets with Errors ≠ 0 and Rows ≠ Errors`.

-   **SGC.Integrations.Importset.rows.ingested**

    Total number of rows ingested for the import sets on the previous day, as recorded in the sn\_cmdb\_int\_util\_cmdb\_integration\_execution table. The score is calculated according to this formula: `Sum of rows ingested`.

-   **SGC.Integrations.Processing Rate**

    Average processing rate of import sets based on the total number of rows processed and the total processing time \(in hours\) for the import sets that either completed successfully or encountered errors on the previous day, as recorded in the sn\_cmdb\_int\_util\_cmdb\_integration\_execution table. The score is calculated according to this formula: `Sum of rows processed​/Total time (in hours)`.


## Reports

Enables real-time visualizations that provide insights into data ingestion, processing trends, and error categorization across your Service Graph Connector connections.

<table id="table_p45_1v1_cjc"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Affected CIs and errors

</td><td>

Relative compare \(\[Omitted image "relative-compare-icon.png"\] Alt text: Relative compare\)

</td><td>

CMDB Integration Execution Error \[sn\_cmdb\_int\_util\_cmdb\_integration\_execution\_error\]

</td><td>

Displays configuration items \(CIs\) added, CIs updated, and cumulative errors occurred during data import over time.

</td></tr><tr><td>

Error breakdown

</td><td>

Column \(\[Omitted image "column-icon.png"\] Alt text: Column icon\)

</td><td>

CMDB Integration Execution Error \[sn\_cmdb\_int\_util\_cmdb\_integration\_execution\_error\]

</td><td>

Displays the count of errors grouped over time.

</td></tr><tr><td>

Import set rows ingested

</td><td>

Single score \(\[Omitted image "icon-single-score-report-p.png"\] Alt text: Single score icon\)

</td><td>

CMDB Integration Execution Import Set \[sn\_cmdb\_int\_util\_cmdb\_integration\_execution\_import\_set\]

</td><td>

Displays the number of import set rows ingested in a day.

</td></tr><tr><td>

Import set processing rate

</td><td>

Single score \(\[Omitted image "icon-single-score-report-p.png"\] Alt text: Single score icon\)

</td><td>

CMDB Integration Execution \[sn\_cmdb\_int\_util\_cmdb\_integration\_execution\]

</td><td>

Displays the average rate at which an import set processes data within an hour.

</td></tr><tr><td>

Records added or updated

</td><td>

Single score \(\[Omitted image "icon-single-score-report-p.png"\] Alt text: Single score icon\)

</td><td>

CMDB Integration Execution Audit \[sn\_cmdb\_int\_util\_cmdb\_integration\_execution\_audit\]

</td><td>

Displays the number of records that were updated or added for CI classes.

</td></tr><tr><td>

Total import sets

</td><td>

Single score \(\[Omitted image "icon-single-score-report-p.png"\] Alt text: Single score icon\)

</td><td>

CMDB Integration Execution Import Set \[sn\_cmdb\_int\_util\_cmdb\_integration\_execution\_import\_set\]

</td><td>

Displays the number of import sets initialized by data sources in the given time frame and the count of import sets categorized by their status.

</td></tr><tr><td>

Updated classes

</td><td>

Column \(\[Omitted image "column-icon.png"\] Alt text: Column icon\)

</td><td>

CMDB Integration Execution Audit \[sn\_cmdb\_int\_util\_cmdb\_integration\_execution\_audit\]

</td><td>

Displays the breakdown of updated and inserted CIs for a class.

</td></tr></tbody>
</table>