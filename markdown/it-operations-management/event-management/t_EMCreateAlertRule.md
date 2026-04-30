---
title: Migrate an alert action rule to an alert management rule
description: Existing alert action rules from an earlier release can be executed, but cannot be modified. Alert action rules that have been migrated become alert management rules and all the definitions of the alert action rules are migrated to the alert management rule format. Migrated rules can be modified.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Alert management rules for resolving alerts, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Migrate an alert action rule to an alert management rule

Existing alert action rules from an earlier release can be executed, but cannot be modified. Alert action rules that have been migrated become alert management rules and all the definitions of the alert action rules are migrated to the alert management rule format. Migrated rules can be modified.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

Existing alert action rules are active, read-only rules. An alert action rule can be modified only after it is migrated to an alert management rule.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Rules** &gt; **Alert Action Rules**.

2.  Select an alert action rule to migrate or delete.

    ![Alert Action Rule form](../image/EMAlertRuleForm.png "Alert Action Rule record")

3.  Click **Migrate**.

    If you clicked **Migrate**, the list of migrated rules can be found, together with new alert management rules, by navigating to **Event Management** &gt; **Rules** &gt; **Alert Management**.

    After a successful migration, all the definitions of the alert action rules are migrated to the alert management rule format.


## Result

When an alert action rule has been migrated successfully, the alert action rule can no longer be modified. However, the new alert management rule can be modified.

## What to do next

If the alert action rule that was migrated had a task template, you can customize the alert management rule designer to display the task template name.

1.  In the header of the alert management rule, click **Additional actions** ![Additional actions](../image/additional-actions.png).
2.  Select **Configure** &gt; **Form Layout**.

    ![Form layout](../image/form-layout.png)

3.  In the **Available** pane, select **Task template** and move it to the **Selected** pane. Position it as required.

    ![Task template](../image/task-template.png)

4.  In the **Task template** field, select the required template.
5.  In the Actions tab, in the Remediation Subflows area, select the Create Task \(legacy\) subflow to run the task template.

    ![Subflow to run task template](../image/create-task-legacy.png)


**Parent Topic:**[Alert management rules for resolving alerts](../concept/alert-management-rule.md)

**Related topics**  


[Apply a quick response in an alert](apply-quick-response-in-alert.md)

