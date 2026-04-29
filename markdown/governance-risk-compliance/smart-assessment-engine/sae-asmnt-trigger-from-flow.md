---
title: Configure the Trigger Smart Assessment Flow action
description: Configure the Trigger Smart Assessment flow action to initiate the Smart Assessment Engine assessments and send them to the specified assessors. You then add the action to your flow.
locale: en-US
release: australia
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Triggering assessments, Configure, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Configure the Trigger Smart Assessment Flow action

Configure the Trigger Smart Assessment flow action to initiate the Smart Assessment Engine assessments and send them to the specified assessors. You then add the action to your flow.

## Before you begin

Role required: flow\_designer

## About this task

The flow includes both a trigger condition and the Trigger Smart Assessment flow action.

An example trigger condition might be that the state in the control table changes to **Attest**.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the **Action** tab, select **Trigger Smart Assessment**.

3.  Fill in the Trigger Smart Assessment action form to design the action.

    The settings on the form are described in [Trigger Smart Assessment action form](../reference/sae-smart-asmnt-action-form.md).

4.  Test the action as described in [Building flows](https://www.servicenow.com/docs/access?context=flows&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

    For descriptions of all these settings, see [Settings in the Test action pop-up window](../reference/sae-test-action-popup.md).

5.  Select **Save**.

    **Note:** After you save the configuration, select **Activate** to trigger the assessment.


## Result

Assessments are triggered.

**Related topics**  


[Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=australia&pubname=australia-application-development&ft:locale=en-US)

[Building flows](https://www.servicenow.com/docs/access?context=flows&version=australia&pubname=australia-build-workflows&ft:locale=en-US)

[Create a flow in Workflow Studio](https://www.servicenow.com/docs/access?context=create-flow&version=australia&pubname=australia-build-workflows&ft:locale=en-US)

