---
title: Create an action from another task
description: Create an action from another task in the Digital Factory Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/industrial-connected-workforce/digital-factory-workspace/create-action-from-another-task.html
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Action Management, Industrial Workflows, Use, Digital Factory Workspace, Industrial Connected Workforce]
---

# Create an action from another task

Create an action from another task in the Digital Factory Workspace.

## Before you begin

You can create an action from an existing action, deviation, breakdown or root cause analysis.

Role required: sn\_icw.action\_user or sn\_icw.action\_expert

## Procedure

1.  Navigate to **Lists** \(\[Omitted image "list-view.png"\] Alt text: List icon.\) in the Digital Factory Workspace.

2.  Select the task that you want to be the parent of the new action.

3.  Select the three-dot menu at the top corner and select **Create action**.

    A new form for the action opens with automatically populated fields for:

    -   Short description
    -   Description
    -   Functional location
    -   Equipment
    -   Opened by
    -   Assignment group
    -   Assigned to
    -   Impact
    -   Urgency
    -   Priority
    -   Due date
    -   Parent \(not available on the form\)
4.  On the Action form, fill in or change the values for the fields.

    For a description of the field values, see [Action form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/action-form.md).

5.  Select **Save**.


## Result

The new action is displayed in the **Tasks** list of the parent task. The parent task cannot be closed until all child tasks in the **Tasks** list are closed.

**Parent Topic:**[Action Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/industrial-action-management.md)

