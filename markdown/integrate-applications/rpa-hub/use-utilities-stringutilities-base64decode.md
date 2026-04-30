---
title: Use the Base64Decode component
description: Convert a base64 string to text by using the Base64Decode component in RPA Desktop Design Studio.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [String utilities, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the Base64Decode component

Convert a base64 string to text by using the Base64Decode component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the Base64Decode component. For more information about these properties, see [Properties of the String Utilities components](../reference/util-stringutil-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **String Utilities**.

2.  Drag the Base64Decode component to the Design surface.

3.  To configure the input field, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the Base64Decode component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port type

</th><th>

Purpose of connection

</th><th>

Data port type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

Base64String

</td><td>

Used to specify Base64 string that converts to a normal string.Takes the encoded Base64 string from a previously executed component, such as Base64Encode component.

For example, if you input a value like `1234test` in the Base64Encode component and then connect it to the Base64Decode component, running the components will result in the Base64Encode component encoding the value `1234test` and passing it to the Base64Decode component. The Base64Decode component then decodes the encoded value, such as "MzIzNDIzdGVzdHR0" and retrieves the original output as "1234test".

![Encoded text decoded by Base64Decode component](../image/base64decode-stringutilities-rpa.png "Base64Encode and Base64Decode components")

</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

Return

</td><td>

Returns a string representing plain text.

</td><td>

Data Out

</td><td>

String

</td></tr></tbody>
</table>5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[String utilities](../concept/string-utilities.md)

