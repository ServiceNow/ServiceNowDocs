---
title: Grouping multiple findings as remediation tasks for easy processing using remediation task rules
description: Remediation tasks help vulnerability analysts and remediation teams manage findings in bulk. By configuring remediation task rules, you can automatically group findings into remediation tasks, eliminating the need for manual task creation and streamlining remediation efforts.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Automating prioritization and triaging, Security Exposure Management workflow, Explore, Unified Security Exposure Management, Security Operations]
---

# Grouping multiple findings as remediation tasks for easy processing using remediation task rules

Remediation tasks help vulnerability analysts and remediation teams manage findings in bulk. By configuring remediation task rules, you can automatically group findings into remediation tasks, eliminating the need for manual task creation and streamlining remediation efforts.

Remediation task rules define how findings are grouped into tasks. A default rule based on vulnerability is included in the system, but rules can also use other attributes such as:

-   Vulnerability severity or summary
-   Configuration item \(CI\) or product model
-   Assignment group
-   Risk score
-   Technology or attack vector

You can define up to six "Group by" criteria and apply multiple conditions. Once a match is found, the system either adds the finding to an existing Open remediation task or creates a new one. These rules apply to newly created findings or the ones updated with attributes that impact task assignment: Task rules can be reapplied to update groupings as needed. Rules are evaluated after CI matching, risk calculation, and assignment.

**Note:** Excessive rules may impact performance. Ensure that rules are optimized to avoid duplication and inefficiency.

️

## Remediation task rule execution mode

You can configure how remediation task rules are evaluated during finding ingestion by setting the execution mode. Two modes are available:

-   **Match All** \(default\): All applicable rules are evaluated and executed for each finding. A finding can be assigned to multiple remediation tasks if it matches more than one rule.
-   **Match First**: Rules are evaluated sequentially by execution order and only the first matching rule is applied. Each finding is assigned to exactly one remediation task.

You can change the execution mode using any of the following methods:

-   Switch between modes using the label link: Match All or Match First rule on the Remediation task rules page.
-   Navigate to **Security Exposure Management** &gt; **Administration** &gt; **Advanced Settings** and update the Remediation Task Rule Mode setting.
-   Update the sn\_sec\_rem.remediation\_task\_rule\_mode system property directly **All** &gt; **System Properties**. Valid values are match-all and match-first.

## How remediation task rules work

When a new finding is created, imported, or reopened, the system evaluates it against the defined remediation task rules. In Match All mode, all rules are evaluated. In Match First mode, evaluation stops at the first matching rule based on execution order. For each rule where the condition matches, the system pulls the relevant data from the "Group by" selections and builds a group name. If a matching open remediation task exists, the finding is added to it. Otherwise, a new task is created. By default, remediation task rules use the assignment group set by the assignment rules on the finding. The assignment of these remediation tasks is controlled by the assignment rules. When a task rule is deleted, you have the option to delete all open tasks created by that rule.

## Managing remediation task rules

**Reapplying rules**: Use the **Reapply** button on the rule form to rerun the rule on all open remediation tasks it created. The reapplication process deletes and recreates tasks based on the updated rule. Reapply behavior depends on the execution mode:

-   Match First: All rules are reapplied sequentially by execution order. You cannot selectively reapply individual rules. Use the drag handles on the rules list to reorder rules by priority before reapplying.
-   Match All: You can select specific rules to reapply using the checkboxes on the rules list, or reapply all rules at once.

**Deleting rules**: When deleting a rule, you may also delete the open tasks created by it. Tasks not in the Open state remain unaffected.

## Creating and managing remediation tasks

Remediation tasks can be created in the following ways:

-   Automatically using remediation task rules \(recommended for efficiency\).
-   Manually in the IT Remediation Workspace. For more information, see [Create a remediation task manually in the IT Remediation Workspace](../../vr-it-remediation-workspace/task/itr-ws-create-remediation-task.md).

## State synchronization

-   **Rolldown**: When a remediation task state changes \(for example, from Open to Under Investigation, this change is pushed to all associated findings.\)
-   **Rollup**: When all associated findings share a common terminal state \(for example, Deferred, Closed - Fixed\), their state rolls up to the remediation task. Rollup jobs run at scheduled intervals \(for example, every 15 minutes\).

## Assignment management

Assignment groups and assignees from remediation tasks are rolled down to associated findings unless those findings already have different assignments. This roll down helps standardize ownership across all related records.

**Parent Topic:**[Automating prioritization and triaging](sem-automating-prioritization-triaging.md)

**Related topics**  


[Configuring remediation task rules](sem-configure-remediation-task-rules.md#)

