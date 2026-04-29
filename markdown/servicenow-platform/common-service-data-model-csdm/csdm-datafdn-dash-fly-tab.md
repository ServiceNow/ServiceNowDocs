---
title: 'Fly' stage reports on the CSDM Data Foundations dashboard
description: Fly stage reports on the CSDM Data Foundations dashboard
locale: en-US
release: australia
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# 'Fly' stage reports on the CSDM Data Foundations dashboard

Fly stage reports on the CSDM Data Foundations dashboard

## Reports on the Fly tab

In this example, a report on the **Fly** tab indicates that there are information objects that are not associated with a business application.

To view detailed information on the impact of a metric and for details on working on issues, select the appropriate **Remediation playbook URL**.

![Fly tab on the Data Foundations dashboard.](../image/csdm-data-fdns-dash-fly.png)

-   **CSDM Foundation Indicators report**
    -   The **Priority** value is the product of the weight of the metric and the severity of the actual score. Priority ranges from 1 — Critical \(the highest priority\), to 5 — Low \(the lowest priority\).
    -   The **Result** column displays a color-coded bar showing the percentage of CIs or the measured item that are in conformance for the key foundational metric.

        -   Red: 0–50% are in conformance.
        -   Yellow: 50–90% are in conformance.
        -   Green: More than 90% are in conformance.
        To promote optimum performance, the system stops collecting data for some metrics when they reach a specified number of non-conforming CIs. For information on managing data collection for a metric that isn't needed or that affects performance of the dashboard, see [Manage performance](../../configuration-management/concept/csdm-cmdb-foundations-dashboards.md#section-manage-performance).

    -   The **Remediation playbook URL** column displays links to knowledge articles in Now Support with instructions for bringing the CIs into conformance. Use your Now Support credentials to access the knowledge article.

**Note:** Starting with the CSDM Data Foundations dashboard v2.2, the following metrics no longer appear on the **Fly** tab:

-   Information objects missing an app service relationship
-   Catalog request items related to service offerings

**Parent Topic:**[CSDM reference](../concept/csdm-content-frame-reference.md)

**Related topics**  


[CSDM Data Foundations dashboard](../concept/csdm-data-foundations-dashboard.md)

