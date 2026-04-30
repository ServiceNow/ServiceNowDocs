---
title: Use the Base64Encode component
description: Encode a string with the base64 algorithm by using the Base64Encode component in RPA Desktop Design Studio.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [String utilities, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Use the Base64Encode component

Encode a string with the base64 algorithm by using the Base64Encode component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the Base64Encode component. For more information about these properties, see [Properties of the String Utilities components](../reference/util-stringutil-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **String Utilities**.

2.  Drag the Base64Encode component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the Base64Encode component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port type

</th><th>

Purpose of connection

</th></tr></thead><tbody><tr><td>

Data In \(Text\)

</td><td>

Passes the text the component encodes from a previously executed component.Used to specify the string that is converted to a Base64 string.

Data type: String

</td></tr><tr><td>

Data Out \(Return\)

</td><td>

Returns the encoded string and passes to the next component.

</td></tr><tr><td>

Control In

</td><td>

Passes the control from the previously executed component.

</td></tr><tr><td>

Control Out

</td><td>

Passes the control to the next component to be executed.

</td></tr></tbody>
</table>5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[String utilities](../concept/string-utilities.md)

