---
title: Use the WriteToCSV component
description: Write the data to a CSV file by using the WriteToCSV component in RPA Desktop Design Studio as part of a Workflow.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data Writer, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the WriteToCSV component

Write the data to a CSV file by using the WriteToCSV component in RPA Desktop Design Studio as part of a Workflow.

## Before you begin

Role required: none

## About this task

You can configure the properties for the WriteToCSV component. For more information about these properties, see [Properties of the Data Writer components](../reference/util-datawriter-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Data Writer**.

2.  Drag the WriteToCSV component to the Design surface.

3.  Connect the data and control ports of the WriteToCSV component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port Name

</th><th>

Port type

</th><th>

Purpose of connection

</th><th>

Data Type

</th></tr></thead><tbody><tr><td>

FilePath

</td><td>

Data In

</td><td>

Passes the path to the CSV file.

</td><td>

String

</td></tr><tr><td>

Data Table

</td><td>

Data In

</td><td>

Passes the data to be written to the CSV file from a previously executed component. The port accepts data in the Data Table format.

</td><td>

Table

</td></tr><tr><td>

Delimiter

</td><td>

Data In

</td><td>

Passes the delimiter from a previously executed component. You can specify a custom delimiter, such as, comma.

</td><td>

String

</td></tr><tr><td>

Append

</td><td>

Data In

</td><td>

Indicate whether the data passed appends or replaces existing data in the CSV file \(True or False\). Double click to configure the port properties. For more information, see [Configure port properties](configure-input-port-properties.md).

</td><td>

Boolean

</td></tr></tbody>
</table>4.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Data Writer](../concept/datawriter-utility.md)

