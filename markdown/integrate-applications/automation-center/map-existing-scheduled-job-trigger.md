---
title: Map an insight rule to an existing scheduled job
description: Map an insight rule to an existing scheduled job to define the type of insight trigger. This insight trigger activates the associated insight rule to run.
locale: en-US
release: yokohama
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create an insight trigger, Create an insight rule, Working with automations, Using Automation Center, Automation Center, Data and Automation]
---

# Map an insight rule to an existing scheduled job

Map an insight rule to an existing scheduled job to define the type of insight trigger. This insight trigger activates the associated insight rule to run.

## Before you begin

This task must be performed in the classic environment.

Create an insight rule. For more information, see [Create an insight rule](create-insight-rule.md).

Role required: sn\_ac.automation\_technical\_user or sn\_ac.automation\_admin

## About this task

When an insight rule is processed, it generates an insight. Insights appear on the Insights widget in the Executions dashboard of Automation Center Workspace.

An insight trigger activates the associated insight rule to run.

An insight rule does not run unless it is mapped to an insight trigger.

## Procedure

1.  Navigate to **All** &gt; **Automation Center** &gt; **Administration** &gt; **Insight Rules**.

2.  Open the insight rule that you want to create and associate an insight trigger to.

3.  On the **Automation Insight Triggers** tab, select **New**.

4.  Select **Map to an existing scheduled job**.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the insight trigger.|
    |Active|Option for ensuring the use of the insight trigger.|
    |Scheduled|Associated scheduled script to trigger the insight rule.|
    |Application|Application that is associated with the insight trigger.|
    |Automation insight rule|Associated automation insight rule.|

6.  Select **Submit**.


**Parent Topic:**[Create an insight trigger](create-insight-trigger.md)

