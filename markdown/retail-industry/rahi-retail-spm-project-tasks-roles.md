---
title: Roles and visibility for project tasks
description: Roles determine which store personas see project tasks in Retail, which surfaces they reach, and which actions they can take on a task.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/rahi-retail-spm-project-tasks-roles.html
release: brazil
topic_type: reference
last_updated: "2026-09-17"
reading_time_minutes: 3
keywords: [location\_project\_stakeholder, location\_manager\_project\_stakeholder, project task roles, visible to customer]
breadcrumb: [Reference, Retail]
---

# Roles and visibility for project tasks

Roles determine which store personas see project tasks in Retail, which surfaces they reach, and which actions they can take on a task.

## Roles required

To see project tasks, a store persona needs a retail responsibility and one of the project stakeholder roles. The stakeholder roles are defined by the App SPM Retail dependency. Retail neither defines nor assigns them, and no retail role inherits them.

|Role|Persona|Grants|
|----|-------|------|
|A retail contributor or fulfiller responsibility|Store associate or store manager|Base requirement. A persona needs one of these before a stakeholder role has any effect.|
|`sn_bus_loc.location_project_stakeholder`|Store associate|Access to the project task surfaces for the persona's service organization.|
|`sn_bus_loc.location_manager_project_stakeholder`|Store manager|The same access as the associate role, plus the actions that change assignment.|

**Note:** Access is scoped to the persona's service organization. A persona at one store doesn't see the project tasks of another store, even when they belong to an assignment group that includes members of that store.

## Surfaces by persona

The surfaces aren't all available to the same personas, and the two mobile paths differ from each other.

**Note:** A stakeholder role is always required, and access is scoped to the persona's own store. A persona holding a retail role but no stakeholder role sees none of these surfaces.

|Surface|Available to|Notes|
|-------|------------|-----|
|**Projects** category in the portal|Contributor or fulfiller with a stakeholder role|The category appears whenever the plugin is active and the persona holds a stakeholder role. It isn't hidden when no project tasks are assigned.|
|**Projects** entry on mobile|Contributor or fulfiller with a stakeholder role|Hidden when the persona has no project tasks assigned to their store. This differs from the portal.|
|**Tasks** filter in **My Work** on mobile|Fulfiller with a stakeholder role|A contributor never reaches this filter, because the **My Work** tab is itself limited to fulfillers. A stakeholder role doesn't override that.|

## Actions by persona

|Action|Store associate|Store manager|
|------|---------------|-------------|
|View projects and project tasks for their store|Yes|Yes|
|Add a comment or an attachment|Yes|Yes|
|Close a task|Yes, when the task is assigned to them and has no open child tasks|Yes, on the same conditions|
|**Assign task** and **Assign to me**|Yes, when the persona can change the assignee and the assignment group of the task|Yes, on the same condition, including reassigning a task that is assigned to an assignment group|

Each action is checked separately, so an action appears only when the persona can perform it. The check runs again on the server before the update is applied, and a persona without permission receives a message rather than a silent failure.

**Note:** Whether these actions appear depends on the persona's permission to change the assignee and assignment group fields. That permission is granted by the Customer Service Management \(CSM\) and Retail Strategic Portfolio Management Suite applications, not by Retail. The requirements expect it to sit with the store manager. The portal and the mobile application apply the same rule.

## What makes an individual task visible

-   **The __Visible to customer__ field**

    The project manager sets this field on each project task. A task without it set doesn't appear on any store-facing surface, whatever roles the persona holds.

-   **Service organization scoping**

    A persona sees only the project tasks of the store they belong to.


Record-level access to project and project task records is owned by the Customer Service Management \(CSM\) and Retail Strategic Portfolio Management Suite applications. Retail adds no access control rules or query rules of its own on those tables. Its portal lists filter on the **Visible to customer** field as well, so an unflagged task is excluded before the list reaches the browser.

**Parent Topic:**[Retail reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-operations-reference.md)

**Related topics**  


[Project tasks in Retail](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-spm-project-tasks-overview.md)

[Project task data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-spm-project-tasks-data-model.md)

