---
title: Configure alert correlation logic order
description: Improve alert management by enabling users to customize correlation logic order. This feature empowers you to fine-tune correlation methods to their specific needs, enhancing alert prioritization and response efficiency.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 1
breadcrumb: [Scheduled jobs and parameters for alert grouping, Alert grouping, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure alert correlation logic order

Improve alert management by enabling users to customize correlation logic order. This feature empowers you to fine-tune correlation methods to their specific needs, enhancing alert prioritization and response efficiency.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  Search for the property **sa\_analytics.agg.query.group\_logic\_order**.

    Default value is “MIXED,NETWORK\_TRAFFIC,PATTERN,GENERALIZED\_PATTERNS,TEXTBASE". This is a comma separated list of the grouping types in the order of their execution.

    **Note:** If one of the grouping types is not specified in the property, it needs to be added manually. Alert correlation rules are trigger-based and applied immediately when an alert is created or updated, before other grouping algorithms.

    -   MIXED: Combination of 2 or more grouping criteria
    -   NETWORK\_TRAFFIC: Network traffic grouping
    -   PATTERN: Automated CI-based patterns grouping
    -   TEXTBASE: Text-based grouping
3.  Use the property **sa\_analytics.agg.query.group\_logic\_order** to define or modify the order of correlation methods based on your preferences.


**Related topics**  


[Alert grouping and use cases](../concept/alert-group-use-cases.md)

