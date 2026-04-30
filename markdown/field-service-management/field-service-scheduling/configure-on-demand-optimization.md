---
title: Configure on demand optimization
description: Enable dispatchers to respond to unexpected changes by configuring on demand intraday optimization, giving them the ability to run Schedule Optimization ad hoc directly from Dispatcher Workspace.
locale: en-US
release: zurich
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Optimizing technician schedules, Schedule Optimization, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Configure on demand optimization

Enable dispatchers to respond to unexpected changes by configuring on demand intraday optimization, giving them the ability to run Schedule Optimization ad hoc directly from Dispatcher Workspace.

## Before you begin

Activate and configure intraday optimization. For more information, see [Activate intraday optimization](activate-intraday-optimization.md) and [Configure intraday optimization](configure-intraday-optimization.md).

Role required: wm\_admin

## About this task

Dispatchers with the 'schedule\_optimization\_user' role can manually trigger optimization in the Dispatcher Workspace. This option is available when an on-demand applicable policy is added to the scheduling attribute and intraday on-demand optimization is enabled.

This video demonstrates how to configure on demand optimization for dispatchers 

## Procedure

1.  Navigate to **All** &gt; **Schedule Optimization** &gt; **Administration** &gt; **Scheduling Attributes**.

2.  Select an existing **Scheduling attribute** and proceed to step 3 or select **New** to [Create a scheduling attribute for Schedule Optimization](configure-scheduling-attributes.md).

3.  In the **On demand applicable policies** related list, select **Edit** to add a policy or select **New** to create a policy.

    Dispatchers can change the policy before running optimization to adapt to current conditions. Maintaining multiple on-demand policies in scheduling attributes, such as policies enabling overtime or travel outside regular work hours, enables dispatchers to adjust policies as needed.

4.  Select **Update**.

5.  Navigate to **All** &gt; **Schedule Optimization** &gt; **Intraday optimization** &gt; **Configurations**.

6.  Select an existing **Intraday configuration** and proceed to step 7 or select **New** to [Configure intraday optimization](configure-intraday-optimization.md).

7.  In the **Qualifiers** tab, set **Enable on demand optimization** to true.

    If the option to enable on-demand isn’t visible, deselect the **Default** option.

8.  Select **Save**.


## Result

Intraday optimization can now be triggered on demand by dispatchers to adapt to changes as they happen throughout the day.

**Related topics**  


[Run optimization for your groups or territories from Dispatcher Workspace](../concept/optimize-agent-schedules-on-demand-in-dispatcher-workspace.md)

