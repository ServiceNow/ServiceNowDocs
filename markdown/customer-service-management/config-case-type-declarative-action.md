---
title: Configure case type declarative actions
description: Configure declarative actions that enable agents to create cases and case tasks from different locations within CSM Configurable Workspace.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring customer service case types, Customer service case types, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Configure case type declarative actions

Configure declarative actions that enable agents to create cases and case tasks from different locations within CSM Configurable Workspace.

## Before you begin

Role required: admin

## About this task

The Customer Service Case Types plugin includes declarative actions that enable agents to create cases and case tasks using the [case type selector](../concept/csm-case-type-select-modals.md) and [case task type selector](../concept/csm-case-task-type-select-modal.md). These declarative actions are disabled by default.

|Action label|Location|Action|
|------------|--------|------|
|**Create Case**|Appears on the Case Task list views.|Displays the case task type selector.|
|**Create Case**|Appears on the Tasks related list tab on case and case type records.|Displays the case task type selector.|
|**Create Case**|Appears on the Case and Case Type list views.|Displays the case type selector.|

Declarative actions are stored in the Action Assignment \[sys\_declarative\_action\_assignment\] table.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Declarative Actions** &gt; **Form Actions**.

    The system displays the Action Assignments list.

2.  Filter the list to display the actions for the CSM Case Types application.

    If necessary, configure the list to display the **Application** column.

3.  For each of the desired declarative actions, set the **Active** field to true.


