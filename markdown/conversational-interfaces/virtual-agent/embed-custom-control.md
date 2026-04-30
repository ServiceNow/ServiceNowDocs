---
title: Add a custom control to a Virtual Agent topic or topic block
description: Add a custom control to a Virtual Agent topic or topic block. During the conversation, you can gather inputs from the user or display outputs to the user.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
keywords: [Add, custom control, Virtual Agent, topic, block]
breadcrumb: [Customizing Virtual Agent with custom controls, Exploring other Virtual Agent features, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Add a custom control to a Virtual Agent topic or topic block

Add a custom control to a Virtual Agent topic or topic block. During the conversation, you can gather inputs from the user or display outputs to the user.

## Before you begin

Do the following before you start this task:

-   [Create and publish the custom input or response control](create-custom-control.md).
-   Create a calling topic or topic block in which the custom control will be embedded.

Role required: virtual\_agent\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

2.  On the home page, select the topic where you will add the custom control.

3.  In the **Flow** tab, drag the Custom Control icon from the Utilities section of the palette to the appropriate position in the topic flow.

    **Note:** If you selected **Available on the palette** in the custom control Properties page, the Custom Control displays as its own icon in the Utilities section of the palette.

4.  Select the custom control node.

5.  On the form, fill in the fields.

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
</table>6.  Select **Save**.

7.  To see how your custom control works in the topic, select **Test** in the header bar.

    Your topic runs in a chat test window.

8.  If no further changes are needed, select **Publish** in the Virtual Agent Designer header bar.


## Result

The topic is active. You can deploy it to your Virtual Agent clients.

