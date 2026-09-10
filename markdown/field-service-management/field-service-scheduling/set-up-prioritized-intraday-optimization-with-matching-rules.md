---
title: Set up prioritized intraday optimization with matching rules
description: Configure prioritized intraday optimization to use matching rules that narrow job assignment decisions. Matching rules deliver focused, efficient job recommendations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/field-service-scheduling/set-up-prioritized-intraday-optimization-with-matching-rules.html
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Matching rules for prioritized intraday optimization, Optimization for prioritized events, Intraday optimization, Schedule Optimization, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Set up prioritized intraday optimization with matching rules

Configure prioritized intraday optimization to use matching rules that narrow job assignment decisions. Matching rules deliver focused, efficient job recommendations.

## Before you begin

-   Complete the setup in [Create an intraday optimization configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-scheduling/configure-intraday-optimization.md).
-   Matching rules for prioritized intraday optimization require [Territory-Based Optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-scheduling/territory-based-optimization.md) to be enabled. Configurations using assignment groups don’t support matching rules.
-   Install the Field Service Management Demo Data \[com.snc.work\_management.demo\] plugin to access example matching rules. For more information see, [Activate Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/t_ActivateFieldServiceManagement.md).

Role required: wm\_admin

## About this task

Matching rules combine one or more matching dimensions using AND logic within a rule. When you configure multiple matching rules, their results combine using OR logic. Matching rules execute in the order specified by the Execution Order field, with lower numbers processing first.

Example:

-   Rule 1 \(strict filter\): Technicians within 5 miles AND with printer skills
-   Rule 2 \(broader filter\): Technicians within 10 miles AND with copier skills
-   Result: The system optimizes with Rule 1 technicians OR Rule 2 technicians

## About this task

-   Filter technicians for prioritized events: Includes affected technician matching dimensions
-   Filter tasks for prioritized events: Includes affected task matching dimensions

You can use these example matching rules or create your own.

## Procedure

1.  Navigate to **All** &gt; **Schedule Optimization** &gt; **Intraday Optimization** &gt; **Configurations**.

2.  Select an active intraday configuration where you want to add the matching rule.

3.  In the **Matching Rules** tab, select **Edit**.

4.  Move the desired matching rules from the **Collection** list to the **Matching Rules** list and select **Save**.

    **Note:** To create custom matching rules instead, see [Create matching rules for intraday events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-scheduling/create-matching-rules-for-intraday-events.md).

5.  Set the **Enable matching rules** field to **True** for each qualifier that should use matching rules.

6.  Enter a **Maximum search radius** value and set the **Distance unit** field to **Miles** or **Kilometers** for each qualifier.

7.  Select **Update**.

8.  Navigate to **All** &gt; **Schedule Optimization** &gt; **Intraday Optimization** &gt; **Event Types**.

9.  For each event type you want to optimize with matching rules, set the **Prioritized** field to **True**.


## Result

When intraday optimization runs for the selected qualifier and detects an event flagged as prioritized, the system applies the configured matching rules.

**Related topics**  


[Activate intraday optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-scheduling/activate-intraday-optimization.md)

[Configure intraday optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-scheduling/configure-intraday-optimization.md)

