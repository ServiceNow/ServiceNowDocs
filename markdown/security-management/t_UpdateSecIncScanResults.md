---
title: Update security incident with lookup results workflow
description: The Update security incident with lookup results workflow updates existing security incidents with lookup results.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Common Security Operations integration flows and orchestration Flow Actions, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Update security incident with lookup results workflow

The **Update security incident with lookup results** workflow updates existing security incidents with lookup results.

## Before you begin

Role required: sn\_si.basic

## About this task

This workflow is triggered by a business rule on the lookup table which monitors when the **Result** field changes to Failed.

Workflow process activities include:

-   [Roll up lookup info to security incident activity](../reference/r_RollUpScanInfoSI.md)
-   [Update Task Worknotes activity](../../security-operations-orchestration/reference/update-task-worknotes-activity.md)

![Update security incident with lookup results workflow diagram](../image/UpdateSILookupResultsWorkflow.png)

**Parent Topic:**[Common Security Operations integration flows and orchestration Flow Actions](../../security-operations-common/concept/common-wf-activities.md)

