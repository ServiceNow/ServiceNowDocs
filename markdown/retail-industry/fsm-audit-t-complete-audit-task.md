---
title: Complete an audit task
description: The Auditor records the outcome of audit work by setting the Result field to Pass or Fail and moving the task to the completed state.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/fsm-audit-t-complete-audit-task.html
release: australia
topic_type: task
last_updated: "2026-07-09"
reading_time_minutes: 1
breadcrumb: [Manage Store Audit, Retail]
---

# Complete an audit task

The Auditor records the outcome of audit work by setting the Result field to Pass or Fail and moving the task to the completed state.

## Before you begin

-   The Auditor or Audit Admin performing this task must hold `sn_fsm_audit.auditor` or `sn_fsm_audit.audit_admin`.
-   The audit task must be active. Deactivated tasks are read-only for all roles.
-   When custom access rules are active, the Auditor must also have access to the related case or work order.

## Procedure

1.  Open the audit task from the consuming product's task list.

2.  Review the work details on the task.

3.  In the **Result** field, select **Pass** or **Fail**.

4.  Update **State** to the completed state defined by the consuming product's workflow.

5.  Click **Save**.


## Result

The audit task is saved with the Auditor's recorded outcome. The full change history is preserved automatically.

## What to do next

When the consuming product has configured automated follow-on actions — such as notifications or case updates — those trigger after the Auditor saves. Contact the Audit Admin if expected follow-up does not occur.

**Related topics**  


[Audit tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/fsm-audit-tasks.md)

[Components installed with Field Service for Audit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/fsm-audit-reference.md)

