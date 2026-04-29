---
title: Performance insights dashboard in Service Graph Workspace
description: Use the Performance insights page in Service Graph Workspace to analyze performance of key CMDB components such as Identification and Reconciliation Engine \(IRE\), and duplicate CIs. You can review and follow recommendations to improve performance.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Insights view, Explore, Service Graph Workspace, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Performance insights dashboard in Service Graph Workspace

Use the Performance insights page in Service Graph Workspace to analyze performance of key CMDB components such as Identification and Reconciliation Engine \(IRE\), and duplicate CIs. You can review and follow recommendations to improve performance.

## Access

1.  Navigate to **Workspaces** &gt; **Service Graph Workspace**.
2.  In the navigation panel, select the Insights icon.
3.  On the Insights page navigation pane, select **Performance insights**.

Role required: sn\_cmdb\_admin

## CMDB performance insights

CMDB performance insights helps you understand the ways in which your configurations impact the performance of your CMDB. You can use the charts and tools within CMDB performance insights to troubleshoot, debug, or diagnose performance issues. CMDB performance insights also analyzes your CMDB and Service Graph Connectors on your instance to generate recommendations on how you can improve the performance of your CMDB. The CMDB performance insights tile itself can show up to two of those recommendations.

Select **View performance insights** to access the CMDB performance insights data.

The Payloads &amp; CIs tab contains the following tiles:

