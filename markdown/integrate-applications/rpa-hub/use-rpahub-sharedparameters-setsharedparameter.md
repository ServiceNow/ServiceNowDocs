---
title: Use the SetSharedParameter component
description: Update the value of a specific shared parameter that you had set for multiple bot processes on the RPA Hub by using the SetSharedParameter component in the RPA Desktop Design Studio.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Shared Parameters, RPA Hub, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Use the SetSharedParameter component

Update the value of a specific shared parameter that you had set for multiple bot processes on the RPA Hub by using the SetSharedParameter component in the RPA Desktop Design Studio.

## Before you begin

Set at least one shared parameter and associate multiple bot processes on the RPA Hub. For more information, see [Create a shared parameter in RPA Hub](../../rpa-hub/task/create-shared-parameter.md) and [Assign a bot process to a shared parameter](../../rpa-hub/task/assign-botprocess-shared-parameter.md).

Assign the automation to the bot process by using the **Assign bot process** option in the **Design** tab of RPA Desktop Design Studio. For more information, see [Assign bot process to an automation project](assign-bot-process.md).

Role required: none

## About this task

You can configure the properties for the SetSharedParameter component. For more information about these properties, see [Properties of the shared parameters](../reference/properties-rpahub-shared-parameters.md).

## Procedure

1.  In the Toolbox pane, navigate to **RPA Hub** &gt; **Shared Parameters**.

2.  Drag the SetSharedParameter component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the SetSharedParameter component to the corresponding ports of the other components.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port type

</th><th>

Purpose of connection

</th><th>

Mandatory?

</th></tr></thead><tbody><tr><td>

Data In \(Name\)

</td><td>

Takes the name of the shared parameter that you had set for bot processes in the RPA Hub from a previously executed component.

</td><td>

Yes.To pass the variable name, double-click the **Name** field and enter the variable name.

</td></tr><tr><td>

Data In \(Value\)

</td><td>

Takes the new value of the shared parameter that you had set for bot processes in the RPA Hub from a previously executed component.

</td><td>

Yes.To pass the variable value, double-click the **Value** field and enter the value.

</td></tr><tr><td>

Data Out \(Return\)

</td><td>

Returns the Boolean response to whether the existing shared parameter value was replaced and passes to the next component.

</td><td>

Yes.To view the output, right-click the **Return** field and select **Preview Data**.

</td></tr><tr><td>

Control In

</td><td>

Connects to the Control Out port of one or more components.

</td><td>

Yes

</td></tr><tr><td>

Control Out

</td><td>

Connects to the Control In port of another component or the default end component.

</td><td>

Yes

</td></tr></tbody>
</table>5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Shared Parameters](../concept/shared-parameters.md)

