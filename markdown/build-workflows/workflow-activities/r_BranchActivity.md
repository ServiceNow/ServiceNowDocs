---
title: Branch workflow activity
description: The Branch activity splits the workflow into multiple transition paths from a single activity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-activities/r\_BranchActivity.html
release: australia
product: Workflow Activities
classification: workflow-activities
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Utility workflow activities, Workflow activities reference, Workflow activities, Classic Workflow, Build workflows]
---

# Branch workflow activity

The **Branch** activity splits the workflow into multiple transition paths from a single activity.

To add a transition path, drag the **Branch** activity onto the canvas. When the Branch activity properties form displays, click **Submit** to add the activity to the canvas. Once the activity is on the canvas, right click in the activity body, then click **Add Condition**.

All transitions from this activity execute concurrently. This activity provides a single **Always** condition. You can draw any number of transitions from this condition. Using this activity is equivalent to drawing multiple transitions from a single condition of another activity.

Branching can affect the behavior of rollback activities. See [Rollback To activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-activities/r_RollbackTo.md) for more information.

**Parent Topic:**[Utility workflow activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-activities/c_UtilityActivities.md)

