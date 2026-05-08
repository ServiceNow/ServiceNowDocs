---
title: Create or edit CI remediation
description: Create a CI remediation rule that lets users manually apply an Orchestration workflow for resolving issues with specific CIs associated with alerts. Define these CIs in the CI filter conditions of the rule.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CI Remediation, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Create or edit CI remediation

Create a CI remediation rule that lets users manually apply an Orchestration workflow for resolving issues with specific CIs associated with alerts. Define these CIs in the CI filter conditions of the rule.

## Before you begin

Create the workflow to remediate CIs. In the workflow settings, select **Remediation Task \[em\_remediation\_task\]** in the **Table** field.

Then submit the workflow definition, and add the following conditions to the workflow properties:

-   **\[Run Remediation\]\[is\]\[true\]**
-   **\[Workflow\]\[is\]\[&lt;name of the new workflow that you just created&gt;\]**

    For example, if the name of the workflow is `CI remediation`, add this condition:

    **\[Workflow\]\[is\]\[CI remediation\]**


After you finish configuring the workflow, make sure that you publish it. For more details, see Create a workflow.

Role required: evt\_mgmt\_admin

## About this task

A CI remediation rule associates a set of CIs that might experience problems with a remediation workflow. The remediation workflow can either resolve the underlying problem or help troubleshoot the problem that generated the alert. For example, you can proactively configure a workflow with the appropriate response actions for predictable alerts. For more details, see the [Event Management Remediation](https://www.youtube.com/watch?v=LXboAU_R_74) short video.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Rules** &gt; **CI Remediations**.

2.  Click **New**, or select a CI remediation to edit.

3.  Fill in the fields, and click **Submit** or **Update**.

    |Control|Description|
    |-------|-----------|
    |CI filter|Conditions to match the CIs that you want to apply this remediation to.|
    |Orchestration workflow|The remediation workflow to apply to CIs that match the filter conditions.|


## Result

In service maps that are opened from the Event Management dashboard, this remediation can be applied to any CIs that match the filter conditions.

**Parent Topic:**[CI Remediation](../concept/ci-remediation.md)

