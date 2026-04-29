---
title: Use the Format component
description: Provide a placeholder and a value in a body of text by using the Format component in RPA Desktop Design Studio.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [String utilities, Utilities, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the Format component

Provide a placeholder and a value in a body of text by using the Format component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the Format component. For more information about these properties, see [Properties of the String Utilities components](../reference/util-stringutil-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **String Utilities**.

2.  Drag the Format component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

    You must insert is \{0\} as the placeholder.

4.  Connect the data and control ports of the Format component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port type

</th><th>

Purpose of connection

</th></tr></thead><tbody><tr><td>

Data In \(\_Format\)

</td><td>

Passes the text body and the placeholder from a previously executed component.Used to specify the format.

Data type: String

</td></tr><tr><td>

Data In \(Input\)

</td><td>

Used to specify the input string that is replaced in given format.Data type: String

</td></tr><tr><td>

Data Out \(Return\)

</td><td>

Returns the text body with the placeholder value inserted in the placeholder. This method returns a string that represents formatted text.

Data type: String

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

