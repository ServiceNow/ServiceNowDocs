---
title: Realign resource assignments with project dates
description: Realign or synchronize the resource assignment dates with the project task dates. This synchronization helps to schedule and align the resource assignments with the timeline of project task.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/project-workspace/realign-resource-assignment-to-task.html
release: australia
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Resource assignments in Project Workspace, Resource planning with Project Workspace, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Realign resource assignments with project dates

Realign or synchronize the resource assignment dates with the project task dates. This synchronization helps to schedule and align the resource assignments with the timeline of project task.

## Before you begin

Role required: it\_project\_manager

## About this task

When you change project dates, a prompt appears to realign resource assignments to the updated dates. However, if you skip this step, resource assignments go out of sync with the project. To prevent this, use the **sn\_pw.resource\_assignment\_auto\_sync\_enabled** system property to realign all resource assignments across projects automatically on a periodic basis.

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Project Workspace** and open a project.

2.  From the project planning pane, double-click the **Planned start date** or **Planned end date** of a project task to edit the field.

    Use the Resources not synced icon \[Omitted image "resources-not-synced-icon.png"\] Alt text: to synchronize the resource assignments dates with the project dates at a project level.

3.  Select **Ok**.

    If the **sn\_pw.resource\_assignment\_auto\_sync\_enabled** system property is set to true, then the resources sync automatically in the background. The bottom resource pane updates without any action, and the manual sync icon \(resources not synced icon\) is hidden since it's no longer needed. The default value is true. When the property is set to false, manual sync via the icon is still required and resources not synced icon is visible. You must have the pps\_admin role to enable this property.

    Alternatively, select more actions context menu and select Realign resource assignments to synchronize the resource assignments dates with the project dates at a project level.


## Result

The resource assignments dates are synchronized with the project task dates.

## Realign resource assignments with project dates

Jason \(Project Manager\) updates the end date of a project from June 30 to August 31. The system prompts the Jason to realign resource assignments, but Jason closes the prompt without running the realignment. As a result, resource assignments still reflect the original end date of June 30. If the system property is configured, it runs automatically and realigns all resource assignments to the updated project dates without any manual action required.

**Parent Topic:**[Resource assignments in Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-workspace/resource-assignments-pw.md)

**Related topics**  


[Resource assignments in Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-workspace/resource-assignments-pw.md)

[Project Workspace reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-workspace/project-workspace-reference.md)

