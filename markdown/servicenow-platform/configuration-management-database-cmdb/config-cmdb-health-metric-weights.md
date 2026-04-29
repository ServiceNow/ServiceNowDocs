---
title: Configure aggregation weights for CMDB Health scores
description: Metrics health scores are aggregated into their respective KPI \(key performance indicator\) scores, which in return are aggregated into the overall CMDB Health score. Modify the default aggregation weights for metrics and KPIs to reflect on the importance of one metric over another is assessing the health of CMDB in the organization.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, CMDB Health, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure aggregation weights for CMDB Health scores

Metrics health scores are aggregated into their respective KPI \(key performance indicator\) scores, which in return are aggregated into the overall CMDB Health score. Modify the default aggregation weights for metrics and KPIs to reflect on the importance of one metric over another is assessing the health of CMDB in the organization.

## About this task

The completeness KPI, for example, consists of the metrics required fields and recommended fields. By default, those metrics are configured to contribute 60% and 40% respectively to the aggregated score of the completeness KPI. You can modify that proportional weight of required fields and recommended fields within the completeness KPI to be, for example, 25% and 75% respectively. You can also modify the proportional weights of the completeness, compliance, and correctness KPIs within the aggregated overall score.

To modify aggregation weights, you must directly access the CMDB Health Metric Preferences \[cmdb\_health\_metric\_pref\] table, where those settings are stored. However, custom settings are used only if the system is set to use legacy calculation methods.

If Domain Support - Domain Extensions is activated, then you can configure aggregation preferences per domain. By default, the weights of KPIs have default settings, and metrics are globally set.

## Before you begin

Toggle the **Use legacy calculation methods** switch on the CMDB Health Dashboard to use legacy calculation methods. Custom weight settings are used in aggregated score calculations only if using legacy calculation methods is in effect.

Role required: sn\_cmdb\_editor, sn\_cmdb\_admin, itil, or itil\_admin

## Procedure

1.  Select **All** and then, in the navigation filter, enter `cmdb_health_metric_pref.list` to open the CMDB Health Metric Preferences table.

2.  Select a metric, KPI, or the **Overall** entry, and set its **Weighted average contribution** attribute to the percentage number that you want.

    Ensure that the sum of the percentage weights adds up to 100% for the respective aggregation:

    -   The sum of the percentage weights of all metrics for a KPI, must add up to 100.
    -   The sum of the percentage weights of all three KPIs \(correctness, compliance, completeness\) must add up to 100.

