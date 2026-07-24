---
title: 'Walk' stage reports on the CSDM Data Foundations dashboard
description: Walk stage reports on the CSDM Data Foundations dashboard
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/common-service-data-model-csdm/csdm-datafdn-dash-walk-tab.html
release: australia
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# 'Walk' stage reports on the CSDM Data Foundations dashboard

Walk stage reports on the CSDM Data Foundations dashboard

## Reports on the Walk tab

In this example, a report on the **Walk** tab indicates that there are Technology management offerings that are not associated with a support group. This indicates a risk that downtimes will take longer to remedy.

To view detailed information on the impact of a metric and for details on working on issues, select the appropriate **Remediation playbook URL**.

\[Omitted image "csdm-data-fdns-dash-walk.png"\] Alt text: Walk tab on the Data Foundations dashboard.

-   **CSDM Foundation Indicators report**
    -   The **Priority** value is the product of the weight of the metric and the severity of the actual score. Priority ranges from 1 — Critical \(the highest priority\), to 5 — Low \(the lowest priority\).
    -   The **Result** column displays a color-coded bar showing the percentage of CIs or the measured item that are in conformance for the key foundational metric.

        -   Red: 0–50% are in conformance.
        -   Yellow: 50–90% are in conformance.
        -   Green: More than 90% are in conformance.
        To promote optimum performance, the system stops collecting data for some metrics when they reach a specified number of non-conforming CIs. For information on managing data collection for a metric that isn't needed or that affects performance of the dashboard, see [Manage performance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/csdm-cmdb-foundations-dashboards.md).

    -   The **Remediation playbook URL** column displays links to knowledge articles in Now Support with instructions for bringing the CIs into conformance. Use your Now Support credentials to access the knowledge article.

**Parent Topic:**[CSDM reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/common-service-data-model-csdm/csdm-content-frame-reference.md)

**Related topics**  


[CSDM Data Foundations dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/csdm-data-foundations-dashboard.md)

