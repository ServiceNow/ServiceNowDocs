---
title: Map an insight rule to a new scheduled script
description: Map an insight rule to a new scheduled script to define the type of insight trigger. This insight trigger activates the associated insight rule to run.
locale: en-US
release: australia
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create an insight trigger, Create an insight rule, Working with automations, Use, Automation Center, Workflow Data Fabric]
---

# Map an insight rule to a new scheduled script

Map an insight rule to a new scheduled script to define the type of insight trigger. This insight trigger activates the associated insight rule to run.

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

4.  Select **Map to a new scheduled script**.

5.  On the form, fill in the fields.

6.  Select **Submit**.


**Parent Topic:**[Create an insight trigger](create-insight-trigger.md)

**Related topics**  


[Automation Scheduled Trigger Execution form](../reference/auto-sched-trigger-exe-form.md)

