---
title: Publish a subflow
description: Publish a subflow to make it available to other users and to add it to activated flows.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Building subflows, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Publish a subflow

Publish a subflow to make it available to other users and to add it to activated flows.

## Before you begin

Role required: flow\_designer or admin

[Create a subflow in Workflow Studio](create-subflow.md), [test the subflow](test-subflow.md), and verify that it is working as expected.

## About this task

When you make changes to a published subflow, the changes remain in the draft state until you publish the subflow again. You must publish a changed subflow to make the changes available to activated flows.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Click the subflows tab and open a tested subflow.

3.  Click **Publish**.


## Result

The subflow can be added to activated flows. If you update the subflow after it is published, you must click **Publish** again to see the changes when the parent flow is run. After publishing changes, all parent flows that use the subflow are automatically updated to use the current version.

**Parent Topic:**[Building subflows](../concept/subflows.md)

