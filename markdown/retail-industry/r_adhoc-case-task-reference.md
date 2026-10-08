---
title: Case and task field and role reference
description: Technical reference for case and task field descriptions, role permissions, state transitions, and system components used in the quick case creation feature.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/retail-industry/r\_adhoc-case-task-reference.html
release: australia
topic_type: reference
last_updated: "2026-10-05"
reading_time_minutes: 4
keywords: [reference, field descriptions, roles, permissions, state transitions, ACL]
breadcrumb: [Quick case and task creation for in-store issues, Retail]
---

# Case and task field and role reference

Technical reference for case and task field descriptions, role permissions, state transitions, and system components used in the quick case creation feature.

## Case fields

When you submit the **Create work item for store** form, the following fields are created on the case record:

|Field Name|Description|API Name|
|----------|-----------|--------|
|Short Description|Brief summary of the issue \(required\)|`short_description`|
|Description|Detailed explanation of the issue \(optional\)|`description`|
|Store|The store that the case is for \(required\). Set automatically for store associates and store managers. Area and region managers select it on the form. The system writes the store to both fields.|`service_organization`, `requesting_service_organization`|
|Priority|Urgency level \(1–5, with 1 being highest\) \(required\)|`priority`|
|State|Case lifecycle state: New, Open, Closed \(read-only to users\)|`state`|
|Assigned To|Store manager or team member responsible for the case|`assigned_to`|

## Task fields

When you add a task to a case, the following fields are captured:

|Field Name|Description|API Name|
|----------|-----------|--------|
|Short Description|Brief summary of the work \(required\)|`short_description`|
|Description|Detailed instructions or context \(optional\)|`description`|
|Assigned To|Team member responsible for completing the task \(optional\). The picker isn't restricted by role, so area and region managers can also be selected, but they can't assign tasks themselves.|`assigned_to`|
|Priority|Urgency level \(1–5\) \(required\)|`priority`|
|Due Date|Expected completion date \(optional\)|`due_date`|
|State|Task lifecycle: Pending Assignment, Accepted, Closed Complete \(read-only to users\)|`state`|

## State transitions

Cases progress: **New** \(created\) → **Open** \(assigned\) → **Closed** \(resolved\)

Tasks progress: Pending Assignment \(created, unassigned\) → Accepted \(assigned\) → Closed Complete \(closed\)

Any entitled user can close a case or task at any time. Open tasks don't block closing the case, and resolution notes aren't forced. On the portal, store associates and store managers enter resolution notes when they close a case, and area and region managers confirm the close in a confirmation popup that asks whether they're sure. On Retail Mobile, area and region managers confirm the close in a Yes/No popup. Closing a task asks for confirmation only.

## Role and permission matrix

|Action|Store associate \(`sn_rtl_instore_ops.associate`\)|Store manager \(`sn_rtl_instore_ops.manager`\)|Area or region manager \(`sn_rtl_instore_ops.manager_contributor`\)|
|------|--------------------------------------------------|----------------------------------------------|-------------------------------------------------------------------|
|Create a case|Yes|Yes|Yes, for any store they're mapped to|
|Add a task to a case|Yes|Yes|Yes|
|Assign a case or task|Yes|Yes|No|
|Use **Assign to me**|Yes|Yes|No|
|Edit a case or task|Yes|Yes|Yes, except assignment fields|
|Close a case or task|Yes|Yes|Yes|
|View cases and tasks|All for their store|All for their store|All for every store they're mapped to|

## System components

The quick case creation feature is composed of the following artifacts:

-   **Record producer: Create work item for store**

    Lightweight form on Retail Service Portal and Retail Mobile for users to report cases. Publishes to both surfaces via a single scoped definition.

-   **SP Widget: Case Actions**

    Portal widget on the case detail page. Shows **Close** next to the overflow menu, and **Assign to me**, **Add task**, and **Edit case** in the overflow menu. **Assign to me** appears only for fulfillers of the case's store.

-   **SP Widget: Task Actions**

    Portal widget on the task detail page. Shows **Close task** next to the overflow menu, and **Edit task** and, for fulfillers only, **Assign to me** in the overflow menu.

-   **Retail Mobile screens and actions**

    Case and task record screens for the Retail Mobile app, with state-dependent action buttons in the overflow menu and at the bottom of the screen, plus the Add task, Edit case, Edit task, and Close case input forms.

-   **Business rule: Set case state to Open when assigned\_to is filled**

    Moves a case from New to Open when someone is assigned. Applies only to cases created with **Create work item for store**. The store-manager auto-routing rule used by Store Plans doesn't run for these cases.

-   **Case type selection: Create work item for store**

    Sets the case's service so that cases created from the record producer are identified as quick in-store cases.

-   **UI Messages: Scoped Labels**

    Translatable, scoped UI messages \(e.g., "Add task" in lowercase\) avoid collisions with out-of-the-box labels.

-   **Form Section: Case Edit View**

    Limits the portal edit modal to Priority, Assignment group, Assigned to, Short description, and Description.


## Known constraints and limitations

-   Ad-hoc cases \(created without a task-plan-template origin\) are unassigned on creation and require manual triage.
-   Area and region managers can be assigned cases and tasks, but they can't assign cases or tasks.
-   The state fields use integer values in scripts, not display values. Case: 1 = New, 10 = Open, 3 = Closed. Task: 10 = Pending Assignment, 17 = Accepted, 3 = Closed Complete.
-   Close Case is gated by platform state-flow validity; you cannot force-close a case in an ineligible state.
-   Tasks created this way never get a questionnaire, so the questionnaire close check used by Store Plans doesn't apply.
-   Bulk case operations and workflows are out of scope for this feature; use Store Plans for multi-item coordination.

**Parent Topic:**[Quick case and task creation for in-store issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/retail-industry/c_adhoc-case-task-creation.md)

