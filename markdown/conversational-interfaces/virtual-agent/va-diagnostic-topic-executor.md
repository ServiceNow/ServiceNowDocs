---
title: Diagnostic Topic Executor utility
description: Use the Diagnostic Topic Executor utility in Virtual Agent to ensure the proper function of components in a topic.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Virtual Agent Designer utilities, Virtual Agent Designer interface reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Diagnostic Topic Executor utility

Use the Diagnostic Topic Executor utility in Virtual Agent to ensure the proper function of components in a topic.

## Diagnostic Topic Executor utility properties

Specify the flow action properties for the node that you want to create.

<table id="action-utility-properties-sheet-table"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Node name

</td><td>

Name of the node.

</td></tr><tr><td class="sub-head" colspan="2">

Input mapping

</td></tr><tr><td>

Diagnostic content

</td><td>

String that is passed to the component being diagnosed.

</td></tr><tr><td class="sub-head" colspan="2">

Output mapping

</td></tr><tr><td>

Is topic executed

</td><td>

Option to confirm that the topic executed properly, with variable data returned by the component. Select **Enable** to activate, and enter a custom variable name for the value if desired.

</td></tr><tr><td>

Is data collection topic executed

</td><td>

Option to confirm that the data collection executed properly, with variable data returned by the component. Select **Enable** to activate, and enter a custom variable name for the value if desired.

</td></tr><tr><td class="sub-head" colspan="2">

Advanced

</td></tr><tr><td class="sub-head" colspan="2">

Hide this node

</td></tr><tr><td>

Conditionally show this node if

</td><td>

No-code condition statement or low-code script that specifies a condition for presenting this node in the conversation. The condition must evaluate to true.

</td></tr></tbody>
</table>## Example Diagnostic Topic Executor utility

![Properties include the node name, a diagnostic string, and output variables that indicate whether the topic executed or collected data.](../images/flow-designer-diagnostic-topic-executor-properties.png)

**Parent Topic:**[Virtual Agent Designer utilities](va-utilities.md)

