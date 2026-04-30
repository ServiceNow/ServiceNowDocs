---
title: Map rich controls to the channel in your custom chat integration
description: Create records for rich controls in the Custom Adapter Configurations \[sys\_cs\_custom\_adapter\_config\] table. If a rich control is missing an outbound transformer implementation, a response is not served to the end user and that user may get an unsatisfactory chat experience.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create a Virtual Agent conversational custom chat integration configuration, Creating conversational custom chat integrations in Virtual Agent, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Map rich controls to the channel in your custom chat integration

Create records for rich controls in the Custom Adapter Configurations \[sys\_cs\_custom\_adapter\_config\] table. If a rich control is missing an outbound transformer implementation, a response is not served to the end user and that user may get an unsatisfactory chat experience.

## Before you begin

[Create a channel identifier for your custom chat integration](create-channel-id-va-cccif.md).

Role required: admin

## About this task

You must create a mapping for any rich controls your conversations will use in the channel. For example, you may need a mapping for **DefaultText**, which supports input and output text response, along with file upload and image response. If your channel doesn't support a control, then you won't need to map it. For example, SMS doesn't support video responses. For a description of each default rich control, see [Default input and output rich controls for a custom chat integration](../reference/default-rich-controls-va-cccif.md).

## Procedure

1.  Navigate to **All**, and then enter `sys_cs_custom_adapter_config.list` in the filter.

2.  On the Custom Adapter Configurations page, click **New**.

3.  On the form, fill in the fields.

<table id="table_zbd_nsp_b4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Provider

</td><td>

Provider that you created.

</td></tr><tr><td>

Control type

</td><td>

Default rich control type.For example, the DefaultPicker rich control type maps to File Picker, Topic Picker, and Boolean controls. For more information about the types of controls, see [Default input and output rich controls for a custom chat integration](../reference/default-rich-controls-va-cccif.md).

</td></tr><tr><td>

Inbound transformer action

</td><td>

Name of the inbound transformer action script for this rich control. For example: `sn_va_sms_twilio.va_sms_twilio_adapter_input_text_inbound_transformer`

</td></tr><tr><td>

Outbound transformation action

</td><td>

Name of the outbound transformer action script for this rich control. For example: `sn_va_sms_twilio.va_sms_twilio_adapter_input_text_outbound_transformer`

</td></tr></tbody>
</table>4.  Click **Submit**.


## What to do next

[Create and configure a scripted REST API for your custom chat integration](configure-rest-api-va-cccif.md)

