---
title: Use the WriteText component
description: Write the data to a text document as part of an automation Workflow by using the WriteText component in RPA Desktop Design Studio. You can add the data in string format to existing string on the text file or replace the existing data with new data.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data Writer, Utilities, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the WriteText component

Write the data to a text document as part of an automation Workflow by using the WriteText component in RPA Desktop Design Studio. You can add the data in string format to existing string on the text file or replace the existing data with new data.

## Before you begin

Role required: none

## About this task

You can configure the properties for the WriteText component. For more information about these properties, see [Properties of the Data Writer components](../reference/util-datawriter-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Data Writer**.

2.  Drag the WriteText component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the WriteText component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port type

</th><th>

Purpose of connection

</th><th>

Mandatory?

</th></tr></thead><tbody><tr><td>

Data In \(Filepath\)

</td><td>

Passes the path to the text file from a previously executed component.

</td><td>

Yes

</td></tr><tr><td>

Data In \(Data\)

</td><td>

Passes the string to be written to the text file from a previously executed component.

</td><td>

Yes

</td></tr><tr><td>

Data In \(Append\)

</td><td>

Passes the Boolean value to indicate whether the string passed appends or replaces existing data in the text file. The values are:-   True: Appends to the existing string.
-   False: Replaces the existing string.


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

Connects to the Control In port of any other component.

</td><td>

No. Connecting the port is optional.

</td></tr></tbody>
</table>5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Data Writer](../concept/datawriter-utility.md)

