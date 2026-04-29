---
title: Set up prioritized intraday optimization with matching rules
description: Configure prioritized intraday optimization to use matching rules that narrow job assignment decisions. Matching rules deliver focused, efficient job recommendations.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Optimization for prioritized events, Intraday optimization, Schedule Optimization, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Set up prioritized intraday optimization with matching rules

Configure prioritized intraday optimization to use matching rules that narrow job assignment decisions. Matching rules deliver focused, efficient job recommendations.

## Before you begin

Matching rules for prioritized intraday optimization require [Territory-Based Optimization](territory-based-optimization.md) to be enabled. Configurations using assignment groups don’t support matching rules.

Install the Field Service Management Demo Data \[com.snc.work\_management.demo\] plugin to access example matching rules. For more information see, [Activate Field Service Management](../../planning-and-policy/task/t_ActivateFieldServiceManagement.md).

Role required: wm\_admin

## About this task

Create matching rules within a specific intraday optimization configuration to control which tasks and technicians are included in optimization runs.

The matching rules execute in the order specified by the **Execution Order** field, with lower numbers processing first. When the demo data is installed, two example matching rules are available:

-   Filter technicians for prioritized events: Includes affected technician criteria
-   Filter tasks for prioritized events: Includes affected task criteria

You can use these example matching rules or create your own.

## Procedure

1.  Navigate to **All** &gt; **Schedule Optimization** &gt; **Intraday Optimization** &gt; **Configurations**.

2.  Select or create the configuration where you want to add the matching rule.

    -   To use an existing configuration: Open the configuration record and go to step 6:
    -   To create a configuration: Select **New** and complete the following steps.
3.  Complete the form.

    -   **Name**: Enter a descriptive name for the configuration.
    -   **Default scheduling attribute configuration**: Select the appropriate configuration.
    -   **Active**: Select the check box to enable this configuration.
    -   Leave the **Default** check box clear. The default record applies system-wide settings and shouldn’t be modified for specific matching rules configurations.
4.  Select **Submit**.

5.  Reopen the configuration you created.

6.  In the **Qualifiers** tab, select **Edit**.

7.  Move qualifiers from the **Collection** list to the **Qualifiers** list and select **Save**.

8.  Set **Enable prioritized event optimization** to **True**.

9.  Add matching rules to your configuration:

    -   To enable existing matching rules, continue to step 10.
    -   To create your own matching rules, select **Save**, then see [Create matching rules for intraday events](create-matching-rules-for-intraday-events.md).
10. In the **Matching Rules** tab, select **Edit**.

11. Move the desired matching rules from the **Collection** list to the **Matching Rules** list and select **Save**.

12. Select **Update**.

13. Choose which event types use matching rules.

    1.  Navigate to **All** &gt; **Schedule Optimization** &gt; **Intraday Optimization** &gt; **Event Types**.

    2.  For each event type you want to optimize with matching rules, set the **Prioritized** field to **True**.


## Result

When intraday optimization runs for the selected qualifier and detects an event flagged as prioritized, the system applies the configured matching rules.

**Related topics**  


[Activate intraday optimization](activate-intraday-optimization.md)

[Configure intraday optimization](configure-intraday-optimization.md)