-   **Partial payloads**

    Partial payloads occur when the data source didn't provide enough information to uniquely identify the CI, preventing IRE from processing the CI.

    -   Total partial payload count:

        Shows the total number of partial payloads that exist in your instance. Large numbers of partial payloads in your instance can cause performance deterioration of the CMDB.

        For more information about partial payloads, see [Identification and Reconciliation Engine \(IRE\)](ire.md).

    -   Discovery source:

        Breaks down the number of partial payloads by discovery sources. You can drill down on slices in this pie chart to see the list of partial payloads with errors, filtered by discovery source.

        You can drill down on specific partial payloads to better understand the error that you're experiencing. When you drill down on a partial payload, you can see the full payload item, which you can review to troubleshoot and address the specific errors.

        For more information about error types, see [Using identification simulation](identification-simulation.md#).

-   **Related records**

    Data about related records that are missing references. A record is missing a reference when the **Referenced** field for that record is empty.

    -   Related records missing reference:

        Shows the total number of records that do not reference a CI in the **Referenced** field in the Related table. You can see a full list of the Related tables and the associated **Referenced** fields in the Related Entries \[cmdb\_related\_entry\] table.

        For more information about Related tables, see [Overview of CMDB](cnfig-mgmt-and-cmdb.md).

    -   Related records missing reference by table:

        Breaks down the number of CMDB records missing references, by table. You can drill down on slices in this chart to see the list of specific records filtered by table.

        Before you can drill down on a slice of this pie chart, you must have any user roles required to view the table.

        You can also select **New** from the list view to create a new related entry table record. For more information about creating or editing a related entry table record, see [Edit a related table from CMDB performance insights](../task/insights-update-record-rltd-table.md).

-   **Duplicate and stale CIs**

    A CI is flagged as duplicate during identification and reconciliation. A CI is flagged as stale if it has not been updated within the Effective Duration time period specified in the [CMDB Health staleness rule](../task/t_CreateCMDBHealthStaleRule.md) for the CI class.

    -   CIs:

        Shows the number of CIs that are either duplicate or stale.

    -   Stale records by class:

        Breaks down the number of stale CIs based on the CI class. You can drill down on slices in this pie chart to see the list of specific CI records filtered by class.

        For more information about stale CIs, see [CMDB Health KPIs and metrics](../reference/r_CMDBHealthMetrics.md).

    -   Duplicate records by class:

        Breaks down the number of duplicate CIs based on the CI class. You can drill down on slices in this pie chart to see the list of specific CI records.

        For more information about duplicate CIs, see [Duplicate CIs remediation](de-duplication-tasks.md).

-   **Relationship records missing parent or child**

    Shows the trend line and number of relationship records in the CI Relationships \[cmdb\_rel\_ci\] table that are missing a parent or child CI. CIs that are missing a parent or child are considered invalid records and can have a performance impact on your instance.

-   **Recommendations**

    Recommendations on this panel include a link to the related documentation and typically enable direct access to the associated tool, feature, or system property. Expand or minimize the panel by selecting the light bulb icon.

    The first two recommendations appear on the CMDB performance insights tile of the Insights view.

    You can only see a recommendation if you have the roles needed to access the feature, tool, or system property. Users with the sn\_cmdb\_admin role can hide recommendations or adjust the order in which recommendations appear. Users can use the **Active** and **Order** fields in the CMDB WS Imp Action Card Config \[sn\_cmdb\_ws\_imp\_action\_card\_config\] table to configure those elements.


The Service Graph connectors tab contains the following tiles:

**Note:**

-   The Service Graph connectors tab only appears if your instance has at least one Service Graph Connector and you have the cmdb\_inst\_admin role.
-   To edit data source or scheduled data import records in Service Graph Workspace, you may need to set **Application scope** to the **Application** of the data source or data import.

-   **Connectors data source**

    Configurations on your Service Graph Connector data sources affect the ingestion and processing of incoming data. Changing your Service Graph Connector data source configurations can streamline data handling, making your CMDB more efficient and reducing impacts on the performance of your instance.

    -   Sources with batch processing turned off:

        Shows the percentage of Service Graph Connector data sources in the Data Sources \[sys\_data\_source\] table with disabled **Use Batch Import**. It also lists the total number of data sources, and the number of data sources with enabled or disabled batch processing.

        To enable batch processing, access the record of a specific data source from the list view and select **Use Batch Import**. For more information about batch processing, see [Data source fields](https://www.servicenow.com/docs/access?context=r_DataSourceFileTypeFields&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

        You can also select **Edit** to update a data source from the list view. For more information about editing a data source, see [Edit a data source from CMDB performance insights](../task/insights-update-data-source.md).

    -   Sources with concurrent import turned off:

        Shows the percentage of scheduled data imports of Service Graph Connector data sources in the Scheduled Data Imports \[scheduled\_import\_set\] table with **Concurrent Import** turned off. It also lists the total number of scheduled data imports, and the number of scheduled data imports with **Concurrent Import** turned on or off.

        To enable concurrent import, access the record of a specific scheduled data import from the list view and select **Concurrent Import**. For more information about concurrent import, see [Concurrent imports](https://www.servicenow.com/docs/access?context=concurrent-imports&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

        You can also select **Edit** to update a scheduled data import from the list view. For more information about editing a scheduled data import, see [Edit a scheduled data import from CMDB performance insights](../task/insights-schedule-data-import.md).

    -   Sources with non-custom size partition method:

        Shows the percentage of scheduled data imports of Service Graph Connector data sources in the Scheduled Data Imports \[scheduled\_import\_set\] table that use a non-custom size partition method. It also lists the total number of scheduled data imports, and the number of scheduled data imports that use a non-custom size partition method.

        To use a custom size partition method, access the record of a specific scheduled data import from the list view. Ensure that **Concurrent Import** is selected. From the **Partition Method** drop-down menu that appears, select **Custom size**. For more information about partition methods, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

        You can also select **Edit** to update a new scheduled data import from the list view. For more information about editing a scheduled data import, see [Edit a scheduled data import from CMDB performance insights](../task/insights-schedule-data-import.md).

-   **Connectors execution trends**

    Aggregates Service Graph Connectors with outlier connector executions, where the number of imported rows or the rate of processing is significantly higher or lower than the 30-day trend.

    -   Connectors with processing rate outliers:

        Shows the number of Service Graph Connectors that are considered outliers with connector execution processing rates outside the expected trend lines within the past 30 days.

    -   Connectors with import count outliers:

        Shows the number of Service Graph Connectors that are considered outliers with connector execution import counts outside the expected trend lines within the past 30 days.

    You can drill down the cards in the Connectors execution trends tile to access the Service Graph connector execution trends window. In that windows, a Service Graph Connector is available in the connectors drop-down menu only if it has an execution record.

    Click the tabs on the Service Graph connector execution trends window to view the following charts and the Connector Execution list view of executed connector import sets:

    -   Processing rate:

        Models the trend line of processing rates for connector executions. Shows the rate at which a connector processes rows of data over a period of time.

        There are two zones, which are the Confidence Band and the Prediction Band. Service Graph Connectors with connection executions that have processing rates outside of the Prediction Band are considered outliers. These zones don't appear when you select more than one Service Graph Connector.

    -   Import count:

        Models the trend line of rows processed for connector executions. Shows the number of rows a connector processes over a period of time.

        There are two zones, which are the Confidence Band and the Prediction Band. Service Graph Connectors with connector executions that have import row counts outside of the Prediction Band are considered outliers.

    On both charts, you can select outlier and non-outlier Service Graph Connectors to see the trend lines against each other.


For more information about processing data with Service Graph Connectors, see [Getting started with Service Graph Connectors](cmdb-sgc-intro.md).

