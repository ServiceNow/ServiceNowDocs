---
title: Create an insight trigger
description: Create an active insight trigger so that you can run the related insight rule.
locale: en-US
release: xanadu
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Create an insight rule, Working with automations, Using Automation Center, Automation Center, Creating integrations with applications]
---

# Create an insight trigger

Create an active insight trigger so that you can run the related insight rule.

## Before you begin

This task must be performed in the classic environment.

Create an insight rule. For more information, see [Create an insight rule](create-insight-rule.md).

Role required: sn\_ac.automation\_technical\_user or sn\_ac.automation\_admin

## About this task

When an insight rule is processed, it generates an insight. Insights appear on the Insights widget in the Executions dashboard of Automation Center Workspace.

An insight trigger activates the associated insight rule to run.

An insight rule doesn’t run unless it’s mapped to an insight trigger.

## Procedure

1.  Navigate to **All** &gt; **Automation Center** &gt; **Administration** &gt; **Insight Rules**.

2.  Open the insight rule for which you want to create and associate an insight trigger to.

3.  On the **Automation Insight Triggers** tab, select **New**.

4.  If the **New** button is unavailable, ensure that the Application scope you are in is same as the one where the record is.

    A message is displayed if the **New** button is unavailable. Follow the message to change the Application scope.

5.  Select the appropriate type of insight trigger that you want to create:

    -   [Map to an existing business rule](map-existing-rule-insight-trigger.md)
    -   [Map to a new scheduled script](map-new-scheduled-script-trigger.md)
    -   [Map to an existing scheduled job](map-existing-scheduled-job-trigger.md)

-   **[Map an insight rule to an existing business rule](map-existing-rule-insight-trigger.md)**  
Map an insight rule to an existing business rule to define the type of insight trigger. This insight trigger activates the associated insight rule to run.
-   **[Map an insight rule to a new scheduled script](map-new-scheduled-script-trigger.md)**  
Map an insight rule to a new scheduled script to define the type of insight trigger. This insight trigger activates the associated insight rule to run.
-   **[Map an insight rule to an existing scheduled job](map-existing-scheduled-job-trigger.md)**  
Map an insight rule to an existing scheduled job to define the type of insight trigger. This insight trigger activates the associated insight rule to run.

**Parent Topic:**[Create an insight rule](create-insight-rule.md)

