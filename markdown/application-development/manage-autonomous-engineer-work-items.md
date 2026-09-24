---
title: Manage work items during execution
description: Monitor Autonomous Engineer work items as they build. You can review generated artifacts and test results, resolve work items that require attention, and export the update set when all work items are complete.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/manage-autonomous-engineer-work-items.html
release: brazil
topic_type: task
last_updated: "2026-09-09"
reading_time_minutes: 3
keywords: [Autonomous Engineer, work items, manage, review, retry, roll back, update set, plan dashboard, ATF tests, deploy]
audience: programmer
breadcrumb: [Use, Autonomous Engineer, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Manage work items during execution

Monitor Autonomous Engineer work items as they build. You can review generated artifacts and test results, resolve work items that require attention, and export the update set when all work items are complete.

## Before you begin

An Autonomous Engineer plan must be in execution. To start a plan, see [Use Autonomous Engineer to implement an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/use-autonomous-engineer.md).

Role required: admin

## About this task

During execution, background agents build work items in parallel. You can review work items as they reach a ready-for-review state without waiting for all work items to complete. Work items that require your attention, for example, if a background agent generated a question, are highlighted in the plan dashboard and the chat panel.

## Procedure

1.  From the plan dashboard, open the **Work items** tab to monitor execution progress.

    The Work items tab lists every work item in the plan. Each row shows the work item name and its current state. The list updates as background agents progress. For a description of each state, see [Autonomous Engineer plan and work item states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown).

2.  When a work item reaches a ready-for-review state, select it to open the work item record.

3.  Review the generated artifacts and Automated Test Framework \(ATF\) test results for the work item.

    Each work item record shows the artifacts that the background agent generated and the ATF test results. Verify that the artifacts meet the acceptance criteria listed in the work item before marking it complete.

    \[Omitted image "ae-work-items-dash.png"\] Alt text: Dashboard showing work item execution progress and status counts. For details, refer to the surrounding description.

4.  Take one of the following actions based on your review.

    |Action|Steps|
    |------|-----|
    |Mark complete|If the work item meets your requirements, mark it complete. The dashboard updates the work item state.|
    |Edit and retry|If your requirements changed or the output does not match what you intended, edit the work item content directly in the work item record. Then ask Autonomous Engineer to retry. A new background agent runs for the work item.|
    |Roll back|If you must undo the changes for a work item, roll back that work item. The rollback applies only to the selected work item and does not affect other work items in the plan.|

5.  Repeat steps 2 through 4 for each work item as it becomes ready for review.

6.  When all work items are complete, export the update set that Autonomous Engineer generated for the plan.

    Autonomous Engineer generates a single update set for the plan when all work items reach a complete state. Export the update set from the plan dashboard and deploy it to a test environment for user acceptance testing, or promote it to production.


## Result

Your implementation is captured in an update set that is ready for deployment.

## What to do next

For information about work item states and their definitions, see [Autonomous Engineer plan and work item states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown). For information about how Autonomous Engineer handles stuck or unresponsive agents automatically during execution, see [Resilience in Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ae-resiliency.md).

**Parent Topic:**[Using Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ae-using-autonomous-engineer.md)

