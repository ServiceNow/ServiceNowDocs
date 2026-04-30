---
title: Configure alert correlation logic order
description: Improve alert management by enabling users to customize correlation logic order. This feature empowers you to fine-tune correlation methods to their specific needs, enhancing alert prioritization and response efficiency.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Scheduled jobs and parameters for alert grouping, Alert grouping, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Configure alert correlation logic order

Improve alert management by enabling users to customize correlation logic order. This feature empowers you to fine-tune correlation methods to their specific needs, enhancing alert prioritization and response efficiency.

## Before you begin

Role required: admin

## About this task

If one of the grouping types is not specified in the property, it needs to be added manually. Alert correlation rules are trigger-based and applied immediately when an alert is created or updated, before other grouping algorithms.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  Search for the property **sa\_analytics.agg.query.group\_logic\_order**.

    Default value is “CMDB,TAG\_BASED,PATTERN,TEXTBASE". This is a comma separated list of the grouping types in the order of their execution.

    -   CMDB: CMDB grouping
    -   TAG\_BASED: Tag cluster
    -   PATTERN: Automated CI-based patterns
    -   TEXTBASE: Text-based grouping
3.  Use the property **sa\_analytics.agg.query.group\_logic\_order** to define or modify the order of correlation methods based on your preferences.


