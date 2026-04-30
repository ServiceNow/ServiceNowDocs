---
title: Use the GetPosition component
description: Get the current mouse position on the screen in integer terms by using the GetPosition component in RPA Desktop Design Studio.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Mouse, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Use the GetPosition component

Get the current mouse position on the screen in integer terms by using the GetPosition component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the GetPosition component. For more information about these properties, see [Properties of the Mouse components](../reference/util-mouse-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Mouse**.

2.  Drag the GetPosition component to the Design surface.

3.  Connect the data and control ports of the GetPosition component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port type

</th><th>

Purpose of connection

</th><th>

Mandatory?

</th></tr></thead><tbody><tr><td>

Date Out \(Left\)

</td><td>

Takes the current mouse device position relative to the left of the screen from a previously executed component.

</td><td>

YesTo preview the data, right-click the **Return** field and click **Preview Data**.

</td></tr><tr><td>

Data Out \(Top\)

</td><td>

Takes the current mouse device position relative to the top of the screen from a previously executed component.

</td><td>

YesTo preview the data, right-click the **Return** field and click **Preview Data**.

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

No

</td></tr></tbody>
</table>4.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Mouse](../concept/mouse-utility.md)

