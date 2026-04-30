---
title: Reducing noise by using advanced log alert filters
description: Advanced alert filters reduce noise by dropping alerts that do not indicate a significant issue.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# Reducing noise by using advanced log alert filters

Advanced alert filters reduce noise by dropping alerts that do not indicate a significant issue.

You use an advanced log alert filter to determine whether to drop or allow an alert. For example, you can define a filter that drops \(discards\) alerts that come from particular sources or alerts for anomalies that do not cross a specified threshold.

Some examples of the actions that advanced filters can enable:

-   Alert only on anomalies shared across multiple hosts.
-   Do not alert on anomalies that happen outside of working hours.
-   Do not alert if the anomaly amplitude does not cross the specified threshold.
-   Alert only on anomalies that are part of a correlation.

For deeper technical information on log alert filters, see the [Advanced Log Alert Filtering \[KB0863538\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0863538) article in the Now Support Knowledge Base.

-   **[Create advanced log alert filters](../task/hla-op-adv-alert-filter-crud.md)**  
Add advanced log alert filters to scan alerts for conditions that you specify. The filters reduce noise by dropping alerts that do not indicate a significant issue. While developing a filter, you can test, update, publish, or activate the filter at any time.

**Parent Topic:**[Using Health Log Analytics](../reference/hla-op-guide-binder.md)

**Related topics**  


[Create advanced log alert filters](../task/hla-op-adv-alert-filter-crud.md)

