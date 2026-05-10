---
title: Trigger assessments from a script
description: Use a script to execute the Trigger Smart Assessment flow action to generate Smart Assessment Engine assessments and assign them to the assessors.
locale: en-US
release: australia
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Triggering assessments, Configure, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Trigger assessments from a script

Use a script to execute the Trigger Smart Assessment flow action to generate Smart Assessment Engine assessments and assign them to the assessors.

## Before you begin

Role required: flow\_designer

## About this task

In the script, you specify the assessment template for the generated assessments and the conditions that trigger the assessments.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the **Actions** tab, select **Trigger Smart Assessment**.

3.  In the More actions menu icon ![](../image/more-actions-menu.png),select **Create code snippet**, and then copy and paste the snippet into your script.


## Result

**Note:** In the snippet, you have the option to specify whether the action should execute synchronously or asynchronously. Select the asynchronous option to help avoid stalling, especially when processing large templates.

The call to the Trigger Smart Assessment action is now part of the script.

## What to do next

Specify the required and optional input settings for the action. The settings are defined on the Trigger Smart Assessment action form and are described in [Trigger Smart Assessment action form](../reference/sae-smart-asmnt-action-form.md).

**Related topics**  


[Flow Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/flow-designer.md)

