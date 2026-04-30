---
title: Pause utility
description: Use the Pause utility to create a temporary halt in your Virtual Agent conversations.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Virtual Agent Designer utilities, Virtual Agent Designer interface reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Pause utility

Use the Pause utility to create a temporary halt in your Virtual Agent conversations.

## Pause utility properties

Specify the flow action properties for the node that you want to create.

<table id="action-utility-properties-sheet-table"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Node name

</td><td>

Name of the Pause node.

</td></tr><tr><td class="sub-head" colspan="2">

Input mapping

</td></tr><tr><td>

Seconds

</td><td>

Duration of pause. **Note:** Any duration value greater than the maximum defined in the system reverts to the maximum, or 60 seconds if not defined.

</td></tr><tr><td class="sub-head" colspan="2">

Advanced

</td></tr><tr><td class="sub-head" colspan="2">

Hide this node

</td></tr><tr><td>

Conditionally show this node if

</td><td>

No-code condition statement or low-code script that specifies a condition for presenting this node in the conversation. The condition must evaluate to true.

</td></tr></tbody>
</table>## Example Pause utility

![Pause utility properties.](../images/flow-designer-pause-properties.png)

**Parent Topic:**[Virtual Agent Designer utilities](va-utilities.md)

