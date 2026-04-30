---
title: Create custom insights using Proactive Prompts
description: Use Proactive Prompts to create insight sections for the employee presence dashboard.
locale: en-US
release: zurich
product: Workplace Concierge
classification: workplace-concierge
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage, Workplace Concierge, Workplace Service Delivery, Employee Service Management]
---

# Create custom insights using Proactive Prompts

Use Proactive Prompts to create insight sections for the employee presence dashboard.

## Before you begin

**Note:** To create insights, you must install [Proactive Prompts](https://store.servicenow.com/sn_appstore_store.do#!/store/application/31e8684cb9c59110dcb7bdfe03456d30/) version 3.1 or later.

Role required: admin

## About this task

As an admin, you can use Proactive Prompts to create insights for employees. These insights are displayed on the presence dashboard and the calendar sections. For more information about Proactive Prompts, see [Proactive Prompts](../../human-resources/concept/proactive-prompts-for-hrsd.md).

For information about the default insights installed with Workplace Concierge, see [Insights installed with Workplace Concierge](../reference/insights-installed-workplace-concierge.md).

## Procedure

1.  Create a signal data source for the insight.

    For more information, see [Create a data source for a signal in Proactive Prompts](../../human-resources/task/proactive-prompts-signal-data-source.md).

2.  Navigate to **All** &gt; **Proactive Prompts** &gt; **Signal Configurations**.

3.  Select **New**.

4.  In the **Channels and actions** field, enter `Presence dashboard`.

5.  In the **Category tags** field, enter one of the following values.

    -   Presence Calendar Insight: Creates an insight for the calendar section of the presence dashboard.
    -   Presence Dashboard Insight: Creates an insight for the presence dashboard.
6.  In the **Datasource** field, select the signal data source that you created earlier.

7.  In the **Schedule** field, select the **On demand** schedule.

    **Note:** The on demand schedule is applicable for Calendar insights. For more information about signal schedules, see [Configure signal schedules in Proactive Prompts](../../human-resources/task/proactive-prompts-signal-schedules.md).

8.  From the **Receiving user** list, select **Employee**.

9.  Fill in the remaining fields based on your requirement, then select **Submit**.

    For a description of the field values, see [Signal configuration form](../../human-resources/reference/proactive-prompts-create-signal-form.md).

    For more information about creating a signal configuration, see [Create a signal in Proactive Prompts](../../human-resources/task/proactive-prompts-signal-create.md).


## Result

You've configured a signal that displays the insight to the user in the scheduled frequency.

**Parent Topic:**[Manage Workplace Concierge - Employee Presence](../concept/manage-workplace-concierge.md)

**Related topics**  


[View employee presence modules](view-employee-routines-and-collaborators.md)

