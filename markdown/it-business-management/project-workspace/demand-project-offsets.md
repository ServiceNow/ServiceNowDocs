---
title: Resource assignment offsets in demand-based projects
description: When you create a project from a demand, resource assignments keep their start dates, and the offset is recalculated in working days based on the project schedule.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-business-management/project-workspace/demand-project-offsets.html
release: australia
product: Project Workspace
classification: project-workspace
topic_type: concept
last_updated: "2026-10-01"
reading_time_minutes: 2
keywords: [resource assignment, offset, demand, project schedule, working days, Project Workspace]
breadcrumb: [Create a project from Project Workspace, Manage projects, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Resource assignment offsets in demand-based projects

When you create a project from a demand, resource assignments keep their start dates, and the offset is recalculated in working days based on the project schedule.

## How offsets work

The **Offset** field on a resource assignment shows, in days, the difference between the start date of the project or task and the start date of the resource assignment.

A demand has no schedule, so the offset on a demand counts every day, including Saturdays and Sundays. A project has a schedule, so the offset on a project counts only the working days defined in that schedule.

When you create a project from a demand, the resource assignments keep their start dates, and the offset is recalculated for the project. This behavior applies when you select **Create Project** in the Related Links of a demand.

## Key benefits

This behavior provides the following benefits:

-   Resource assignments start on the dates that were planned in the demand.
-   Weekends and holidays that the demand didn't account for don't push assignments to later dates.
-   The offset matches how the project schedule counts time, so the dates and the offset stay consistent.

## How it works

When a demand is converted to a project, the following happens:

1.  Each resource assignment keeps its start date.
2.  The offset is recalculated as the number of working days between the project start date and the assignment start date.
3.  The working days come from the schedule in the **Schedule** field of the project.

For example, a demand and its project both start on August 3, and a resource assignment starts on August 17. The offset for the same assignment is shown in the following table.

|Record|Assignment start date|Offset|Days counted|
|------|---------------------|------|------------|
|Demand|August 17|14 days|Every day|
|Project|August 17|10 days|Working days in the project schedule|

The assignment keeps its start date. The offset drops from 14 to 10 because the two weekends between August 3 and August 17 aren't counted.

## Considerations

Consider the following when you work with offsets in projects created from a demand:

-   Holidays and other non-working days that are defined in the schedule aren't counted in the offset.
-   The **Schedule** field of the project is populated with a default schedule, Project Management Schedule, in which the working days are Monday to Friday. The default schedule can be replaced with a different one.

**Parent Topic:**[Create a project from Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/project-workspace/create-project-from-project-workspace.md)

**Related topics**  


[Resource assignment form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/project-workspace/pw-resource-assignment-form.md)

[Resource assignments in Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/project-workspace/resource-assignments-pw.md)

[Assign a project schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/project-management/t_UseAProjectSchedule.md)

