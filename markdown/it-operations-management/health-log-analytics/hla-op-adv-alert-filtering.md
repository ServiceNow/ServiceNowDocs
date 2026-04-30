---
title: Reducing noise by adding advanced log alert filters in Health Log Analytics
description: Use advanced log alert filters to determine whether to allow an alert or to drop it. These filters reduce noise by dropping alerts that don't indicate a significant issue.
locale: en-US
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Controlling alert generation, prioritization, and anomaly detection, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Reducing noise by adding advanced log alert filters in Health Log Analytics

Use advanced log alert filters to determine whether to allow an alert or to drop it. These filters reduce noise by dropping alerts that don't indicate a significant issue.

You can add advanced log alert filters to scan alerts for your defined conditions. For example, you can define a filter that drops alerts coming from specific log sources, or alerts for anomalies that do not cross the specified threshold.

Some examples of the actions that advanced filters can enable:

-   Alert only on anomalies that are shared across multiple hosts.
-   Do not alert on anomalies that happen outside of working hours.
-   Do not alert if the anomaly does not cross the specified threshold.
-   Alert only on anomalies that are part of a correlation.

You can manage advanced log alert filters as follows:

-   [Create advanced log alert filters](../task/hla-op-adv-alert-filter-crud.md)

    Add advanced log alert filters to scan alerts for conditions that you specify. The filters reduce noise by dropping alerts that do not indicate a significant issue. While developing a filter, you can test, update, publish, or activate the filter at any time.

-   Continue modifying the filter by reopening the filter record from the [filters list](../task/hla-op-search-queries-manage.md). You can then edit, test, publish, and activate the filter.

For more technical information on log alert filters, see the [Advanced Log Alert Filtering \[KB0863538\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0863538) article in the Now Support Knowledge Base.

-   **[Create advanced log alert filters](../task/hla-op-adv-alert-filter-crud.md)**  
Add advanced log alert filters to scan alerts for conditions that you specify. The filters reduce noise by dropping alerts that do not indicate a significant issue. While developing a filter, you can test, update, publish, or activate the filter at any time.

**Parent Topic:**[Controlling Health Log Analytics alert generation, prioritization, and anomaly detection](hla-controlling-alert-generation.md)

