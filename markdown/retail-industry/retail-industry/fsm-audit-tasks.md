---
title: Audit tasks
description: The wm\_audit\_task table is a specialized work-management task that represents a single audit work item. It inherits all scheduling, assignment, state, and fulfillment behavior from the platform wm\_task type and adds an audit-specific result field.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-07-28"
reading_time_minutes: 1
---

# Audit tasks

The `wm_audit_task` table is a specialized work-management task that represents a single audit work item. It inherits all scheduling, assignment, state, and fulfillment behavior from the platform `wm_task` type and adds an audit-specific result field.

## Table inheritance

`wm_audit_task` extends `wm_task` \(owned by `sn_wm_core`\). Every column, relationship, business rule, and state machine defined on `wm_task` is available on `wm_audit_task` without duplication. Consuming apps query and update audit tasks using standard GlideRecord APIs against `wm_audit_task`.

## Audit-specific fields

|Field|Type|Default|Description|
|-----|----|-------|-----------|
|`result`|Choice|\(empty\)|The Auditor's outcome — empty \(default\), Pass, or Fail. Set by the Auditor when the audit is complete.|
|`task_plan_template_item`|Reference|\(empty\)|Links the audit task to a task-plan-template item from `sn_task_plan`. **Plugin-gated:** present only when `sn_task_plan` is installed. Scripts must guard access with `current.isValidField('task_plan_template_item')`.|

## Plugin-gated field: task\_plan\_template\_item

The `task_plan_template_item` column is conditionally present:

-   **When `sn_task_plan` is installed:** the field exists on the table and links the audit task to a reusable task-plan-template item.
-   **When `sn_task_plan` is not installed:** the field does not exist on the table.

The column is shipped via XML at `src/main/plugins/com.sn_fsm_audit/if/com.sn_task_plan_templates/dictionary/wm_audit_task.xml` and is not a Fluent SDK artifact. Server-side scripts that read or write this field must guard access with `current.isValidField('task_plan_template_item')` so the same script works in both install configurations.

## Read-only state on inactive records

When an audit task's `active` field is `false`, all fields on the record are read-only regardless of role. This is enforced by a platform UI Policy and cannot be bypassed by any consuming app.

**Related topics**  


[Field Service for Audit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/fsm-audit-overview.md)

[Components installed with Field Service for Audit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/fsm-audit-reference.md)

[Complete an audit task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

