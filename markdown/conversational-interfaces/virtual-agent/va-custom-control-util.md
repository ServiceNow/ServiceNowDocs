---
title: Custom control utility
description: Use the Custom Control utility in a Virtual Agent topic or topic block to reference a custom input control or a custom response control. Custom controls complement the controls provided in Virtual Agent Designer.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Virtual Agent Designer utilities, Virtual Agent Designer interface reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Custom control utility

Use the Custom Control utility in a Virtual Agent topic or topic block to reference a custom input control or a custom response control. Custom controls complement the controls provided in Virtual Agent Designer.

## Custom control utility properties

Specify the properties of the custom input control or custom response control that you are adding to a topic or topic block. For more information about custom controls and their use, see [Customizing Virtual Agent with custom controls](../concept/custom-controls.md).

**Note:** Custom controls do not work on Internet Explorer version 11.

<table id="id_dst_y5v_1tb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Custom control

</td><td>

The name of a custom control asset that has been published in Virtual Agent Designer.

</td></tr><tr><td>

Node name

</td><td>

The name of the custom control you selected.

</td></tr><tr><td>

Input mapping

</td><td>

The variables to be used as input to the selected custom control. For example, the following image has example variables:

 ![Input mapping variables on this custom control include transaction date and time, customer name, and product issue.](../images/map-cc-input-values-topic-block.png)

 The contents of this area change according to the custom control you selected. Options may include string input, referenced records, scripts, and so forth.

</td></tr><tr><td>

Output mapping

</td><td>

The variables to be output by the selected custom control. For example, the following image has example variables that are enabled:

 ![Output mapping variables for this custom control include issue and username.](../images/cc-output-mapping-topic.png)

 The contents of this area change according to the custom control you selected.

</td></tr><tr><td class="sub-head" colspan="2">

Advanced

</td></tr><tr><td class="sub-head" colspan="2">

Hide this node

</td></tr><tr><td>

Conditionally use this node if

</td><td>

A no-code condition statement or low-code script that specifies a condition for presenting this node in the conversation. The condition must evaluate to true.

</td></tr></tbody>
</table>## Example custom control utility

![Custom control utility properties sheet for an input control.](../images/custom-control-utility-properties.png)

**Parent Topic:**[Virtual Agent Designer utilities](va-utilities.md)

