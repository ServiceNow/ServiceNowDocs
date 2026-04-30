---
title: Exclude patterns from learned patterns
description: Exclude CI-based or CI class-based alerts and patterns when you encounter alerts incorrectly added to a learned pattern by the Learned Patterns job. For example, a pattern might include an alert that occurred at the same time as other alerts but is not actually related to them. This maintains accuracy, ensuring better alert groupings and improved management efficiency.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Automated alert grouping, Alert grouping types and creation methods, Alert grouping, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Exclude patterns from learned patterns

Exclude CI-based or CI class-based alerts and patterns when you encounter alerts incorrectly added to a learned pattern by the Learned Patterns job. For example, a pattern might include an alert that occurred at the same time as other alerts but is not actually related to them. This maintains accuracy, ensuring better alert groupings and improved management efficiency.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

You select the incorrect alert in a pattern to exclude the entire pattern to which it belongs.

**Note:** When you exclude an incorrect alert, any other patterns containing that alert are also excluded.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Reporting** &gt; **Learned Patterns**.

    ![Exclude pattern navigation](../image/em-exclude-pattern-nav.png)

2.  On the Learned Patterns page, expand the anomalous pattern.

    ![Expanded patterns](../image/em-expanded-patterns.png)

3.  Select the pattern name to open it for exclusion.

4.  On the SA Alert Aggregation Learned Pattern page, select **Exclude**.

    ![Option to exclude the selected pattern](../image/em-pattern-exclude.png)


## Result

The entire pattern is removed from the Learned Patterns report and listed on the Excluded Patterns page, located at **Event Management** &gt; **Administration** &gt; **Excluded patterns**.

If the pattern includes other alerts, you can restore it by reclaiming those alerts as a learned pattern. For further details, see [Restore excluded patterns](restore-excluded-patterns.md).

