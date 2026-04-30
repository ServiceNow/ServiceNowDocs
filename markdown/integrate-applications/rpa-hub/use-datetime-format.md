---
title: Use the Compare component
description: Compare two dates and time to find out whether the dates are the same by using the Compare component in RPA Desktop Design Studio.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [DateTime, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the Compare component

Compare two dates and time to find out whether the dates are the same by using the Compare component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the Compare component. For more information about these properties, see [Properties of the DateTime components](../reference/util-datetime-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **DateTime**.

2.  Drag the Compare component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the Compare component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port type

</th><th>

Purpose of connection

</th><th>

Mandatory?

</th></tr></thead><tbody><tr><td>

Data In \(date1\)

</td><td>

Passes the first date of the two dates to be compared, from a previously executed component.

</td><td>

Yes

</td></tr><tr><td>

Data In \(date2\)

</td><td>

Passes the second date of the two dates to be compared, from a previously executed component.

</td><td>

Yes

</td></tr><tr><td>

Data Out

</td><td>

Returns one of the values based on the comparison result:-   **-1** if the first date is earlier than the second.
-   **0** if the first and second dates are the same.
-   **1** if the first date is later the second date.


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

