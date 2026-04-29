---
title: Use the GetTextBetween component
description: Find the string characters that are placed between two strings by using the GetTextBetween component in RPA Desktop Design Studio.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [String utilities, Utilities, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the GetTextBetween component

Find the string characters that are placed between two strings by using the GetTextBetween component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the GetTextBetween component. For more information about these properties, see [Properties of the String Utilities components](../reference/util-stringutil-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **String Utilities**.

2.  Drag the GetTextBetween component onto the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the GetTextBetween component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port type

</th><th>

Purpose of connection

</th><th>

Mandatory?

</th></tr></thead><tbody><tr><td>

Data In \(Text\)

</td><td>

Takes the text that the component searches from a previously executed component.

</td><td>

Yes

</td></tr><tr><td>

Data In \(findStr1\)

</td><td>

Takes the first set of string characters that is placed on one side of the string the component searches from a previously executed component.

</td><td>

Yes

</td></tr><tr><td>

Data In \(findStr2\)

</td><td>

Takes the first set of string characters that is placed on the other side of the string the component searches from a previously executed component.

</td><td>

Yes

</td></tr><tr><td>

Data Out

</td><td>

Returns the string between strings and passes to the next component.**Note:** The returned value may include spaces. Spaces between characters are also counted as characters.

</td><td>

Yes

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

No

</td></tr></tbody>
</table>5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[String utilities](../concept/string-utilities.md)

