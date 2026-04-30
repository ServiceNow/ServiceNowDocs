---
title: Configure intraday optimization
description: Continuously run schedule optimization at selected intervals throughout the day to efficiently reassign tasks and maximize productivity. Additionally, enable dispatchers to run optimization on demand.
locale: en-US
release: zurich
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Optimizing technician schedules, Schedule Optimization, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Configure intraday optimization

Continuously run schedule optimization at selected intervals throughout the day to efficiently reassign tasks and maximize productivity. Additionally, enable dispatchers to run optimization on demand.

## Before you begin

Configure the scheduling attributes and activate intraday optimization. For more information see, [Create a scheduling attribute for Schedule Optimization](configure-scheduling-attributes.md) and [Activate intraday optimization](activate-intraday-optimization.md).

Role required: wm\_admin

## About this task

This video demonstrates how to configure intraday optimization for a specific group or territory. 

**Note:** This video demonstrates how to configure intraday optimization for a specific group or territory. To create a default intraday configuration for all groups and territories, see step 5.

You can configure the schedule optimization engine to automatically update assigned work order tasks throughout the day as scheduling conditions change. Common conditions that trigger intraday optimization to run are an agent running late, an agent calling in sick, an agent using PTO, a task being canceled, or a new high priority task being added.

You can also enable dispatchers to manually trigger optimization to run from the Dispatcher Workspace when the intraday on demand optimization configuration is enabled and an on demand applicable policy has been added to the scheduling attribute. See [Create a scheduling attribute for Schedule Optimization](configure-scheduling-attributes.md) to add an on-demand applicable policy to the configuration.

## Procedure

1.  Navigate to **All** &gt; **Schedule Optimization** &gt; **Intraday Optimization** &gt; **Configurations**.

2.  Select **New**.

3.  Provide a name for the configuration.

4.  Set the default scheduling attribute configuration in the **Default scheduling attribute configuration** field.

    To enable dispatchers to run optimization on demand from the Dispatcher Workspace, select a scheduling attribute that has an on-demand applicable policy added to the configuration.

5.  Select the **Default** check box to create a global record for all groups and territories.

    **Note:** Only 1 default record can exist. If you are creating a new default record, deactivate the existing default record.

6.  Select the **Active** check box.

7.  In the **Schedule** tab, select a flow to trigger the intraday configuration and a default processing window.

8.  Select **Submit**.

9.  Select the Intraday configuration.

10. In the **Qualifiers** tab, add your groups or territories.

    **Note:** The **Qualifiers** tab is not available for the default record.

11. Select **Save**.

12. Enable dispatchers to run optimization for a group or territory from Dispatcher Workspace by setting **Enable on demand optimization** to true.

13. Select **Submit**.

14. Create an attribute override for a particular time frame to override the default scheduling attribute or processing window from the related intraday configuration for a particular group or territory.

    1.  Select the **Attribute overrides** tab

    2.  Select **New**.

    3.  Enter the applicable dates in the **Applies from** and **Applies to** fields.

    4.  Choose a scheduling attribute configuration and processing window.

    5.  Select **Submit**.


