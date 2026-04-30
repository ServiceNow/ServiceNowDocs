---
title: Use the Add component
description: Increase or decrease the time or date by the value you specify as part of a Workflow with the Add component in RPA Desktop Design Studio.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [DateTime, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the Add component

Increase or decrease the time or date by the value you specify as part of a Workflow with the Add component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the Add component. For more information about these properties, see [Properties of the DateTime components](../reference/util-datetime-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **DateTime**.

2.  Drag the Add component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the Add component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port type

</th><th>

Purpose of connection

</th><th>

Mandatory?

</th></tr></thead><tbody><tr><td>

Data In \(SourceDate\)

</td><td>

Passes the source date, which is the date or time that the Add component increases or decreases by the value you specify, from a previously executed component.

</td><td>

Yes

</td></tr><tr><td>

Data In \(Type\)

</td><td>

Passes the unit of time from a previously executed component. You can provide the following values:-   Year
-   Month
-   Day
-   Hour
-   Minute
-   Second
-   Millisecond
-   Tick


</td><td>

Yes

</td></tr><tr><td>

Data In \(Value\)

</td><td>

Passes the numeric value by which you want to change the source date, from a previously executed component. For example, if you provide 5 and the source date 10/8/2019, then the new source date will be 10/13/2019.

</td><td>

Yes

</td></tr><tr><td>

Data Out

</td><td>

Returns the updated date and time.

</td><td>

Yes.To preview the data, right-click the **Return** field and click **Preview Data**.

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


**Parent Topic:**[DateTime](../concept/datetime-utility.md)

