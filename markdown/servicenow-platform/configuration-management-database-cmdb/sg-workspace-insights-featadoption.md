---
title: Feature adoption insights dashboard in Service Graph Workspace
description: Use the Feature adoption insights page in Service Graph Workspace to see and increase the level of adoption of key CMDB features and service instances to improve the overall health of the CMDB. Explore how tools and features can maximize the health and efficiency of your CMDB and use direct links to install and start using features immediately.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 12
breadcrumb: [Insights view, Explore, Service Graph Workspace, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Feature adoption insights dashboard in Service Graph Workspace

Use the Feature adoption insights page in Service Graph Workspace to see and increase the level of adoption of key CMDB features and service instances to improve the overall health of the CMDB. Explore how tools and features can maximize the health and efficiency of your CMDB and use direct links to install and start using features immediately.

## Access

1.  Navigate to **Workspaces** &gt; **Service Graph Workspace**.
2.  In the navigation panel, select the Insights icon.
3.  On the Insights page navigation pane, select **Feature adoption**.

Role required: Any role containing sn\_cmdb\_user \(sn\_cmdb\_user, sn\_cmdb\_editor, sn\_cmdb\_admin\)

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

Cards use different methods to examine the instance and determine if the card's feature is installed, activated, and being used. For example, some cards check for the installation status of plugins and some cards rely on data in the specific feature tables. Many counts and aggregation data that appear on cards is based on [Performance Analytics indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/c_Indicators.md) built on top of the Base Aggregate Data \[sn\_cmdb\_ws\_base\_aggregate\_data\] table.

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

    Determines whether the [CMDB application for APIs and CLI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-cli/cmdb-cli-commands.md) store app is installed.

    This card appears only if the store app isn't installed, providing helpful resources for exploration and adoption.


## CMDB feature adoption: Data governance

The overall adoption level for data governance maps to the following findings in the instance:

-   Low \(red\): Less than 33% of features are used
-   Moderate \(amber\): 33—66% of features are used
-   High \(green\): Over 66% of features are used

The overall level of adoption of data governance is based on whether [CMDB Data Manager](cmdb-data-management-landing.md) features are used.

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

-   **Principal classes**

    Checks if the Principal Class filter is configured with at least one principal class. The Principal Class filter limits the number of CIs that appear in list views, to show only CIs of principal classes. Reducing the amount of data in list views to only relevant data, improves performance and efficiency.

    For more information about managing the Principal Class filter in CI Class Manager, see [Update the list of classes in the Principal Class filter](../task/update-principal-class-filter.md).


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
    If CMDB Query Builder is in use, shows a chart with counts of query executions and query executions in reports, for the past six months, by month.

    Point to the chart to see monthly aggregation data.

-   **Intelligent search**

    Determines if [Intelligent Search for CMDB](intelligent-search-cmdb.md) is in use by checking the NLQ Query Logs \[nlq\_query\_log\] table for any records where **source** is **CMDB\_WS**, from the past 90 days. If Intelligent Search is in use, shows counts of Intelligent Search queries for the past six months, by month.

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


