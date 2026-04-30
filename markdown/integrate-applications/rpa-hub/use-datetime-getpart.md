---
title: Use the GetPart component
description: Get the value of a part of the date format by using the GetPart component in RPA Desktop Design Studio. For example, you might want to get the value of the month in the MM/DD/YYYY format.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [DateTime, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the GetPart component

Get the value of a part of the date format by using the GetPart component in RPA Desktop Design Studio. For example, you might want to get the value of the month in the MM/DD/YYYY format.

## Before you begin

Role required: none

## About this task

You can configure the properties for the GetPart component. For more information about these properties, see [Properties of the DateTime components](../reference/util-datetime-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **DateTime**.

2.  Drag the GetPart component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the GetPart component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port name

</th><th>

Purpose of connection

</th><th>

Port type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

SourceDate

</td><td>

Passes the date and time for which you want to view the part, from a previously executed component.Drag the Now component from DateTime to get today's date as the source date. For example, if the source date is 01-Feb-2025.

</td><td>

Data In

</td><td>

DateTime

</td></tr><tr><td>

Format

</td><td>

Passes the part of the date and format that the value of which is returned, from a previously executed component.For example, enter `MMM`.

</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

Return

</td><td>

Returns the value of the part of the date format.If the format is MMM, the output is Feb.

</td><td>

Data Out

</td><td>

String

</td></tr></tbody>
</table>5.  To test the component, under the **DESIGN** tab, click **Run**.


## GetPart component with Now component

![GetPart component gets a part of the date using Now component as the source date.](../image/getpart-datetime-rpa.png "GetPart component")

**Parent Topic:**[DateTime](../concept/datetime-utility.md)

