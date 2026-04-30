---
title: Command List form for pattern-based discovery
description: The Command List form contains all commands used in discovery by infrastructure or application type patterns.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Discovery reference, Discovery, ITOM Visibility, IT Operations Management]
---

# Command List form for pattern-based discovery

The **Command List** form contains all commands used in discovery by infrastructure or application type patterns.

For information on viewing a list of commands used by a pattern, see [View Patterns commands through the Discovery Patterns module](../../discovery/task/view-command-pattern-discovery.md).

<table id="table_brg_3yh_fwb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Applicable OS Class

</td><td>

The command is intended to run on this OS class.

</td></tr><tr><td>

CI Type

</td><td>

The pattern that contains this command is assigned to this CI type. **Note:** Some ServiceNow applications refer to CI types as CI classes.

</td></tr><tr><td>

Command

</td><td>

The discovery command.

</td></tr><tr><td>

Command Type

</td><td>

Type of command:-   **Shell Command**
-   **WMI Query**
-   **SNMP Query** \(Tabular and Scalar\)
-   **SNMP Walk**
-   **HTTP GET** \(for Basic Authentication credentials, not Token\)

</td></tr><tr><td>

Is Failover Step

</td><td>

This command is used in a failover step inside a pattern. Possible values are true or false.

</td></tr><tr><td>

Outdated

</td><td>

This field is for internal use. Possible values are true or false.

</td></tr><tr><td>

Pattern

</td><td>

The command is part of this discovery pattern.

</td></tr><tr><td>

Step name

</td><td>

Name of the step that contains this command.

</td></tr><tr><td>

Domain

</td><td>

The command is validated for discovering CIs in this domain. This field is applicable for domain-separated environment.

</td></tr></tbody>
</table>**Parent Topic:**[Discovery reference](../../discovery/reference/discovery-references.md)

**Related topics**  


[Command Validation Tasks form for pattern-based discovery](command-validation-reference.md)

[Discovery commands for probes and patterns](../../discovery/concept/discovery-command-probe-pattern.md)

