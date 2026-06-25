---
title: Realign resource assignment to project task using Project Workspace
description: Realign or synchronize the resource assignment dates with the project task dates. This synchronization helps to schedule and align the resource assignments with the timeline of project task.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/resource-management/realign-ra-pws-rmw.html
release: australia
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage resource assignments from Project Workspace, Use, Resource Management Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Realign resource assignment to project task using Project Workspace

Realign or synchronize the resource assignment dates with the project task dates. This synchronization helps to schedule and align the resource assignments with the timeline of project task.

## Before you begin

Role required: it\_project\_manager

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Project Workspace** and open a project.

2.  From the project planning pane, double-click the **Planned start date** or **Planned end date** of a project task to edit the field.

    Use the Resources not synced icon \[Omitted image "resources-not-synced-icon.png"\] Alt text: to synchronize the resource assignments dates with the project dates at a project level.

3.  Select **Ok**.

    If the **sn\_pw.resource\_assignment\_auto\_sync\_enabled** system property is set to true, then the resources sync automatically in the background. The bottom resource pane updates without any action, and the manual sync icon \(resources not synced icon\) is hidden since it's no longer needed. The default value is true. When the property is set to false, manual sync via the icon is still required and resources not synced icon is visible. You must have the pps\_admin role to enable this property.

    Alternatively, select more actions context menu and select Realign resource assignments to synchronize the resource assignments dates with the project dates at a project level.


## Result

The resource assignments dates are synchronized with the project task dates.

**Parent Topic:**[Manage resource assignments from Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/resource-management/use-ra-rmw.md)

**Related topics**  


[Resource assignments in Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-workspace/resource-assignments-pw.md)

[Project Workspace reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-workspace/project-workspace-reference.md)

