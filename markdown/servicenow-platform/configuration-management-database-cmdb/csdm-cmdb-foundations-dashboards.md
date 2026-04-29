---
title: Monitor health in CSDM and CMDB Data Foundations Dashboards
description: The ServiceNow CSDM and CMDB Data Foundations Dashboards store app contains dashboards with insights into the key foundational metrics of your CMDB and Common Service Data Model \(CSDM\). This app uses ServiceNow health benchmarks to provide recommendations to ensure that the CMDB and CSDM are properly configured for optimal usage and to mitigate any potential risks.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Monitor health in CSDM and CMDB Data Foundations Dashboards

The ServiceNow® CSDM and CMDB Data Foundations Dashboards store app contains dashboards with insights into the key foundational metrics of your CMDB and Common Service Data Model \(CSDM\). This app uses ServiceNow® health benchmarks to provide recommendations to ensure that the CMDB and CSDM are properly configured for optimal usage and to mitigate any potential risks.

**Note:** CSDM and the CMDB Data Foundations Dashboards don't support domain separation.

For an introduction, watch the ServiceNow [Data Foundations Dashboards for CSDM and CMDB](https://www.youtube.com/watch?v=kPY9eItc3dM) video.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

The CSDM and CMDB Data Foundations Dashboards store app provides dashboards that complement each other. See the respective sections for each of the following dashboards:

-   **[CMDB Data Foundations dashboard](cmdb-data-foundations-dashboard.md)**

    Evaluates various configurations and customizations in the CMDB. This dashboard checks that important data is valid and properly configured, and identifies and provides visibility into potential risks in the implementation. Use the CMDB Data Foundations dashboard to prevent issues and support continuous effective functioning of the CMDB.

-   **[CSDM Data Foundations dashboard](../../csdm-implementation/concept/csdm-data-foundations-dashboard.md)**

    The CSDM Data Foundations dashboard displays key CSDM metrics on a single page to assist you in getting the full benefit from your ServiceNow AI Platform® products.


The CSDM and the CMDB Data Foundations dashboards capability is provided by the com.snc.cmdb.getwell plugin, which is activated by default in base systems.

## Access the dashboards

Use either of the following steps to access the CSDM and the CMDB Data Foundations Dashboards:

-   In CMDB Workspace:
    1.  Navigate to **Workspaces** &gt; **CMDB Workspace**.
    2.  Select **Management** in the CMDB Workspace menu bar.
    3.  Select **CMDB Data Foundations Dashboard** or **CSDM Data Foundations Dashboard** in Management tools, in the Optimize section.
-   Navigate to **All** &gt; **Configuration**, and then select **CMDB Data Foundations Dashboard** or **CSDM Data Foundations Dashboard**.

You can toggle between the two dashboards by clicking the change dashboard icon \(![Change dashboard.](../image/ChangeDashboard.png)\) on the title bar of either dashboard.

## Manage performance

It might be useful to manage the performance impact of some metrics that are greatly affected by, for example, a large CMDB or a high number of non-compliant CIs. You can use any of the following methods to manage performance of those metrics to improve the overall performance of the dashboards:

-   **Deactivate a metric**

    Deactivate any CMDB or CSDM metrics that aren't needed or that require extensive resources and affect performance. The active/non-active settings for metrics are preserved across family release upgrades.

    To deactivate a metric:

    1.  Access the CMDB/CSDM Get Well Metrics \[sn\_getwell\_metric\] table where all CMDB and CSDM metrics are stored.
    2.  Navigate to the list view of the table \[sn\_getwell\_metric\].
    3.  Locate the metric that you want to deactivate and set its **Active** column to **false**.
    Tiles on the dashboards that are associated with inactive metrics stop collecting data and aren't refreshed.

-   **Limit a metric**

    For the following metrics, you can use metric-specific settings to limit their performance impact:

    -   CMDB metrics:
        -   **CIs Processed via IRE**
        -   **CIs with Relationships to Parent and Child**
        -   **Hardware CIs with Serial Numbers**
    -   CSDM metrics:
        -   **Application Services with 'Consumes::Consumed By' Relationship to Business Application**
        -   **Application Services with Business Application Relationships**
        -   **Business Application with Application Service Relationship**
    The following columns in the CMDB/CSDM Get Well Metrics \[sn\_getwell\_metric\] table are set with default values per metric that limit performance impact, some of which can be fine tuned. Review those settings for example, when there is a large number of non-compliant CIs for a metric. Another example is having a large CMDB where a small number of compliant CIs for a metric is already a sufficient indication of health and there is no need to process the rest of the CIs for that metric.

    -   **Aggregate limit**: The maximum number or percentage of non-compliant CIs that are reported for the metric. Once that threshold is reached, counting for the metric stops for the run and the score for the metric is set to 0 \(you can't customize the default value\).
    -   **Fail count threshold**: The threshold of the number of consecutive metric runs that failed due to exceeding the metric's **Runtime threshold**. When that threshold is reached, the respective metric is automatically deactivated.
    -   **Runtime threshold**: The time threshold in seconds that is considered too long for a metric run. When exceeded, the current metric run is considered failed.
    For most metrics, when the number of consecutive runs that fail because the runtime exceeds **Runtime threshold**, is greater than the **Fail count threshold**, the system automatically deactivates the metric. You can manually reactivate a deactivated metric by setting its **Active** column to **true**. An exception to those column definitions and usage is the CMDB **CIs Processed via IRE** metric. For details, see [CMDB Data Foundations dashboard](cmdb-data-foundations-dashboard.md).


