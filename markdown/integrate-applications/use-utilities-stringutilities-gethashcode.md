---
title: Use the GetHashCode component
description: Generate a HashCode from a string by using the GetHashCode component in RPA Desktop Design Studio.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [String utilities, Utilities, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the GetHashCode component

Generate a HashCode from a string by using the GetHashCode component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the GetHashCode component. For more information about these properties, see [Properties of the String Utilities components](../reference/util-stringutil-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **String Utilities**.

2.  Drag the GetHashCode component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the GetHashCode component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port type

</th><th>

Purpose of connection

</th></tr></thead><tbody><tr><td>

Data In \(Text\)

</td><td>

Takes the string from a previously executed component.Used to specify the string from where the hashcode is computed.

Data type: String

</td></tr><tr><td>

Data Out \(Return\)

</td><td>

Returns the generated HashCode and passes to the next component.Data type: String

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

