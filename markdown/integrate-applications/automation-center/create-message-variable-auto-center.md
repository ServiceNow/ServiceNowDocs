---
title: Write a script for an automation message variable
description: Write JavaScript code input for variables that are added in the message of an insight rule.
locale: en-US
release: australia
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create an insight rule, Working with automations, Use, Automation Center, Workflow Data Fabric]
---

# Write a script for an automation message variable

Write JavaScript code input for variables that are added in the message of an insight rule.

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

2.  Open an insight rule that you want to write JavaScript code for the associated message variable.

3.  On the **Automation Message Variables** tab, select a variable.

4.  On the form, fill in the fields.

<table id="table_pyx_mhd_4qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the automation message variable.This field is auto-generated.

</td></tr><tr><td>

Field

</td><td>

Qualifier for message variable.Values in this list appear depending on the entry that is selected in the **Applies to** field while you’re creating an insight rule.

 This field appears only when the **Applies to** field is selected and when the **Threshold type** field is empty, while you’re creating an insight rule. For more information, see [Insight rule form](../reference/insight-rule-form.md).

</td></tr><tr><td>

Application

</td><td>

Name of the associated application.This field is auto-generated.

</td></tr><tr><td>

Automation insight rule

</td><td>

Name of the associated insight rule.This field is auto-generated.

</td></tr><tr><td>

Advanced

</td><td>

Advanced script.This field is auto-generated.

</td></tr><tr><td>

Script

</td><td>

Text field that accepts JavaScript code input and provides controls, such as syntax checking and formatting.For example, to return a value, enter `return 100;`.

 This field doesn’t appear when the **Applies to** field is selected and when the **Threshold type** field is empty, while you’re creating an insight rule. For more information, see [Insight rule form](../reference/insight-rule-form.md).

</td></tr></tbody>
</table>5.  Select **Update**.


**Parent Topic:**[Create an insight rule](create-insight-rule.md)

