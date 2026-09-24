---
title: Project task data model
description: The project and project task records that Retail reads, the fields it displays, and the three fields it writes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/rahi-retail-spm-project-tasks-data-model.html
release: brazil
topic_type: reference
last_updated: "2026-09-17"
reading_time_minutes: 2
keywords: [customer\_project, customer\_project\_task, project task data model]
breadcrumb: [Reference, Retail]
---

# Project task data model

The project and project task records that Retail reads, the fields it displays, and the three fields it writes.

## Table ownership

Project tasks are stored on tables that the Customer Service Management \(CSM\) and Retail Strategic Portfolio Management Suite applications own. Retail defines no columns on either table.

|Table|Access|Purpose|
|-----|------|-------|
|`customer_project`|Read|The store life cycle project. Shown in the project list and on the project page.|
|`customer_project_task`|Read and write|The work items within a project. Shown in the task lists and on the task page.|

Retail writes only three fields, and only through the task actions: `state`, `assigned_to`, and `assignment_group`. Every other field is read-only from a store persona's perspective. The artifacts that surface these tables install only when the App SPM Retail plugin is present.

## Fields used by this feature

|Field|Table|Used for|
|-----|-----|--------|
|`service_organization`|`customer_project`|Identifies the store that the project belongs to. Used to build the portal breadcrumb.|
|`project_manager`, `state`, `description`, `end_date`|`customer_project`|Project card and project page fields.|
|`visible_to_customer`|`customer_project_task`|The visibility gate. Portal lists filter on this field, so an unflagged task never reaches a store persona.|
|`customer_project`|`customer_project_task`|Links a task to its project. Rendered as a link in the task header.|
|`parent`|`customer_project_task`|Child tasks. Also walked to build the breadcrumb chain of ancestor tasks.|
|`rollup`, `top_task`|`customer_project_task`|Determine whether a task can be closed.|
|`state`|`customer_project_task`|Gates the task actions, and is set when a persona closes a task.|
|`assigned_to`, `assignment_group`|`customer_project_task`|Set by the assignment actions.|
|`number`, `short_description`, `priority`, `end_date`|`customer_project_task`|Task list columns and task card fields.|

**Tip:** The task field labeled **Due date** on the mobile task card reads the `end_date` field, not `planned_end_date`. The `planned_end_date` field is inherited but isn't populated on project task records.

## Task states that close a task

A project task is treated as closed, and its actions are withdrawn, in three states:

-   Closed Complete
-   Closed Incomplete
-   Closed Skipped

In any other state, including Pending, the task is open and its actions remain available subject to the persona's access.

## Relationships

-   A project task references its project through the `customer_project` field.
-   A project task can have child project tasks on the same table, through the `parent` field. The task page lists the immediate children.
-   A project is associated with a store through its `service_organization` field, which resolves to a retail organization.

**Parent Topic:**[Retail reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-operations-reference.md)

**Related topics**  


[Project tasks in Retail](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-spm-project-tasks-overview.md)

[Roles and visibility for project tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-spm-project-tasks-roles.md)

