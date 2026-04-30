---
title: Geolocation utility
description: Use the Geolocation utility to gather map coordinates from a user, to personalize topics to a user's location, provide data for navigation or on-site tasks, and other services.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Virtual Agent Designer utilities, Virtual Agent Designer interface reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Geolocation utility

Use the Geolocation utility to gather map coordinates from a user, to personalize topics to a user's location, provide data for navigation or on-site tasks, and other services.

## Geolocation utility properties

Specify the flow action properties for the node that you want to create.

<table id="action-utility-properties-sheet-table"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Node name

</td><td>

Name of the Geolocation node.

</td></tr><tr><td class="sub-head" colspan="2">

Input mapping

</td></tr><tr><td>

Permission prompt

</td><td>

String for the custom prompt requesting geolocation from a user.

</td></tr><tr><td class="sub-head" colspan="2">

Output mapping

</td></tr><tr><td>

Latitude

</td><td>

User's latitude returned after the Permission prompt. **Note:** All Output Mappings are customizable. Select **Enable** to activate each one, and input a custom variable name to store the value under if desired.

</td></tr><tr><td>

Longitude

</td><td>

User's longitude returned after the Permission prompt.

</td></tr><tr><td>

Error message

</td><td>

Message returned if the geolocation attempt encounters an error.

</td></tr><tr><td>

Error type

</td><td>

Type of error returned based on the error message.

</td></tr><tr><td>

Status

</td><td>

Status of the geolocation data.

</td></tr><tr><td class="sub-head" colspan="2">

Advanced

</td></tr><tr><td class="sub-head" colspan="2">

Hide this node

</td></tr><tr><td>

Conditionally show this node if

</td><td>

No-code condition statement or low-code script that specifies a condition for presenting this node in the conversation. The condition must evaluate to true.

</td></tr></tbody>
</table>## Example Geolocation utility

![Geolocation utility properties.](../images/flow-designer-geolocation-properties.png)

**Parent Topic:**[Virtual Agent Designer utilities](va-utilities.md)

