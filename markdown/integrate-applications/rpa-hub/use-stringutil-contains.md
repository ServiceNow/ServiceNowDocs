---
title: Use the Contains component
description: Check whether a body of text contains a specified text by using the Contains component in the RPA Desktop Design Studio.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [String utilities, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the Contains component

Check whether a body of text contains a specified text by using the Contains component in the RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the Contains component. For more information about these properties, see [Properties of the String Utilities components](../reference/util-stringutil-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **String Utilities**.

2.  Drag the Contains component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the Contains component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port type

</th><th>

Purpose of connection

</th></tr></thead><tbody><tr><td>

Data In \(Text\)

</td><td>

Takes the text that the component searches from a previously executed component. Data type: String

</td></tr><tr><td>

Data In \(textToSearch\)

</td><td>

Takes the text that the component tries to find from a previously executed component.Used to specify the string that must be checked, whether it is available or not.

Data type: String

</td></tr><tr><td>

Data In \(IgnoreCase\)

</td><td>

Takes the Boolean value to indicate whether the component ignores the case while searching for the text.Used to specify the boolean value. If value is false, it checks the case sensitive, otherwise it ignores the case sensitive.

Data type: Boolean

</td></tr><tr><td>

Data Out

</td><td>

Returns the Boolean response to whether the text searched was found and passes to another component.Data type: Boolean

</td></tr><tr><td>

Control In

</td><td>

Connects to the Control Out port of one or more components.

</td></tr><tr><td>

Control Out

</td><td>

Connects to the Control In port of another component or the default end component.

</td></tr></tbody>
</table>5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[String utilities](../concept/string-utilities.md)

