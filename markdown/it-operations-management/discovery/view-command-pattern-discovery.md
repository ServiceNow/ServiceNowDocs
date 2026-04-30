---
title: View Patterns commands through the Discovery Patterns module
description: View all the commands required for an infrastructure or application pattern to verify you have sufficient permissions to run discovery.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-02-20"
reading_time_minutes: 1
breadcrumb: [Discovery commands for probes and patterns, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# View Patterns commands through the Discovery Patterns module

View all the commands required for an infrastructure or application pattern to verify you have sufficient permissions to run discovery.

## Before you begin

-   Confirm that the following applications have been installed:
    -   Pattern Designer Enhancements \(sn\_itom\_pde\)
    -   Discovery and Service Mapping Patterns \(sn\_itom\_pattern\)
-   If you’re viewing commands for the first time, have upgraded Discovery and Service Mapping Patterns, or have customized any pattern, refresh the command list by navigating to **All** &gt; **Pattern Designer** &gt; **Command Validation Tool** &gt; **Commands List** and selecting **Refresh Command List**.

Role required: discovery\_admin

## About this task

The discovery\_admin role is required to access the **Discovery Patterns** module. Starting with Pattern Designer Enhancements version 3.9.0, the new pde\_viewer role can view pattern commands through the **Command List** module but can't edit or modify them. For more information, see [View Patterns commands through the Command List module](view-pattern-command-in-command-list.md).

## Procedure

1.  Navigate to **All** &gt; **Pattern Designer** &gt; **Discovery Patterns**.

2.  In the **Name** field, search for the relevant pattern.

3.  Select and hold \(or right-click\) the name of the pattern and select **List Pattern Commands**.


## Result

You’re redirected to the Command List form filtered for the selected pattern.

For more information on the Command List form fields, see [Command List form for pattern-based discovery](../../it-operations-management/reference/commands-list-discovery.md).

**Related topics**  


[Discovery commands for probes and patterns](../concept/discovery-command-probe-pattern.md)

[Validate commands used in pattern-based discovery](../../it-operations-management/task/validate-discovery-commands.md)

[View command validation task results in pattern-based discovery](view-command-validation-task-results.md)

