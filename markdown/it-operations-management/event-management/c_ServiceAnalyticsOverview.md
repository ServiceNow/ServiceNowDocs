---
title: Alert grouping
description: Alert grouping is the process of organizing and consolidating related alerts into sets based on common characteristics or criteria. This helps in simplifying alert management by reducing noise, making it easier to prioritize, track, and address issues efficiently. Grouped alerts provide a clearer overview of related incidents, facilitating quicker root cause analysis and remediation.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Alert grouping

Alert grouping is the process of organizing and consolidating related alerts into sets based on common characteristics or criteria. This helps in simplifying alert management by reducing noise, making it easier to prioritize, track, and address issues efficiently. Grouped alerts provide a clearer overview of related incidents, facilitating quicker root cause analysis and remediation.

## Understanding alert grouping

Watch this brief video to learn how alert grouping organizes alerts into clusters based on specific criteria.

Video explaining how alert grouping organizes alerts into clusters based on specific criteria.

## How alert grouping works

Alert grouping enhances operational efficiency and optimizes alert management by categorizing alerts. Here’s how it works:

1.  Event consolidation: Event Management collects alerts from multiple sources, providing a centralized view of notifications and alerts. This consolidation enables teams to manage alerts more efficiently and recognize critical issues more easily.
2.  Contextual Enrichment: Alerts are enriched with data from the Configuration Management Database \(CMDB\), which contains detailed information about applications and infrastructure components. This context allows teams to better understand the significance of alerts and prioritize responses based on their impact.
3.  Intelligent Correlation: Event Management utilizes different types of machine learning algorithms to automatically group related alerts. This intelligent grouping reduces alert noise by combining similar alerts, allowing teams to concentrate on significant issues rather than being inundated with multiple notifications.

## Benefits of alert grouping

-   Creating [automated alert groups](c_SACorrelatedAlertGroups.md) by aggregating alerts based on predefined patterns.
-   Correlating alerts using timestamps and CI identification to form automated alert groups.
-   Forming [CMDB based alert grouping](cmdb-alert-groups.md) by correlating alerts based on CI relationships in the CMDB.
-   Correlating alerts based on text similarity of alerts using NLP \(Natural Language Processing\).

**Related topics**  


[Synchronizing alert response with automated alert grouping](../task/coordinating-alert-response-with-automated-alert-grouping.md)

