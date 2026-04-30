---
title: Map an insight rule to an existing business rule
description: Map an insight rule to an existing business rule to define the type of insight trigger. This insight trigger activates the associated insight rule to run.
locale: en-US
release: zurich
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create an insight trigger, Create an insight rule, Working with automations, Use, Automation Center, Workflow Data Fabric]
---

# Map an insight rule to an existing business rule

Map an insight rule to an existing business rule to define the type of insight trigger. This insight trigger activates the associated insight rule to run.

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

4.  Select **Map to an existing business rule**.

5.  On the form, fill in the fields.

<table id="id_nxm_4kw_5tb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the insight trigger.

</td></tr><tr><td>

Active

</td><td>

Option for ensuring the use of the insight trigger.

</td></tr><tr><td>

Business rule

</td><td>

Applicable business rule that is required to trigger the insight rule.The mapped business rule script field must contain the new sn\_ac.ACInsightTriggerUtil\(current, previous\).raiseInsightByBR\(&lt;Business Rule SysId&gt;\); API to trigger the insight rule.

</td></tr><tr><td>

Application

</td><td>

Application that is associated with the insight trigger.

</td></tr><tr><td>

Automation insight rule

</td><td>

Associated automation insight rule.

</td></tr></tbody>
</table>6.  Select **Submit**.


**Parent Topic:**[Create an insight trigger](create-insight-trigger.md)

