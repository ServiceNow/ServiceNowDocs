---
title: Deflection utility
description: Use the Deflection utility in Virtual Agent to track issues that Virtual Agent helped to resolve or actually resolved for a user.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Virtual Agent Designer utilities, Virtual Agent Designer interface reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Deflection utility

Use the Deflection utility in Virtual Agent to track issues that Virtual Agent helped to resolve or actually resolved for a user.

## Deflection utility properties

Specify the flow action properties for the node that you want to create.

<table id="action-utility-properties-sheet-table"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Node name

</td><td>

Name of the Deflection node.

</td></tr><tr><td class="sub-head" colspan="2">

Input mapping

</td></tr><tr><td>

Deflection configuration

</td><td>

Select from a list of pre-defined deflection configurations. For more information, see [Create deflection configurations and patterns](../task/set-up-deflection-settings-va.md).

</td></tr><tr><td>

Deflection pattern

</td><td>

Select from a list of pre-defined deflection patterns. Ensure that your selection is tied to a pre-defined deflection. See [Create deflection configurations and patterns](../task/set-up-deflection-settings-va.md) for more.

</td></tr><tr><td>

Activity table

</td><td>

Table name where the deflection activity occurs. Add incident or task tables related to the deflection.

</td></tr><tr><td>

Activity IDs

</td><td>

List of comma-separated Activity IDs. Add AI Search results or related tasks in the deflection occurrence.

</td></tr><tr><td class="sub-head" colspan="2">

Advanced

</td></tr><tr><td class="sub-head" colspan="2">

Hide this node

</td></tr><tr><td>

Conditionally show this node if

</td><td>

No-code condition statement or low-code script that specifies a condition for presenting this node in the conversation. The condition must evaluate to true.

</td></tr></tbody>
</table>## Example Deflection utility

![Action utility properties.](../images/flow-designer-deflection-properties.png)

**Parent Topic:**[Virtual Agent Designer utilities](va-utilities.md)

