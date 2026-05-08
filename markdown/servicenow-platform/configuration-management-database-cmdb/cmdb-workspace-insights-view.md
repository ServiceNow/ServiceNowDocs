---
title: Insights view in CMDB Workspace
description: Use the Insights view in CMDB Workspace to see and increase the level of adoption of key CMDB features and application services to improve the overall health of the CMDB. Explore how tools and features can maximize the health and efficiency of your CMDB and use direct links to install and start using features immediately.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 25
breadcrumb: [Explore, CMDB Workspace, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Insights view in CMDB Workspace

Use the Insights view in CMDB Workspace to see and increase the level of adoption of key CMDB features and application services to improve the overall health of the CMDB. Explore how tools and features can maximize the health and efficiency of your CMDB and use direct links to install and start using features immediately.

## Access

Role requirement: sn\_cmdb\_user \(CMDB User\), or a user role containing sn\_cmdb\_user \(sn\_cmdb\_admin, sn\_cmdb\_editor\).

To access the Insights view, navigate to **Workspaces** &gt; **CMDB Workspace** and then select **Insights** in the CMDB Workspace menu bar.

The Insights view includes the following tiles:

-   CMDB feature adoption
-   CMDB performance insights
-   Application services
-   Cloud vs Non-cloud resources

## CMDB feature adoption

Shows dial charts for the overall adoption levels of all three categories of CMDB tools and features:

-   **Data ingestion**

    Tools and features that support and ensure ingestion of high-quality data into the CMDB.

-   **Data governance**

    Tools and features that let you manage the CMDB data after it has been ingested.

-   **Search and analytics**

    Tools and features that provide meaningful and helpful insights into the CMDB data.


Select each dial chart in the tile to access its tab and associated cards with further details about the features in the category. Pay special attention to categories with low levels of adoption and those features that aren't yet implemented in the instance and which you should consider for adoption.

Each category tab shows cards for the features in the category and the following general cards:

-   Overall adoption level for the tab: The calculated overall level of adoption for the tab. Calculations are specific for each tab, and can be based, for example, on the level of adoption of some or all the features in the tab.
-   Adoption progress: Installation, activation, or usage status per feature in the tab. Select a feature link to access a relevant resource such as the feature's landing page with an overview dashboard or an installation location.

Depending on adoption level, a card might contain any of the following resource links:

-   **Learn more**: Link to documentation to learn and explore the benefits and usage of the feature.
-   **View demo**: Link to a short demo about the feature.
-   **Get started**: Link to a landing page where you can start immediately utilizing the feature.
-   **Install app**: Link to the ServiceNow Store where you can immediately install the app.

Cards use different methods to examine the instance and determine if the card's feature is installed, activated, and being used. For example, some cards check for the installation status of plugins and some cards rely on data in the specific feature tables. Many counts and aggregation data that appear on cards is based on Performance Analytics indicators built on top of the Base Aggregate Data \[sn\_cmdb\_ws\_base\_aggregate\_data\] table.

-   If the result is that the card's feature is installed or being used, then the card shows charts and counts about the level of usage. In which case, the card's label might slightly adjust.
-   If the result is that the card's feature isn't installed or isn't in use, then links are provided to resources where you can explore, install, and start using the feature.

Most of the cards scheduled jobs run every 24 hours, therefore, depending on the type of data, some card data is based on recent but not current data. The Last updated timestamp in the cards reflects the collection time for the data that was used for the card. Also, immediately after getting started with a feature, a card won't reflect on the latest status or usage of the feature, until up to 24 hours when the card's scheduled job runs \(for the CIs processed by IRE based on source card, the associated scheduled job, CMDB Workspace - Populate aggregates Monthly, runs monthly\).

The following sections provide details for each card, including the calculation script used for the card.

## CMDB feature adoption: Data ingestion

The overall adoption level for data ingestion maps to the following findings in the instance:

-   Low \(red\): Less than 80% of CIs are processed by Identification and Reconciliation Engine \(IRE\)
-   Moderate \(amber\): 80—90% of CIs are processed by IRE
-   High \(green\): Over 90% of CIs are processed by IRE

Data ingestion contains the following features and aggregations:

-   **CIs processed by IRE**

    Determines the percentage of CIs that are processed by [IRE](c_CMDBIdentifyandReconcile.md), by checking the Source \[sys\_object\_source\] table. CIs that aren't processed by IRE introduce a data integrity risk.

    The percentage of CIs that are being processed by IRE determines both, the level of adoption for this feature card and the overall adoption level for the entire data ingestion category.

-   **Service Graph Connectors**

    Determines the installation and usage status of [Getting started with Service Graph Connectors](cmdb-sgc-intro.md), by checking:

    -   If the ITOM Licensing plugin \(com.snc.itom.license\) is active
    -   If there is at least one Service Graph Connector installed in the instance
    If Service Graph Connectors are installed and are in use, then the card shows a count of those connectors.

    **Note:** The count of Service Graph connectors that appears on the card might be slightly different than the number of connectors that show on the ServiceNow Store site because the counting methods that are used are different.

-   **IntegrationHub ETL**

    Determines whether the [IntegrationHub ETL](integrationhub-etl.md) store app is installed and used, based on records in the CMDB Integration Studio Application Data Sources \[cmdb\_inst\_application\_feed\] table. If IntegrationHub ETL is in use, then the card shows a count of ETL transform maps in IntegrationHub ETL \(demo ETL transform maps aren't counted\).

    Select **View ETL transform maps** to open IntegrationHub ETL where you can examine existing ETL transform maps and create new ones.

-   **CIs processed by IRE based on source**

    Chart showing CIs processed by IRE, grouped by Service Graph Connectors, ServiceNow Discovery, a combination of both, and others, for the past six months.

    The following discovery sources are counted as ServiceNow Discovery​:

    -   ServiceNow
    -   ServiceWatch​
    -   ACC-Visibility​
    -   AgentClientCollector
    -   CredentiallessDiscovery
    Point to the chart to show monthly aggregation data.

    This card is hidden if there are no CIs processed by IRE.

-   **CMDB application for APIs and CLI**

    Determines whether the CMDB application for APIs and CLI store app is installed.

    This card appears only if the store app isn't installed, providing helpful resources for exploration and adoption.


## CMDB feature adoption: Data governance

The overall adoption level for data governance maps to the following findings in the instance:

-   Low \(red\): Less than 33% of features are used
-   Moderate \(amber\): 33—66% of features are used
-   High \(green\): Over 66% of features are used

The overall level of adoption of data governance is based on whether [CMDB Data Manager](cmdb-data-management-landing.md) features are used.

**Note:** Historical data might not be available for all past 90 days because CMDB Workspace version 3.4, which relies on Performance Analytics indicators to collect and save historical usage data, was deployed less than 90 days ago. This situation might result in a discrepancy between actual usage and what the card shows.

-   **CMDB Data Manager/CIs used in Data Manager policies**

    Determines usage by checking if either of the following conditions is true:

    -   There are any user-created Delete, Retire, or Archive policies \(by searching table CMDB Data Manager Policy and Attributes \[cmdb\_data\_manager\_policy\_and\_attributes\]\)
    -   There are any CIs processed by these user-created Delete, Retire, or Archive policies, in the last 90 days \(by searching table CMDB Data Management Policy Executions \[cmdb\_data\_management\_policy\_execution\]\)
    If CMDB Data Manager is in use, shows a chart with CIs that were processed by these policies in the past six months, by month, and by policy type.

-   **Data attestation/CIs used in data attestation**

    Determines usage by checking if either of the following conditions is true:

    -   There are any user-created [Attestation policies](attesting-cis.md) \(by searching table CMDB Data Manager Policy and Attributes \[cmdb\_data\_manager\_policy\_and\_attributes\]\)
    -   There are any CIs processed by these user-created Attestation policies, in the last 90 days \(by searching table CMDB Data Management Policy Executions \[cmdb\_data\_management\_policy\_execution\]\)
    If data attestation is in use, shows a chart with CIs that were processed by attestation policy tasks in the past six months, by month.

-   **Data synchronization**

    Checks if there is at least one class for which the **managed\_by\_group** attribute is globally set so that all class CIs are synchronized on the same value.

    For information about synchronizing group assignment attributes using the CI Class Manager, see [Set the group for a CI or an entire class of CIs](../../csdm-implementation/task/csdm-data-synchronize-enable.md) and [Synchronizing group assignment attributes](../../csdm-implementation/concept/csdm-data-synchronize.md).

    The Data synchronization card is available starting with CMDB Workspace v3.6.

-   **Principal classes**

    Checks if the Principal Class filter is configured with at least one principal class. The Principal Class filter limits the number of CIs that appear in list views, to show only CIs of principal classes. Reducing the amount of data in list views to only relevant data, improves performance and efficiency.

    For more information about managing the Principal Class filter in CI Class Manager, see [Update the list of classes in the Principal Class filter](../task/update-principal-class-filter.md).

    The Principal class card is available starting with CMDB Workspace v3.6.


## CMDB feature adoption: Search &amp; analytics

The overall adoption level for search &amp; analytics maps to the following findings in the instance:

-   Low \(red\): Less than 33% of features are used
-   Moderate \(amber\): 33—66% of features are used
-   High \(green\): Over 66% of features are used

Search &amp; analytics contains the following features and aggregations:

-   **CMDB Query Builder/Query Builder queries**

    Determines if the [CMDB Query Builder](querying-cmdb.md) is in use, by checking if either of the following conditions is true:

    -   There are any records in the Saved Queries \[qb\_saved\_query\] table in which **Source** is **QB**
    -   There are any queries executed or queries executed with reports, in the last 90 days

        **Note:** Historical data might not be available for all past 90 days because CMDB Workspace version 3.4, which relies on Performance Analytics indicators to collect and save historical usage data, was deployed less than 90 days ago. This situation might result in a discrepancy between actual usage and what the card shows.

    If CMDB Query Builder is in use, shows a chart with counts of query executions and query executions in reports, for the past six months, by month.

    Point to the chart to see monthly aggregation data.

-   **Intelligent search**

    Determines if [Intelligent Search for CMDB](intelligent-search-cmdb.md) is in use by checking the NLQ Query Logs \[nlq\_query\_log\] table for any records where **source** is **CMDB\_WS**, from the past 90 days. If Intelligent Search is in use, shows counts of Intelligent Search queries for the past six months, by month.

    **Note:** Historical data might not be available for all past 90 days because CMDB Workspace version 3.4, which relies on Performance Analytics indicators to collect and save historical usage data, was deployed less than 90 days ago. This situation might result in a discrepancy between actual usage and what the card shows.

-   **CMDB 360 — Records in Multisource**

    Total number of raw [CMDB 360](multisource-cmdb.md) records in the CMDB 360 data store that contains records for each discovery source report, per each CI attribute. This card is identical to the [Total CMDB 360 records](cmdb360-exp-cmdb-workspace.md) card in the Discovery Sources tile in the CMDB 360 view.

    This card appears only if CMDB 360 is enabled, which is determined by checking the ITOM Discovery License \(com.snc.itom.discovery.license\) plugin and the system property [glide.identification\_engine.multisource\_enabled](../reference/components-multisource-cmdb.md).

-   **CMDB 360 queries**

    Count of CMDB 360 queries that exist in the CMDB Multisource Queries \[cmdb\_multisource\_query\] table.

    This card appears only if CMDB 360 is enabled, which is determined by checking the ITOM Discovery License \(com.snc.itom.discovery.license\) plugin and the system property [glide.identification\_engine.multisource\_enabled](../reference/components-multisource-cmdb.md).

-   **CMDB Data Foundation dashboard**

    Determines if the [CMDB and CSDM Data Foundations Dashboards](csdm-cmdb-foundations-dashboards.md) store app \(which includes the CMDB Data Foundation dashboard\) is installed.

    This card appears only if the store app isn't installed, providing helpful resources for exploration and adoption. However, the feature is still included in calculating the search &amp; analytics overall level of adoption.

-   **CMDB Health Dashboard**

    Determines if [CMDB Health](c_CMDBHealth.md) is in use by checking if at least one CMDB Health Dashboard job is enabled.

    This card appears only if the feature isn't in use, providing helpful resources for exploration and adoption. However, the feature is still included in calculating the search &amp; analytics overall level of adoption.


## CMDB performance insights

CMDB performance insights is available starting with CMDB Workspace v3.6 and only appears for users with the sn\_cmdb\_admin \(CMDB Admin\) role.

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
-   To edit data source or scheduled data import records from CMDB Workspace, you may need to set **Application scope** to the **Application** of the data source or data import.

-   **Connectors data source**

    Configurations on your Service Graph Connector data sources affect the ingestion and processing of incoming data. Changing your Service Graph Connector data source configurations can streamline data handling, making your CMDB more efficient and reducing impacts on the performance of your instance.

    -   Sources with batch processing turned off:

        Shows the percentage of Service Graph Connector data sources in the Data Sources \[sys\_data\_source\] table with disabled **Use Batch Import**. It also lists the total number of data sources, and the number of data sources with enabled or disabled batch processing.

        To enable batch processing, access the record of a specific data source from the list view and select **Use Batch Import**. For more information about batch processing, see Data source fields.

        You can also select **Edit** to update a data source from the list view. For more information about editing a data source, see [Edit a data source from CMDB performance insights](../task/insights-update-data-source.md).

    -   Sources with concurrent import turned off:

        Shows the percentage of scheduled data imports of Service Graph Connector data sources in the Scheduled Data Imports \[scheduled\_import\_set\] table with **Concurrent Import** turned off. It also lists the total number of scheduled data imports, and the number of scheduled data imports with **Concurrent Import** turned on or off.

        To enable concurrent import, access the record of a specific scheduled data import from the list view and select **Concurrent Import**. For more information about concurrent import, see Concurrent imports.

        You can also select **Edit** to update a scheduled data import from the list view. For more information about editing a scheduled data import, see [Edit a scheduled data import from CMDB performance insights](../task/insights-schedule-data-import.md).

    -   Sources with non-custom size partition method:

        Shows the percentage of scheduled data imports of Service Graph Connector data sources in the Scheduled Data Imports \[scheduled\_import\_set\] table that use a non-custom size partition method. It also lists the total number of scheduled data imports, and the number of scheduled data imports that use a non-custom size partition method.

        To use a custom size partition method, access the record of a specific scheduled data import from the list view. Ensure that **Concurrent Import** is selected. From the **Partition Method** drop-down menu that appears, select **Custom size**. For more information about partition methods, see Schedule a data import.

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

## Cloud vs Non-cloud resources

Charts showing counts and details for resourcesand application services that are hosted on various cloud services versus those that aren't. Resourcesand application services can be deployed on cloud services such as the Microsoft Azure Cloud, or on the local instance or other non-cloud solutions. For some ongoing operations in the organization, it might be necessary to have those details which can be difficult to obtain.

For details about the charts, see 'Cloud vs Non-cloud resources' in the [Home view in CMDB Workspace](cmdb-workspace-home-view.md) topic.

## Application services

Shows a count of [application services](application-services.md) in your organization, based on records in the Service Instance \[cmdb\_ci\_service\_auto\] table. The chart shows the trend of total number of application services per day, for the past seven days.

Select the tile to access the Application Services dashboard where you can monitor the adoption level and health of application services. For details about the Application Services dashboard, see [Use Service instance \(Application Services\) dashboard to monitor health](../task/app-service-dashboard.md).

**Parent Topic:**[Exploring CMDB Workspace](exploring-cmdb-workspace.md)

