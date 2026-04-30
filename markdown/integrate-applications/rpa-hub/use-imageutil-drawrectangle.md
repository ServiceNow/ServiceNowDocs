---
title: Use the DrawRectangle component
description: Draw a rectangle on an image and specify its dimensions as part of an automation Workflow by using the DrawRectangle component in RPA Desktop Design Studio.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Image Utilities, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Use the DrawRectangle component

Draw a rectangle on an image and specify its dimensions as part of an automation Workflow by using the DrawRectangle component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the DrawRectangle component. For more information about these properties, see [Properties of the Image Utilities components](../reference/util-imageutil-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Image Utilities**.

2.  Drag the DrawRectangle component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the DrawRectangle component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port type

</th><th>

Purpose of connection

</th><th>

Mandatory?

</th></tr></thead><tbody><tr><td>

Data In \(Image\)

</td><td>

Takes the image on which the method draws a rectangle from a previously executed component.

</td><td>

Yes

</td></tr><tr><td>

Data In \(Top\)

</td><td>

Takes the top measurement from a previously executed component.

</td><td>

No

</td></tr><tr><td>

Data In \(Left\)

</td><td>

Takes the left measurement from a previously executed component.

</td><td>

No

</td></tr><tr><td>

Data In \(Height\)

</td><td>

Takes the height of the rectangle from a previously executed component.

</td><td>

No

</td></tr><tr><td>

Data In \(Width\)

</td><td>

Takes the width of the rectangle from a previously executed component.

</td><td>

No

</td></tr><tr><td>

Data In \(Color\)

</td><td>

Takes the color of the rectangle in hex values from a previously executed component.

</td><td>

Yes

</td></tr><tr><td>

Data In \(Thickness\)

</td><td>

Takes the border thickness of the rectangle from a previously executed component.

</td><td>

Yes

</td></tr><tr><td>

Data Out

</td><td>

Returns the image after drawing a rectangle with the specified dimensions.

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


**Parent Topic:**[Image Utilities](../concept/image-utilities.md)

