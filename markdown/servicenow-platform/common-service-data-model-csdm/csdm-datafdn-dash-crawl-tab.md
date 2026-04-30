---
title: 'Crawl' stage reports on the CSDM Data Foundations dashboard
description: Crawl stage reports on the CSDM Data Foundations dashboard
locale: en-US
release: zurich
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: reference
last_updated: "2026-01-22"
reading_time_minutes: 2
breadcrumb: [Reference, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# 'Crawl' stage reports on the CSDM Data Foundations dashboard

Crawl stage reports on the CSDM Data Foundations dashboard

## Reports on the Crawl tab

In this example, a report on the **Crawl** tab indicates that there are service instances that are not associated with a business application.

![Crawl tab on the Data Foundations dashboard.](../image/csdm-data-fdns-dash-crawl.png)

-   **CSDM Foundation Indicators report**
    -   The **Priority** value is the product of the weight of the metric and the severity of the actual score. Priority ranges from 1 — Critical \(the highest priority\), to 5 — Low \(the lowest priority\).
    -   The **Result** column displays a color-coded bar showing the percentage of CIs or the measured item that are in compliance for the key foundational metric.

        -   Red: 0–50% are in compliance.
        -   Yellow: 50–90% are in compliance.
        -   Green: More than 90% are in compliance.
        To ensure optimum performance, the system stops collecting data for some metrics when they reach a specified number of non-compliant CIs. For information on managing data collection for a metric that isn't needed or that affects performance of the dashboard, see [Manage performance](../../configuration-management/concept/csdm-cmdb-foundations-dashboards.md#section-manage-performance).

    -   The **Remediation playbook URL** column displays links to knowledge articles in Now Support with instructions for bringing the CIs into compliance. Use your Now Support credentials to access the knowledge article.

To view detailed information on the impact of a metric and for details on working on issues, select the appropriate **Remediation playbook URL**.

-   **App services missing business app relationship**

    Percent of CIs missing an important relationship. The service instance is a base-system CMDB table that should map to the related business application in use. Because the service instance is typically the system that a caller identifies when they report an issue with an application, the relationship is required if you are to identify the affected business application. For more information, see [Use Application Services dashboard to monitor health](../../configuration-management/task/app-service-dashboard.md).

-   **CIs with Mismatched Operational Status and Life Cycle Stage**

    The report identifies life-cycle value mismatches among CMDB, asset, and IBI. This information is helpful when you're aligning existing status data to the CSDM guidelines.

-   **App service to business app not Consumed by**

    The report identifies incorrect relationships.

-   **Business apps missing app service relationship**

    Percent of CIs missing an important relationship.


## Managing performance of data collection

The system runs scheduled jobs that collect data for three CSDM metrics:

-   App services that are missing a business app relationship
-   Business apps that are missing an app service relationship
-   App services where the relationship to business apps is not Consumed by

For information on managing data collection for a metric that isn't needed or that affects performance of the dashboard, see [Manage performance](../../configuration-management/concept/csdm-cmdb-foundations-dashboards.md#section-manage-performance).

**Parent Topic:**[CSDM reference](../concept/csdm-content-frame-reference.md)

**Related topics**  


[CSDM Data Foundations dashboard](../concept/csdm-data-foundations-dashboard.md)

