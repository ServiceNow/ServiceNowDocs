---
title: Use the Confirm component
description: Set a confirmation message that is shown in a dialog box requiring user inputs by using the Confirm component in the RPA Desktop Design Studio.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [General, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the Confirm component

Set a confirmation message that is shown in a dialog box requiring user inputs by using the Confirm component in the RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

The Confirm component is used as part of an Attended Robot automation. Use this component to request a confirmation from the user as a response to a user action. For example, request user inputs on whether the user wants to save a file.

To configure the properties, see [Properties of Confirm components](../reference/Properties-general-components.md#confirm-components).

## Procedure

1.  In the Toolbox pane, navigate to **General** &gt; **MessageBox**.

2.  Drag the Confirm component to the Design surface.

3.  To provide inputs to the parameters, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the Confirm component to the corresponding ports of the other components as described in the following table.

<table id="table_gtq_gq1_ntb"><thead><tr><th>

Port type

</th><th>

Port name

</th><th>

Data type

</th><th>

Purpose of connection

</th><th>

Default value

</th><th>

Mandatory?

</th></tr></thead><tbody><tr><td>

Data in

</td><td>

Message

</td><td>

String

</td><td>

Takes the confirmation message from another component.

</td><td>

No default value

</td><td>

Yes

</td></tr><tr><td>

Data out

</td><td>

Return

</td><td>

Boolean

</td><td>

Returns the Boolean value based on the user input.If True, the user has clicked **Ok**. Else, if False, the user has clicked **False**.

</td><td>

Not applicable

</td><td>

Not applicable

</td></tr></tbody>
</table>5.  To test the component, right-click the component bar and click **Run From Here**.


**Parent Topic:**[General](../concept/general-component.md)

