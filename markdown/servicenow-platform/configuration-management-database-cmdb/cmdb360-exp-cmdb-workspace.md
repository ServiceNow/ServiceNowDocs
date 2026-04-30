---
title: CMDB 360 experience in CMDB Workspace and in Service Graph Workspace
description: The CMDB 360 view in CMDB Workspace and in Service Graph Workspace provides aggregations and analysis of CMDB 360 data which you can use to track activities and identify Potential issues of discovery sources. You can also create different types of your own queries and associated schedules and reports to explore CMDB data.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 9
breadcrumb: [CMDB 360/Multisource CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB 360 experience in CMDB Workspaceand in Service Graph Workspace

The CMDB 360 view in CMDB Workspace and in Service Graph Workspaceprovides aggregations and analysis of CMDB 360 data which you can use to track activities and identify Potential issues of discovery sources. You can also create different types of your own queries and associated schedules and reports to explore CMDB data.

Use the CMDB 360 view in [CMDB Workspace](cmdb-workspace.md)or the CMDB 360 insights page in [Service Graph Workspace store app](sg-workspace.md), to access all of the CMDB 360 capabilities. For information about all CMDB 360 dashboard settings, see [Configure the CMDB 360 dashboard in CMDB Workspace or in Service Graph Workspace](../task/workspc-mltsrc-configure.md).

**Note:** Most cards on the CMDB 360 dashboard support non-CMDB tables in their aggregation, or can be configured to provide support. However, the CIs not reported by discovery sources card, for example, doesn't apply to non-CMDB tables. Creating queries for non-CMDB tables is also supported. For information about support for non-CMDB tables, see [IRE support for non-CMDB tables](ire-support-non-cmdb-tables.md).

## Access

Requirements:

-   Role requirement: sn\_cmdb\_user \(CMDB user\) or any role containing sn\_cmdb\_user
-   Additional requirement: [Enable and configure CMDB 360](multisource-cmdb.md#section_enable_multisource_CMDB)

To access the CMDB 360 view experience:

-   In Service Graph Workspace: Navigate to **Workspaces** &gt; **Service Graph Workspace**. Then, in the navigation panel, select the Insights icon and in the Insights page navigation panel, select **CMDB 360**
-   In CMDB Workspace: Navigate to **Workspaces** &gt; **CMDB Workspace**, and then in the CMDB Workspace menu bar, select **CMDB 360**.

## Potential issues

Cards on the Potential issues tile show details about CIs with discovery sources that are incorrectly reporting on the CIs.

-   **CIs not reported by discovery sources**

    Lists CIs that are discovered by multiple discovery sources, but one or more of the discovery sources has stopped reporting within a specified number of days. The [Number of days since CIs were last discovered by a discovery source](../task/workspc-mltsrc-configure.md#substeps_my2_p3z_dvb) dashboard setting is used in the card's aggregation.

    Drill down on this card to see a list view of the CIs for the card and the specific discovery source per CI that is no longer reporting.

    Example: You configure 7 days for the setting. A Linux server CI named backup-linux.sea.com is reported by these discovery sources within the specified number of days:

    -   ServiceNow - today.
    -   ServiceWatch - 4 days ago.
    -   AgentClientCollector - 8 days ago.
    In this scenario, the CI shows on the CIs not reported by discovery sources card, since AgentClientCollector reported over seven days ago.

-   **Data mismatch**

    Lists CIs for which different discovery sources are reporting different values. Attributes are considered mismatched when different discovery sources report different values for the attribute. CIs that appear when you drill down on this card can reveal issues with the individual CI, or your reconciliation rules.

    The specific records that appear in the drilled-down list view, depend on the [Data mismatch](../task/workspc-mltsrc-configure.md#substeps_my2_p3z_dvb) dashboard settings.

    In the Data mismatch records list view, select an item in a Source column to access the Multisource Data Preview page with details about all discovery sources with values for the attribute. On the Multisource Data Preview page you can use the Search Attributes box to search for specific attributes and also choose one of the following options:

    -   **All attributes**: Shows all attributes of the selected class, regardless of whether they have a value in the CMDB.
    -   **Attributes with CMDB values**: Shows only attributes of the selected class, with a value in the CMDB.
    -   **Attributes with multisource data**: Shows all attributes of the selected class, and for each attribute shows current CMDB value and any other discovery sources with a value for the attribute.
    Regardless of the option that you choose on the Multisource Data Preview page, a discovery source value that was used for the current CMDB value – is highlighted in green. These values are identical to the CMDB value of the attribute.


## Saved queries

The Saved queries card shows up to 20 of your CMDB 360 queries. You can use the card to edit and run those queries, or create new queries. Saved queries are sorted on both the card and list view by the most recently created or updated queries.

If your instance has been upgraded from an instance that contained Multisource Report Builder queries, then those queries appear on the Saved queries card.

-   Click a saved query to modify or view it before running.
-   Click a query's action icon and then select **Run**.
-   Click **View All Queries** to see all the Saved queries where you can examine or run a query.
-   Click **Create Query** to create a query of one of the following types:
    -   [Get Records](../task/workspc-mltsrc-query-get-records.md): Creates a query that you can use to explore your CMDB 360 data. It queries your CMDB 360 for CIs matching your criteria that are reported by specified discovery sources.
    -   [Find Gap](../task/workspc-mltsrc-query-find-gap.md): Creates a query that you can use to analyze gaps in discovery sources reporting your CMDB 360 data. It queries discovery sources that report CIs against discovery sources that don't report those same CIs.
    -   [Compare Attribute Values](../task/workspc-mltsrc-query-comp-attr-value.md): Creates a query that you can use to identify CIs with attribute values that differ across multiple discovery sources or against the CMDB. It queries at least two discovery sources and/or the CMDB for CIs that match your criteria.
-   [Schedule a CMDB 360 query for a report](../task/workspc-mltsrc-query-schedule.md) to run that query on a regular basis. Scheduling a query enables you to create a CMDB 360 report that integrates the query results with the [platform Reporting feature](https://www.servicenow.com/docs/access?context=reporting-landing-page&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

## Discovery sources

Cards in the Discovery sources tile show aggregated counts for your discovery sources.This tile also includes coverage cards showing a breakdown of CIs per the number of discovery sources reporting those CIs.

-   **Number of discovery sources**

    The total number of discovery sources that report CMDB 360 data.

-   **Total CMDB 360 records**

    The total number of raw CMDB 360 records in the CMDB 360 data store that contains records for each discovery source report, per each CI attribute.

-   **Reconciled CIs**

    The total number of unique CIs created in the CMDB after processing incoming data from all discovery sources, including after reconciling data from multiple discovery sources for the same CIs. For more information, see [CMDB Identification and Reconciliation](c_CMDBIdentifyandReconcile.md).

-   **Discovery source overviewt**

    The distribution of CMDB 360 CIs across all reporting discovery sources.

-   **Coverage: CIs with a single discovery source**

    Shows CIs that are only reported by a single discovery source, with a breakdown by the discovery source reporting those CIs. The number on the chart is the actual total number of CIs with a single discovery source, regardless of any dashboard settings. The number of records in list views that appear when you drill down the chart, depends on dashboard settings and can be only a subset of that total.

-   **Coverage: CIs by number of discovery sources**

    Shows CIs reported by multiple discovery sources, grouped by the number of discovery sources that are reporting those CIs.


You can use the following options to filter the calculated records in the CMDB 360 data store that apply to all cards in the Discovery sources tile:

-   All \(default\): Includes records from both CMDB and non-CMDB tables.
-   CMDB CI: Includes records only from CMDB classes.
-   Principal Class: Includes records only from principal classes. For information about defining a class as principal and therefore including that class in the Principal Class filter, see [Create a CI class](../task/t_CreateCIType.md).

Various settings apply only to the coverage charts. They determine the scope and type of data that is included in the coverage charts and can greatly affect the performance of the associated calculation job:

-   The dashboard Coverage settings determine the mixture of classes for the records in drill-down list views. For information about these settings and their effect, see [Coverage cards](../task/workspc-mltsrc-configure.md#table_ldr_cnz_dvb).
-   The system properties **sn\_cmdb\_ws.ms.calculate\_cmdb\_only** and **glide.identification\_engine.multisource\_non\_cmdb\_ci\_enabled** determine if both CMDB and non-CMDB or CMDB only data, is included in the coverage charts. For more information about these system properties, see [Components related to CMDB 360](../reference/components-multisource-cmdb.md).

    **Note:** If the **sn\_cmdb\_ws.ms.calculate\_cmdb\_only** is true or **glide.identification\_engine.multisource\_non\_cmdb\_ci\_enabled** is false, then both 'All' and 'CMDB CI' filters show CMDB data only \(non-CMDB data is ignored\).

-   The **sn\_cmdb\_ws.ms.report\_class\_ci\_count\_max\_threshold** system property and the CMDB 360 Analytics Skipped Class \[sn\_cmdb\_ws\_ms\_skip\_class\] table, together, determine class inclusion in the coverage charts.

    If the record count for a class \(CMDB or non-CMDB\) in the CMDB 360 Data \[cmdb\_multisource\_data\] table exceeds the value set by the **sn\_cmdb\_ws.ms.report\_class\_ci\_count\_max\_threshold** system property, then a record is created in the CMDB 360 Analytics Skipped Class \[sn\_cmdb\_ws\_ms\_skip\_class\] table and by default, the class is skipped in future calculations for the coverage charts. You can include a skipped class in the coverage charts by setting the **Override class CI records population** column of a skipped class in the **sn\_cmdb\_ws\_ms\_skip\_class** table, to 'true'.

    **Note:** Some classes, when included or excluded from the coverage charts, can greatly impact the overall performance of the chart calculations. For more information, see [Components related to CMDB 360](../reference/components-multisource-cmdb.md).


