---
title: Integrate custom controls
description: Implement and leverage custom controls built using the custom control framework in your integration.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Supported Virtual Agent and Agent Chat features for custom chat integrations, Creating conversational custom chat integrations in Virtual Agent, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Integrate custom controls

Implement and leverage custom controls built using the custom control framework in your integration.

## Before you begin

Role required: virtual\_agent\_admin or admin

## About this task

Map custom controls to a provider channel.

-   **Implement custom controls created in Workflow Studio**

    Use the example script to implement custom controls created in Workflow Studio.

    Example: Custom controls support

    ```
    {
        uiType: "CustomControl",
        group: "DefaultCustomControl",
        name: "The name of the Custom Control (sys_cs_custom_control.name)",
        required: true/false,
        uxComponentDefinitionSysId: "seismicComponentId" // or null if not
        isInput: true/false, // whether to wait for a response value or if just output
        serializedControlData: "User defined JSON from generateControlData function";    
    }
    ```

    Example: Custom controls script

    ```
    (function execute(inputs, outputs) {
        var rich_controls = inputs.rich_control;
        //this is the data returned from the 'serialized control data function' defind in designer
        var serializedControlData = rich_control['serializedControlData'];
        // if this rich control will require a response to move forward in topic flow
        var isInput = rich_control['isInput'];
        // if the component is suggesting using a Seismic control (web) that handles this
        var uxComponentDefinitionId = rich_control['uxComponentDefinitionSysId'];
        // the name of the custom control
        var name - rich_control['name'];
    
        // 1) now perform some logic to transform this data into a custom ui (slack/facebook/sms ascii art/html/etc)
        // 2) attach to outputs, i.e. outputs.text_message='foo :)'; for sms twillio
    
        // basic flow is to take the serializedControlData/Name/compId(optional) and create a custom UI component here
        // that your client understands (i.e. a slack rich form payload)
    })(inputs, outputs);
    ```

-   **Implement a provider-specific transformation of a custom control**

    You can implement a provider-specific transformation for each custom control by using the **Sub type** field in the Custom Adapter Configuration \[sys\_cs\_custom\_adapter\_config\] table. You can publish a newer version of a custom control or a pre-built, ServiceNow custom control, also referred to as a default custom control, if needed. This involves publishing the appropriate Inbound and Outbound Workflow Studio action scripts and updating the configuration in the Custom Adapter Configuration \[sys\_cs\_custom\_adapter\_config\] table.

    -   If you're publishing your own version of a ServiceNow custom control, overwrite the custom control record in the Custom Adapter Configuration table with your own Inbound and Outbound action script names.
    -   Only one record with the same **Sub type** is allowed. If the same custom control is implemented by two different parties, only one can update the existing record with new Inbound and Outbound transformers.
    **Note:** Once you override an existing custom control record, the system uses the new version of the custom control. For example, transformation scripts can transform multiple custom controls, such as Time Picker and Auth. If you add a Time Picker control with different inbound and outbound transforms, the newer Time Picker control is used. You cannot revert to the original version of the custom control.


## Procedure

1.  Navigate to **All**, and then enter `sys_cs_custom_adapter_config.list` in the filter.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_zbd_nsp_b4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Provider

</td><td>

The name of the channel identifier for your custom chat integration. For details, see [Create a channel identifier for your custom chat integration](create-channel-id-va-cccif.md).

</td></tr><tr><td>

Control type

</td><td>

Select the custom control that you designed. For custom controls, the type is always DefaultCustomControl.

 To learn more about custom controls, see [Customizing Virtual Agent with custom controls](../concept/custom-controls.md).

</td></tr><tr><td>

Sub type

</td><td>

Name of the custom control.

</td></tr><tr><td>

Inbound transformer action

</td><td>

Name of the inbound transformer action script for this rich control, such as, sn\_va\_sms\_twilio.va\_sms\_twilio\_adapter\_input\_text\_inbound\_transformer.

</td></tr><tr><td>

Outbound transformation action

</td><td>

Name of the outbound transformer action script for this rich control, such as, sn\_va\_sms\_twilio.va\_sms\_twilio\_adapter\_input\_text\_outbound\_transformer.

</td></tr></tbody>
</table>4.  Select **Submit**.


**Parent Topic:**[Supported Virtual Agent and Agent Chat features for custom chat integrations](../concept/va-features-custom-chat-integrations.md)

