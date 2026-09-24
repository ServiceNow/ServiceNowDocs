---
title: Case and task field and role reference
description: Technical reference for case and task field descriptions, role permissions, state transitions, and system components used in the quick case creation feature.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/r\_adhoc-case-task-reference.html
release: brazil
topic_type: reference
last_updated: "2026-07-15"
reading_time_minutes: 3
keywords: [reference, field descriptions, roles, permissions, state transitions, ACL]
breadcrumb: [Quick case and task creation for in-store issues, Retail]
---

# Case and task field and role reference

Technical reference for case and task field descriptions, role permissions, state transitions, and system components used in the quick case creation feature.

## Case fields

When you report an issue, the following fields are created on the case record:

|Field Name|Description|API Name|
|----------|-----------|--------|
|Short Description|Brief summary of the issue \(required\)|`short_description`|
|Description|Detailed explanation of the issue \(optional\)|`description`|
|Store|The retail location associated with the case. Auto-populated for associates; required picker for managers.|`service_organization`|
|Priority|Urgency level \(1–5, with 1 being highest\) \(required\)|`priority`|
|State|Case lifecycle state: New, Open, Closed \(read-only to users\)|`state`|
|Assigned To|Store manager or team member responsible for the case|`assigned_to`|

## Task fields

When you add a task to a case, the following fields are captured:

|Field Name|Description|API Name|
|----------|-----------|--------|
|Short Description|Brief summary of the work \(required\)|`short_description`|
|Description|Detailed instructions or context \(optional\)|`description`|
|Assigned To|Team member responsible for completing the task \(required\). Must be a store associate or manager; cannot be an area/region manager.|`assigned_to`|
|Priority|Urgency level \(1–5\)|`priority`|
|Due Date|Expected completion date \(optional\)|`due_date`|
|State|Task lifecycle: Pending Dispatch, Accepted, Closed Complete \(read-only to users\)|`state`|

## State transitions

Cases progress: **New** \(created\) → **Open** \(assigned\) → **Closed** \(resolved\)

Tasks progress: **Pending Dispatch** \(created\) → **Accepted** \(acknowledged\) → **Closed Complete** \(resolved\)

**Note:** Only managers can close cases. Only the assigned user or a manager can close tasks. If a questionnaire is linked, it must be submitted before the task closes.

## Role and permission matrix

|Action|Associate|Manager|Plan Author|Area/Region Mgr|
|------|---------|-------|-----------|---------------|
|Create case|✓|✓|✓|✓|
|Create task|✓|✓|✓|✓|
|Assign case to self|✗|✓|✗|✗|
|Reassign case|✗|✓|✗|✗|
|Close case|✗|✓|✗|✗|
|Assign task|Store team only|Store team only|Store team only|Store team only|
|Close task|If assigned|✓|✗|✗|

## System components

The quick case creation feature is composed of the following artifacts:

-   **Record Producer: Report an Issue**

    Lightweight form on Retail Service Portal and RSM Mobile for users to report cases. Publishes to both surfaces via a single scoped definition.

-   **SP Widget: Case Actions**

    Portal widget that displays action buttons \(Close, Assign to Me, Edit Case, Add Task\) on the case detail page. Button visibility is state-dependent.

-   **Assignment Rule: Auto-Route to Store Manager**

    Automatically assigns template-originated cases to the store manager on creation.

-   **Service Definition: Create Work Item for Store**

    Maps the Record Producer to the case table and controls form field visibility per role.

-   **UI Messages: Scoped Labels**

    Translatable, scoped UI messages \(e.g., "Add task" in lowercase\) avoid collisions with out-of-the-box labels.

-   **Form Section: Case Edit View**

    Restricts the edit modal to Assignment Group and Assigned To fields only, read-only for other fields.


## Known constraints and limitations

-   Ad-hoc cases \(created without a task-plan-template origin\) are unassigned on creation and require manual triage.
-   Area/Region Managers cannot be assigned to tasks \(can only be assigned to cases if they are the reporter\).
-   Case state field uses integer values in scripts, not display values \(e.g., 0=New, 1=Open, 3=Closed\).
-   Close Case is gated by platform state-flow validity; you cannot force-close a case in an ineligible state.
-   Questionnaires linked to tasks must be submitted before task closure \(hard block, unlike cases\).
-   Bulk case operations and workflows are out of scope for this feature; use Store Plans for multi-item coordination.

**Parent Topic:**[Quick case and task creation for in-store issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/c_adhoc-case-task-creation.md)

