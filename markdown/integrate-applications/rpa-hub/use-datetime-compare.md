---
title: Use the Format component
description: Change the format of a date by using the Format component in RPA Desktop Design Studio.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [DateTime, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Use the Format component

Change the format of a date by using the Format component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the Format component. For more information about these properties, see [Properties of the DateTime components](../reference/util-datetime-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **DateTime**.

2.  Drag the Format component to the Design surface.

3.  Click the component settings icon \(![Component settings icon](../image/component-settings-icon.png)\).

4.  Do the following:

    1.  In the From field, specify the date format you want to change.

    2.  In the To field, specify the destination date format.

    3.  Click **OK**.

5.  To configure the input field, see [Configure port properties](configure-input-port-properties.md).

6.  Connect the data and control ports of the Format component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port type

</th><th>

Purpose of connection

</th><th>

Mandatory?

</th></tr></thead><tbody><tr><td>

Data In \(DateObject\)

</td><td>

Passes the date object through the Data Out port of another component. For example, 03-25-2009.

</td><td>

Yes

</td></tr><tr><td>

Data Out

</td><td>

Returns the date object in the destination date format.

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
</table>7.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[DateTime](../concept/datetime-utility.md)

