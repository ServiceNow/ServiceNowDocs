---
title: Use the Min component
description: Take two integers and find which one is smaller as part of an automation Workflow by using the Min component in RPA Desktop Design Studio.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Math, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the Min component

Take two integers and find which one is smaller as part of an automation Workflow by using the Min component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the Min component. For more information about these properties, see [Properties of the Math components](../reference/properties-math-component.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Math**.

2.  Drag the Min component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the Min component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port type

</th><th>

Purpose of connection

</th><th>

Mandatory?

</th></tr></thead><tbody><tr><td>

Data In \(Value1\)

</td><td>

Takes the first of the two integers that the method compares from a previously executed component.

</td><td>

Yes

</td></tr><tr><td>

Data In \(Value2\)

</td><td>

Takes the last of the two integers that the method compares from a previously executed component.

</td><td>

Yes

</td></tr><tr><td>

Data Out

</td><td>

Returns the smaller of the two integers entered and passes to the next component.

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


**Parent Topic:**[Math](../concept/math.md)

