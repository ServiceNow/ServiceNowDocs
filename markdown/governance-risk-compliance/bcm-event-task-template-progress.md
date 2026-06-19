---
title: Event task creation progress in exercise and crisis events
description: When event tasks are created in bulk from task template groups or task templates, the Event tasks list defers refresh to avoid impacting large events. This topic explains the banner and auto-refresh behavior.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/bcm-event-task-template-progress.html
release: australia
topic_type: concept
last_updated: "2026-05-16"
reading_time_minutes: 1
breadcrumb: [Structured workflows for Exercises, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Event task creation progress in exercise and crisis events

When event tasks are created in bulk from task template groups or task templates, the Event tasks list defers refresh to avoid impacting large events. This topic explains the banner and auto-refresh behavior.

## Progress banner

The banner **The event tasks are updated. Select Refresh to see updated data. List will auto-refresh once all tasks are created.** is shown while the system is creating event tasks from **Add groups** or **Add tasks**. The banner remains visible until the system completes creation.

\[Omitted image "event-tasks-auto-refresh-banner.png"\] Alt text: Yellow banner stating the event tasks are updated, with a Refresh button.

## Auto-refresh window

About ten seconds after the last event task is created, the **Event tasks** list refreshes once. The list is not refreshed each time a task is created, because event task lists can be large. You can also select **Refresh** on the banner at any time to force an immediate refresh.

## Behavior on activated plans

Opening **Add groups** or **Add tasks** from the **Event tasks** tab of an activated plan skips the **Select activated plan** step in the dialog, because the activated plan context is already known. Refresh behavior is identical to the exercise or crisis event **Event tasks** list.

\[Omitted image "activated-plan-event-tasks-grouped.png"\] Alt text: Exercise event Event tasks tab grouped by activated plan.

\[Omitted image "activated-plan-event-task-list.png"\] Alt text: Activated plan event task list showing tasks created from a task template group.

**Parent Topic:**[Structured workflows for Exercises](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/performing-tasks-to-manage-exercise-events.md)

