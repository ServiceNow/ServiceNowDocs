---
title: Command Validation Tasks form for pattern-based discovery
description: Command Validation Tasks form displays the fields that you must fill when you create or modify a task for testing a pattern command.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Discovery reference, Discovery, ITOM Visibility, IT Operations Management]
---

# Command Validation Tasks form for pattern-based discovery

**Command Validation Tasks** form displays the fields that you must fill when you create or modify a task for testing a pattern command.

For more information about testing pattern commands, see [Validate commands used in pattern-based discovery](../task/validate-discovery-commands.md).

<table id="table_h5t_b2m_c5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

The task number is automatically created by the system.

</td></tr><tr><td>

MID Server Selection Method

</td><td>

Select the relevant method:-   **Specific MID Server** - To define the MID Server for this test.
-   **Automatic MID Selection** - To use a MID Server that's assigned to the IP range or IP network that you want to use for the test. Select this method only if you have configured a MID Server with IP ranges or as a default MID Server for Discovery.
-   **Try All Eligible MID Servers** - To use any MID Server available for the the IP range or IP network that you want to use for the test. Select this method only if you have configured a MID Server with IP ranges or as a default MID Server for Discovery.

</td></tr><tr><td>

MID Server

</td><td>

The MID Server name.This field appears only if **Specific MID Server** is selected from **MID Server Selection Method**.

</td></tr><tr><td>

Validate All Pattern Commands

</td><td>

The check box for validating all commands used by a specific pattern simultaneously.

</td></tr><tr><td>

OS Class

</td><td>

The CI class that represents the servers on which you run this validation task.

</td></tr><tr><td>

Command Type

</td><td>

The command type that depends on the kind of the server:-   **Shell Command**
-   **WMI Query**
-   **SNMP Query** \(Tabular and Scalar\)
-   **SNMP Walk**
-   **HTTP GET** \(for Basic Authentication credentials, not Token\)

 This field is available only when **Validate Al Patterns Commands** isn't selected.

</td></tr><tr><td>

IP Addresses

</td><td>

Any combination of IP v4 Addresses, IP Ranges, or IP networks. For example:-   `10.196.39.12, 10.196.39.12` - Comma-separated IP addresses for a list of standalone addresses.
-   `1.1.1.1-1.1.1.100` - Hyphen-separated IP addresses for an IP range.
-   `1.1.1.1/28` - Slash notation for an IP network.

 **Note:** To use IP range or IP network, ensure you have installed the ParseIPRanges script include. For more information, refer to [KB1123625: Command Validation Tool](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1123625).

</td></tr><tr><td>

Commands

</td><td>

The commands for which you want to test credentials. Typically, it's a command that discovery process failed to execute. For example, **/api/v1/pods?limit=50** or **sudo dmidecode**.You can select only commands from the list of available commands.

 This field is available only when **Validate All Patterns Commands** isn't selected.

</td></tr><tr><td>

Pattern

</td><td>

The name of the pattern for which you want to validate the commands. This field is available only when **Validate All Patterns Commands** isn't selected.

</td></tr></tbody>
</table>**Parent Topic:**[Discovery reference](../../discovery/reference/discovery-references.md)

**Related topics**  


[Command List form for pattern-based discovery](commands-list-discovery.md)

[Discovery commands for probes and patterns](../../discovery/concept/discovery-command-probe-pattern.md)

