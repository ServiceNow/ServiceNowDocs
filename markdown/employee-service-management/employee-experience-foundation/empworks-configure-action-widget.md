---
title: Configure task scope and action widget
description: Configure a custom AIX action widget to override the default action group on task list and task detail pages for specific task types in the selected scope. Use this when you need task-specific actions that differ from the standard action group.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/employee-experience-foundation/empworks-configure-action-widget.html
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-07-27"
reading_time_minutes: 2
keywords: [AIX action widget, task configuration, Employee Center action group, Employee Slate, Employee Works]
breadcrumb: [Task configuration, Tasks and requests, Working with Employee Slate capabilities, Employee Slate, Unified Employee Experience, Employee Service Management]
---

# Configure task scope and action widget

Configure a custom AIX action widget to override the default action group on task list and task detail pages for specific task types in the selected scope. Use this when you need task-specific actions that differ from the standard action group.

## Before you begin

Role required: sn\_hr\_sp.esc\_admin or admin

## About this task

Configure a custom AIX action widget when the out-of-the-box action group doesn't meet your needs for a task type.

-   The **AIX action widget** field accepts a custom widget built for your organization and replaces the action group on both list and detail views.
-   The **AI insights** tab appears only when **Applies to** is set to **All** or Employee Slate. AI insights apply only to Employee Slate. A banner on the tab indicates that this configuration has no effect in Employee Center.
-   After an upgrade, existing task configuration records automatically set **Applies to** to **All** and clear the **Use custom script** check box. Your existing AI insights skill configurations continue to work without modification.

## Procedure

1.  Go to **All** &gt; **Employee Center** &gt; **Administration** &gt; **To-dos Configurations**, select a to-dos configuration, and open the **Task Configuration** related list.

2.  Open the task configuration for the required record type, such as **Request**.

3.  In the **Applies to** field, specify the experience that uses this task configuration.

    \[Omitted image "es-insights-action.png"\] Alt text: Task Configuration record with scope selection set to Employee Slate.

    Applies to options:

    -   **All** \(default\): Applies the configuration to both Employee Center and Employee Slate. When **Use widget** is selected on the **Primary Info** tab, both the **Widget** field \(for Employee Center\) and the **AIX widget** field \(for Employee Slate\) are mandatory, each with its own widget parameters.
    -   Employee Center: Only the **Widget** field and **Widget parameters** appear on the **Primary Info** tab. The **AI insights** tab and the Employee Slate **Card Info** tab don't appear, because AI insights apply only to Employee Slate.
    -   Employee Slate: Only the **AIX widget** field \(mandatory\) and **AIX Widget parameters** appear on the **Primary Info** tab. Select the out-of-the-box widget or a custom widget built for your organization.
4.  Go to the **Action** tab.

    \[Omitted image "es-insights-action-group.png"\] Alt text: Task Configuration Action tab with Action group set to Approvals action group and AIX action widget set to Custom action.

    -   Search and select an existing an action group such as `Approvals action group`.
    -   Select a custom action widget built for your organization
    For new task configurations targeting only Employee Slate, configure only the AIX Action Widget.

    **Note:** When you don't add a custom action to the AIX action widget, the action group falls back to Employee Center action behavior.

5.  [Configure a custom AI insights skill for a task type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/empworks-configure-ai-insights-skill.md).

6.  Save the task configuration.


## Result

The custom widget replaces the action group on the task list view and the task detail view.

## What to do next

Clear the **AIX action widget** field to fall back to the Employee Center action group.

**Related topics**  


[Configure action group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/update-approval-hub-action-group.md)

[Configure a custom AI insights skill for a task type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/empworks-configure-ai-insights-skill.md)

