---
title: Create a custom control definition
description: Define a custom input or response control definition that maps to a custom component.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-09-16"
reading_time_minutes: 1
breadcrumb: [Customizing Virtual Agent with custom controls, Exploring other Virtual Agent features, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Create a custom control definition

Define a custom input or response control definition that maps to a custom component.

## Before you begin

A custom control definition needs a custom component. For example, a slider input control uses a custom slider component. To begin, create the customizable component that you will use for your control.

Role required: virtual\_agent\_admin or admin

## About this task

For a given custom control, create a separate control definition for each channel in which the control will be used.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Custom Control Definitions**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_yfl_rhc_bpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the custom control to be created.

</td></tr><tr><td>

Type

</td><td>

Type of custom control. Choices are as follows:-   Input
-   Response


</td></tr><tr><td>

Domain

</td><td>

Domain in which this control is used.

</td></tr></tbody>
</table>4.  Select **Submit**.

5.  Open the custom control record that you just created.

6.  In the Custom Control Definitions related list, select **New**.

7.  On the form, fill in the fields.

<table id="table_p2p_shq_cmb"><thead><tr><th>

Field

</th><th>

Descrlption

</th></tr></thead><tbody><tr><td>

Channel

</td><td>

Channels in which your control can be used. The channel is a chat client, such as a web client or messaging app, that is supported in Virtual Agent.

 If your control can be used in more than one channel, create a Custom Control Definition for each channel. If channels are defined, then the custom control can only run in the specified channels.

</td></tr><tr><td>

Application

</td><td>

Scope that this control belongs to.

</td></tr><tr><td>

UX Component Definition

</td><td>

List of custom components that are created for use as custom controls in Virtual Agent.

 Choose an optional component for your custom control.

</td></tr><tr><td>

Domain

</td><td>

Domain where this control is used.

</td></tr></tbody>
</table>8.  Select **Submit**.


## Result

The custom control definition is available for use. You can specify it when you create the appropriate control in Virtual Agent Designer.

## What to do next

[Create the custom control](create-custom-control.md) in Virtual Agent Designer.

