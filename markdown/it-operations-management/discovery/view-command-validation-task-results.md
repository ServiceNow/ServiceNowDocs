---
title: View command validation task results in pattern-based discovery
description: View the results of command validation tasks to verify you have the correct credentials and permissions to run pattern-based discovery successfully.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Discovery commands for probes and patterns, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# View command validation task results in pattern-based discovery

View the results of command validation tasks to verify you have the correct credentials and permissions to run pattern-based discovery successfully.

## Before you begin

-   Verify that Pattern Designer Enhancements \(sn\_itom\_pde\) is installed.
-   Verify that a command validation task has been created. For more information, see [Validate commands used in pattern-based discovery](../../it-operations-management/task/validate-discovery-commands.md).

Role required: One of the following.

-   discovery\_admin
-   pde\_viewer \(starting with Pattern Designer Enhancements version 3.9.0\)

## About this task

Starting with Pattern Designer Enhancements version 3.9.0, the new pde\_viewer role can view the command validation task results through the **Command Validation Tasks** and **Command Validation Task Results** modules but can't edit or modify them.

## Procedure

1.  Navigate to **All** &gt; **Pattern Designer** &gt; **Command Validation Tool** &gt; **Command Validation Tasks**.

2.  In the **Number** column, search for the relevant command validation task.

3.  Select the relevant command validation task.

4.  Verify that the **Status** field is set to **Complete**.

5.  In the **Command Validation Task Results** tab, check if **FAILURE** appears in the **Result** column.

6.  If any of the commands failed, select the link in the **Command Type** column.

7.  Review the failure description in the **Results Details** column.


## What to do next

If you're using the discovery\_admin role and a command fails, follow the remediation suggestions in the **Open suggestions to troubleshoot failure** related link.

1.  Select the **Open suggestions to troubleshoot failure** link.

    ![Open suggestions to troubleshoot failure](../../it-operations-management/image/pde-command-validation-task-result-suggestion.png)

2.  Follow the instructions in the **Steps to Remediate** window.

**Note:** This functionality isn't available to users with the pde\_viewer role.

**Related topics**  


[Command Validation Tasks form for pattern-based discovery](../../it-operations-management/reference/command-validation-reference.md)

[Discovery commands for probes and patterns](../concept/discovery-command-probe-pattern.md)

[Command List form for pattern-based discovery](../../it-operations-management/reference/commands-list-discovery.md)

