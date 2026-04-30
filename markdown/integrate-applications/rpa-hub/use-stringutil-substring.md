---
title: Use the SubString component
description: Retrieve a substring from a string by using the SubString component in RPA Desktop Design Studio. You can specify the start character position and length of the substring.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [String utilities, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the SubString component

Retrieve a substring from a string by using the SubString component in RPA Desktop Design Studio. You can specify the start character position and length of the substring.

## Before you begin

Role required: none

## About this task

You can configure the properties for the SubString component. For more information about these properties, see [Properties of the String Utilities components](../reference/util-stringutil-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **String Utilities**.

2.  Drag the SubString component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the SubString component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port type

</th><th>

Purpose of connection

</th><th>

Mandatory?

</th></tr></thead><tbody><tr><td>

Data In \(String\)

</td><td>

Takes the string from which the component creates a substring from a previously executed component.

</td><td>

Yes

</td></tr><tr><td>

Data In \(startindex\)

</td><td>

Takes the index position value of the string characters from a previously executed component.For example, if RPA is the string and 2 is the index value, the substring starts from the character"A" and is A.

</td><td>

Yes

</td></tr><tr><td>

Data Out \(String\)

</td><td>

Returns the substring and passes to the next component.

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

