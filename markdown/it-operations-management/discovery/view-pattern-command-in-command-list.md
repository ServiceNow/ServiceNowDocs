---
title: View Patterns commands through the Command List module
description: View and filter infrastructure or application pattern commands by various criteria, including pattern, CI type, or command, to confirm you have all the required permissions.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-11-11"
reading_time_minutes: 1
breadcrumb: [Discovery commands for probes and patterns, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# View Patterns commands through the Command List module

View and filter infrastructure or application pattern commands by various criteria, including pattern, CI type, or command, to confirm you have all the required permissions.

## Before you begin

-   Verify that Pattern Designer Enhancements \(sn\_itom\_pde\) is installed.
-   If you have the discovery\_admin role and match one of these conditions, refresh the command list:

    -   You are viewing commands for the first time
    -   You have customized any pattern
    -   You have upgraded Discovery and Service Mapping Patterns
    You can refresh the command list by navigating to **All** &gt; **Pattern Designer** &gt; **Command Validation Tool** &gt; **Commands List** and selecting **Refresh Command List**.

    **Note:** The pde\_viewer role can't refresh commands.


Role required: One of the following.

-   discovery\_admin
-   pde\_viewer \(starting with Pattern Designer Enhancements version 3.9.0\)

## About this task

Starting with Pattern Designer Enhancements version 3.9.0, the new pde\_viewer role can view commands through the **Command List** module but can't edit or modify them.

## Procedure

1.  Navigate to **All** &gt; **Pattern Designer** &gt; **Command Validation Tool** &gt; **Commands List**.

2.  Filter the command list according to your requirements.

    For more information about the filtering options, see [Command List form for pattern-based discovery](../../it-operations-management/reference/commands-list-discovery.md).


**Related topics**  


[View Patterns commands through the Discovery Patterns module](view-command-pattern-discovery.md)

[Validate commands used in pattern-based discovery](../../it-operations-management/task/validate-discovery-commands.md)

[View command validation task results in pattern-based discovery](view-command-validation-task-results.md)

[Discovery commands for probes and patterns](../concept/discovery-command-probe-pattern.md)

