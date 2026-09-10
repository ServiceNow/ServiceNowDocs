---
title: Components installed with Care Team Work Management
description: Several types of components are installed when you activate Care Team Work Management, including script includes, UI actions, and flows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/ctwm-components-installed.html
release: australia
topic_type: reference
last_updated: "2026-04-23"
reading_time_minutes: 1
keywords: [components, script includes, UI actions]
breadcrumb: [Reference, Care Team Work Management, Healthcare Operations, Healthcare and Life Sciences]
---

# Components installed with Care Team Work Management

Several types of components are installed when you activate Care Team Work Management, including script includes, UI actions, and flows.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).

For tables and roles installed with Care Team Work Management, see [Tables installed with Care Team Work Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/ctwm-tables-installed.md) and [Roles installed with Care Team Work Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/ctwm-roles-installed.md).

## UI actions installed with Care Team Work Management

<table id="table_ctwm_ui_actions"><tbody><tr><td>

**UI action name**

</td><td>

**Table**

</td><td>

**Description**

</td></tr><tr><td>

Cancel

</td><td>

Healthcare Orchestration Case \[sn\_hco\_orchestration\_case\]

</td><td>

Cancels the healthcare orchestration case after validating that child tasks can also be cancelled.

</td></tr><tr><td>

Close Case

</td><td>

Healthcare Orchestration Case \[sn\_hco\_orchestration\_case\]

</td><td>

Closes the healthcare orchestration case via the Validate and close cancel cases tasks flow.

</td></tr><tr><td>

Publish

</td><td>

Task Plan Template \[sn\_task\_plan\_template\]

</td><td>

Publishes the task plan template so it can be used to generate cases and tasks. Restricted to the template owner or admins.

</td></tr></tbody>
</table>## Flows installed with Care Team Work Management

<table id="table_ctwm_flows"><tbody><tr><td>

**Flow name**

</td><td>

**Description**

</td></tr><tr><td>

Validate and close cancel cases tasks

</td><td>

Validates the state of all child tasks and closes or cancels the healthcare orchestration case accordingly.

</td></tr></tbody>
</table>## Work configuration components installed with Care Team Work Management

These FSM Work Configuration components isolate Care Team Task business logic from standard field service work orders. Care team tasks can be assigned directly to agents without a qualification or dispatch step.

<table id="table_ctwm_work_configurations"><tbody><tr><td>

**Record**

</td><td>

**Table**

</td><td>

**Description**

</td></tr><tr><td>

Care Team Work Management

</td><td>

Work Configuration \[wm\_work\_configuration\]

</td><td>

Resolves care team tasks to the Care Team SM Configuration, bound to the Care Team Task \[sn\_cto\_task\] table.

</td></tr><tr><td>

Care Team Work Management

</td><td>

SM Configuration \[sm\_config\]

</td><td>

Disables qualification and auto-dispatch for care team tasks, so tasks can be assigned directly to an agent.

</td></tr><tr><td>

Care Team Task Type

</td><td>

Work Type \[wm\_work\_type\]

</td><td>

The work type stamped on care team tasks so FSM's resolver reaches the Care Team SM Configuration.

</td></tr><tr><td>

Care Team Work Management

</td><td>

Work Type Category \[wm\_work\_type\_category\]

</td><td>

Groups the Care Team Task Type work type.

</td></tr></tbody>
</table>A care team task is automatically transitioned to **Assigned** once it is in an open state and has an assignee. No qualification or dispatch step is required.

