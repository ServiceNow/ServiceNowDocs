---
title: Use the GetTextAfter component
description: Find the string characters that are placed after a string by using the GetTextAfter component in RPA Desktop Design Studio.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [String utilities, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the GetTextAfter component

Find the string characters that are placed after a string by using the GetTextAfter component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the GetTextAfter component. For more information about these properties, see [Properties of the String Utilities components](../reference/util-stringutil-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **String Utilities**.

2.  Drag the GetTextAfter component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the GetTextAfter component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port type

</th><th>

Purpose of connection

</th></tr></thead><tbody><tr><td>

Data In \(Text\)

</td><td>

Takes the text that the component searches from a previously executed component.Used to specify the string from where a substring is extracted, beginning at a specific position identified by a string match, and continuing for a specified length.

Data type: String

</td></tr><tr><td>

Data In \(findStr\)

</td><td>

Takes the string characters that the component finds in the text from a previously executed component.Used to specify the string that determines the starting position based on a string match.

Data type: String

</td></tr><tr><td>

Data In \(length\)

</td><td>

Takes the number of characters that the component finds in the text from a previously executed component.Used to specify the number of characters to be extracted from a given string.

Data type: Integer

</td></tr><tr><td>

Data Out

</td><td>

Returns the string the component found and passes to the next component.This method returns a string that represents the text after the search text.

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

